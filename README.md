<img src="https://github.com/rhiokim/large-scale-frontend/raw/master/media/rhino-wide.png" width="50%" />

```
Development
 \_ Manage source code and local dev automation
 \_ Focus on code without additional work
```

## Purpose

Save your life with large scale frontend

## Guide

### Workflow

#### Git

* Commit Message Convention
  * Side Effects
    * Easy to make release notes & Change logs
  * Good Convention Guidelines
    * 😀 [Angular Team Guidelines](https://github.com/angular/angular/blob/master/CONTRIBUTING.md#commit)
    > This guide is quite awesome when you wirte any kind of open source libraries
    * 😊 [Erlang - Writing good commit message](https://github.com/erlang/otp/wiki/Writing-good-commit-messages)
    > And this is also good option
  * Tool to save your life
    * [Commitizen](https://github.com/commitizen/cz-cli)

#### Hooking

* Side Effects
  * Reduce human error immediatly when you work with git every time. In other words, you don't need to care of it at all
* NPM
  * [npm-scripts](https://docs.npmjs.com/misc/scripts)
* Git
  * [description] https://github.com/typicode/husky
  * [description] https://github.com/marionebl/commitlint
  * [description] https://github.com/okonet/lint-staged

#### CI

* Google Cloud Build
* Travis
* Circle

#### CD

* Cloud
  * AWS
  * Now.sh
  * Digital Ocean
  * Heroku
* Static Web Publishing
  * Netlify
  * Surge
  * Github gh-pages

#### Versioning

* Side Effects
* Tools
  * NPM
  * Yarn
  * np

#### Documentation

* Manaual
  * Gitbook
  * Flybook
* README.md
  * https://github.com/jfmengels/all-contributors-cli
* CHANGELOG.md
* LICENSE.md
* Comments

### Application Architecture

* 코드베이스
  * Monorepo
    * What?
    * Why?
    * When?
    * How?
  * 분산/MSA
  * 공통 모듈라이징
* 환경
  * 모바일
    * WebView
  * 데스크탑
  * 그외
  * 디버깅

### Modern Framwork

* Web Component
* Router
* React.js
* Vue.js

### State Management

* Redux/Vuex

### Code Quality

* Typing
* Lint

### Testing

[Wikipedia](https://en.wikipedia.org/wiki/Software_testing##Testing_levels)

모던 웹 애플리케이션 테스팅 환경은 과거에 비해 월등히 좋아지고 있으며 러닝커브가 낮아지고 있다.

2013년 초부터 웹 컴포넌트 기반 개발 환경이 바탕이 되면서 최근 2015년부터는 본격적으로 체계가 갖춰진 테스트를 유지할 수 있게 되었다. 테스트의 방식과 테스트 레벨의 중요도가 달라지고 있다.

큰 사이즈의 확장 가능한 애플리케이션을 유지하기 위해선 아래에 제시한 몇가지 테스트 환경 구축과 테스팅 전략에 대해서 충분히 이해하면 좋다.

* Unit(스냅샷)
  * Jest
  * Mocha
* E2E
  * [Nightwatch.js](http://nightwatchjs.org/)
  * [Cypress.io](https://www.cypress.io/)
  * [Jest with Puppeteer](https://github.com/smooth-code/jest-puppeteer)

### Debugging

* Logging in Production
  * Node.js
  * Web Application
    * Sentry

### Performance

* PWA
* SEO
* Bundling
* Minify
* NginX Configuration
  * This can help your server improve the SPA(Single Page Application) and web site's performance and security, while also ensuring that resources are served with the correct content-type and are accessible, if needed, even cross-domain.
  * [Configuration your web server to prevent caching](https://github.com/vuejs-templates/pwa/blob/development/docs/prevent_caching.md)
  * [Caching best practices & max-age gotchas](https://jakearchibald.com/2016/caching-best-practices/)
  * [HTML5 Boilerplate Nginx Configuration](https://github.com/h5bp/server-configs-nginx)
* Tools
  * Lighthouse - https://developers.google.com/web/tools/lighthouse/?hl=ko
  > Lighthouse 는 웹 앱의 품질 개선을 위한 오픈소스 자동화 도구

### The Design of Principles

* Design Ops
* Definition
  * token
  * element
  * component
  * pattern
  * template
* Component Design

#### CSS

### DDD

### Etc

* SoC
* Modularization
  * Common Regular Expression
    * Email
    * Name
    * Phone
    * Number Format
    * Time
    * Date
    * Zip Code

## Contribute

## LICENSE