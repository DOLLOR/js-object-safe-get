# js-object-safe-get

```javascript
const safeGet = (data, path, defaultValue) => {
  if (!path) return defaultValue;
  let paths = path.split('.');
  let res = data;
  while (paths.length) {
    res = res[paths.shift()]
    if (res == null) return defaultValue;
  }
  return res;
};
```
