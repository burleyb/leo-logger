# Leo-Logger
Such an awesome logger that we had to break it out from the LEO SDK and make it its own project!

## Available methods
 * sub
 * info
 * json
 * time
 * timeEnd
 * log
 * debug
 * error
 * configure

## Available configuration options
 * a = all
 * t = time
 * i = info
 * d = debug
 * e = error
 * T = printTimestamp

## Usage example:
```bash
export LEO_LOGGER='/.*/d'
```

## Working with namespaces
You can log logs for specific namespaces by passing a string when requiring the leo-logger. Example:
```javascript
const logger = require('leo-logger')('my-special-namespace');
```
When you use a namespace, logging works the same, but the output will be prefixed with the namespace:
```javascript
logger.log('My namespaced log');
// outputs: my-special-namespace my namespaced log
```

If you want to display logs for certain namespaces only, you can adjust LEO_LOGGER to match the namespace.
```bash
# Example outputting all logs for my-special-namespace
export LEO_LOGGER='/my\-special\-namespace/a'
```

### Loggers
```javascript
logger.log('my logged message');
logger.info('my info');
logger.debug('just some debugging code');

```

### Timers
```javascript
// start a timer
logger.time('myTimer');
// stop a timer
logger.timeEnd('endTimer');
```

## To-Do
More documentation with examples with code and output.

# Support
Want to hire an expert, or need technical support? Reach out to the Leo team: https://leoinsights.com/contact
