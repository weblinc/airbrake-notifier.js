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
        /* path defaults to /notifier_api/v2/notices.xml */
        path : '/notifier_api/v2/notices.xml',
        /* Configurations below are optional */
        defaults : {
            url       : window.location.href,
            component : 'product',
            action    : 'show',
            session   : { name: 'genericUser', accountType: 'normal' },
            params    : { query: 'javascript', type: 'json' } 
        },
        errorIgnore : [], // Array of regexes of errors to ignore
        userAgentIgnore : [], // Array of regexes of user agent strings to ignore
        backtraceIgnore : [] // Array of regexes of files in a backtrace to ignore
    });
</script>
```

Contributing
---

This project uses [smoosh](https://github.com/fat/smoosh) for compiling, linting.
