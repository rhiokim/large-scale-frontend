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

* Unit(스냅샷)
* E2E

### Debugging

* Logging in Production
  * Node.js
  * Web Application

### Performance

* PWA
* SEO
* Bundling
* Minify
* NginX Configuration
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