# Update

- Head to https://tellidasubscriptions.launchaco.com/
- edit the website
- export it locally
- rename file to index.html
- remove the launchaco ad
- add the tracking script at the bottom of the index
- commit and push to master, it will be deployed by Netlify

```
<script type='text/javascript'>
  //some default pre init
  var Countly = Countly || {};
  Countly.q = Countly.q || [];

  //provide countly initialization parameters
  Countly.app_key = '49f43958cf5f74cde981a3b400ebcd6653da65fa';
  Countly.url = 'https://t.outofscreen.com';

  Countly.q.push(['track_sessions']);
  Countly.q.push(['track_pageview']);
  Countly.q.push(['track_clicks']);

  //load countly script asynchronously
  (function() {
      var cly = document.createElement('script'); cly.type = 'text/javascript';
      cly.async = true;
      //enter url of script here
      cly.src = 'https://t.outofscreen.com/sdk/web/countly.min.js';
      cly.onload = function(){Countly.init()};
      var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(cly, s);
  })();
</script>
```
