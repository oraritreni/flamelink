> All the methods that you would need to work with the Flamelink "Settings" are available on the `app.settings` namespace.

---

!> Support for multiple environments and locales are currently in development. Once these exciting features are released, you will be able to set up multiple languages and streams for your development. This will allow you to have different data for "production", "staging", "development", etc.

On initialization of your Flamelink app instance, you should specify the environment you want to connect to, as well as the default locale. If no environment is specified, the default environment will be `"production"` and the locale will be `"en-US"`.

```javascript
import * as firebase from 'firebase';
import flamelink from 'flamelink';

const app = flamelink({
  ... other config ...
  env: 'production',
  locale: 'en-US'
});
```

---

## .setEnvironment()

If you want to set the environment to something else after instantiation, you can easily do so with the `setEnvironment()` method:

```javascript
app.settings.setEnvironment('staging')
  .then(env => console.log(`Your environment is set as "${env}"`)
  .catch(error => console.error('Something went wrong while setting the environment. Details:', error);
```

### Input parameters

The `.setEnvironment()` method takes a single parameter

- `{String}` `env`: The environment you want to set.

### Return value

A `Promise` that resolves to the set environment `{String}` on success or will reject with an error if an unsupported environment is set.

---

## .getEnvironment()

To retrieve the currently selected environment, you can do so with the `getEnvironment()` method:

```javascript
app.settings.getEnvironment()
  .then(env => console.log(`Your environment is set as "${env}"`)
  .catch(error => console.error('Something went wrong while retrieving the environment. Details:', error);
```

### Input parameters

The `.getEnvironment()` method takes no parameters

### Return value

A `Promise` that resolves to the currently set environment `{String}` on success.

---

## .setLocale()

If you want to set the locale to something else after instantiation, you can easily do so with the `setLocale()` method:

```javascript
app.settings.setLocale('en-GB')
  .then(locale => console.log(`Your locale is set as "${locale}"`)
  .catch(error => console.error('Something went wrong while setting the locale. Details:', error);
```

### Input parameters

The `.setLocale()` method takes a single parameter

- `{String}` `locale`: The locale you want to set.

### Return value

A `Promise` that resolves to the set locale `{String}` on success or will reject with an error if an unsupported locale is set.

---

## .getLocale()

To retrieve the currently selected locale, you can do so with the `getLocale()` method:

```javascript
app.settings.getLocale()
  .then(locale => console.log(`Your locale is set as "${locale}"`)
  .catch(error => console.error('Something went wrong while retrieving the locale. Details:', error);
```

### Input parameters

The `.getLocale()` method takes no parameters

### Return value

A `Promise` that resolves to the currently set locale `{String}` on success.

---

> 🔥🔥🔥 **Pretty sure your keyboard's melting from all that hot code you're dropping** 🔥🔥🔥
