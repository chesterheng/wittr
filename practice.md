2.4 Registering a Service Worker

```git
git checkout task-register-sw
```

File: public/js/main/IndexController.js
```javascript
IndexController.prototype._registerServiceWorker = function() {
  // TODO: register service worker
  if(!navigator.serviceWorker) return;

  navigator.serviceWorker.register('/sw.js').then(function () {
    console.log('Registration worked!');
  }).catch(function () {
    console.log('Registration failed!');
  });
};
```

2.3 Adding a Service Worker To the Project

File: public/js/sw/index.js
```javascript
self.addEventListener('fetch', function(event) {
  console.log(event.request);
});
```
