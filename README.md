# adlist
Various ad and anti-feature blocking rules. Works best with [uBlock Origin](https://github.com/gorhill/uBlock).

To install, copy this to your blocker (for uBlock: Options → 3rd-party-filters → Custom):

```
https://gitlab.com/notpushkin/adlist/raw/master/filters.txt
```

Optionally, add these dynamic filtering rules as well:

```
* disqus.com * block
* disquscdn.com * block
* facebook.com * block
* facebook.net * block
* fbcdn.net * block
* google-analytics.com * block
* googleadservices.com * block
* googletagservices.com * block
facebook.com facebook.com * noop
facebook.com facebook.net * noop
facebook.com fbcdn.net * noop
```

Finally, you can [block third-party iframes as well][3pfr]:

```
* * 3p-frame block
# To unbreak recaptcha you'll need to whitelist google though:
* google.com * noop
```

[3pfr]: https://github.com/gorhill/uBlock/wiki/Dynamic-filtering:-Benefits-of-blocking-3rd-party-iframe-tags