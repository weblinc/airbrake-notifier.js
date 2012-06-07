airbrake-notifier.js
======

Client-side error notifier for Airbrake/Hoptoad

Usage
---

Call `AirbrakeInit` after the inclusion of `airbrake-notifier.js`. `key`, `host` and `env` are required.

```
<script src="airbrake-notifier.js"></script>
<script>
    AirbrakeInit({
        key  : 'abcdefabcdefabcdefabcdefabcdef11',
        host : 'localhost:3000',
        env  : 'production',
        defaults : {
            url       : window.location.href,
            component : 'product',
            action    : 'show',
            session   : { name: 'genericUser', accountType: 'normal' },
            params    : { query: 'javascript', type: 'json' } 
        }
    });
</script>
```

Contributing
---

This project uses [smoosh](https://github.com/fat/smoosh) for compiling, linting.
