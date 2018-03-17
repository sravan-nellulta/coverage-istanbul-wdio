# Front-end JavaScript test coverage with Istanbul and WebDriverIO (Selenium)

Sample code-base to generate test coverage with integration testing using WDIO(WebDriverIO)

## Highlevel understanding

1. Generate instrument code using command:`istanbul instrument`

```
istanbul instrument test/web.js --output  test/web.inst.js --embed-source true
(or)
npm run inst
```

2. Link instrumented js with web applucation instead of actual code
3. Run integration testing using WDIO 
4. Save `coverage.json` by executing script on web app `window.__coverage__`
```
wdio
(or)
npm run test
```
5. Generate viewable report `coverage/lcov-report/index.html` from `coverage.json` by using `istanbul report`
```
node reporter.js
(or)
npm run report
```
5. Open Coverage report on browser `open coverage/lcov-report/index.html`


## Installation

install istanbul
```
npm i -g istanbul
npm i -D istanbul
```

Install wdio
```
npm i -g webdriverio
```

Install Selenium Standalone
```
npm i -g selenium-standalone
selenium-standalone install
```

Start Selenium Standalone
```
selenium-standalone start
```