Running

```
"start": "ng serve",
"build": "ng build",
"export": "ng build --prod && cat dist/angular-web-component/runtime-es2015*.js dist/angular-web-component/polyfills-es2015*.js dist/angular-web-component/main-es5*.js > export/info-box.js && cp dist/angular-web-component/styles.*.css export/info-box.css && cp dist/angular-web-component/index.html export/index.html",
"live": "npx http-server export",
```

Embed 

```
  <info-box signupTitle="Hola" thankyouMessage="Daniel"></info-box>
  <script src='https://raw.githack.com/danielnaranjo/angular-widger-demo/dev/export/info-box.js'></script>
```
or
```
  <script type="text/javascript" charset="utf-8">
    window.addEventListener('load', () => {
      const widgetElement = document.createElement('info-box')
      // document.body is not necessary here, it can be any other element
      document.body.appendChild(widgetElement) 
      const widgetCode = document.createElement('script')
      widgetCode.src = 'https://raw.githack.com/danielnaranjo/angular-widger-demo/dev/export/info-box.js'
      document.body.appendChild(widgetCode)
    })
</script>
```