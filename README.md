<img src="https://github.com/rhiokim/large-scale-frontend/raw/master/media/rhino-wide.png" width="50%" />

```
Development
 \_ Manage source code and local dev automation
 \_ Focus on code without additional work
```

## Purpose

Save your life with large scale frontend architecture

## Guide

Base -> Development -> Build -> Test -> Maintain -> Refactor

-> Workflow
  -> SCM
    -> Co-Working
      -> Code Quality
        -> Continuous Integration
          -> Continuous Delivery
            -> Versioning
              -> Documentation

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

#### Code Quality

* Typing
* Lint

#### CI(Continuous Integration)

* Google Cloud Build
* Gitlab Pipeline
* [AWS CodeBuild](https://aws.amazon.com/ko/codebuild/)
* Travis
* Circle CI

#### CD(Continuous Delivery)

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
  * semver
    * https://semver.org/
    * https://docs.npmjs.com/misc/semver

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
* Universal Rendering
  * Next.js
  * Nuxt.js
  * Others?
* Serverless
  * zeit/now
  * google
* 환경
  * 모바일
    * Native Interfaces with Web Application
  * 데스크탑
  * 그외
  * 디버깅

#### WACQA(Web Application Consideration Tree)

> WACQA is just LGTM

* Client-side
  * Framework - How much time we can spend for that?
    * How to manages dependencies?
    * How to migrate version issue?
    * Learning costs
    * Pros & Cons for our goals
    * Tooling costs
  * Responseive
    * Browser
    * Mobile
    * TV
  * PWA
    * Service Worker
    * Web Push
  * SEO
    * Will we happy with SEO?
  * Universal Rendering - SSR
    * Really need this to archive our goal?
  * Static Typing
    * Can you answer me why we are need this thing on our project?
  * i18n - Internationalization
  * a11y - Web Accessibility
  * Testing - unit(snapshot), e2e and others?
  * Browers Capability
  * CSS - Pre-processor (SASS/Less/Stylus) and JSS
* Backend-side
  * coming up

### Modern Framwork

* Web Component
* Router
* React.js
* Vue.js

### Style

* CSS
  * css
  * inline style
  * CSSModules
  * styled-component

### State Management

과거 MVC 패턴이 웹 애플리케이션을 구현의 대부분이였던 시절에 애플리케이션의 상태관리는 각 Model 과 Controller 에 의해서 관리되어졌다. 물론 그때 당시의 상태관리는 그렇게 복잡하지 않았다. 아니 그렇게 복잡한 상태를 관리할 애플리케이션을 구현하지 않았다.

하지만 모던 웹 브라우저의 기술을 급속도로 발전하고 웹 애플리케이션의 구조도 급속도로 변화하였다.

웹 애플리케이션의 구현 패턴도 MVC 에서 2013년을 기점으로 마크업, 스타일시트를 단일 파일에 담은 웹 컴포넌트의 형태로 변화하면서 상태관리의 복잡함을 단방향 데이터 흐름(Uni-direction Data Flow)으로 그 패러다임을 발전시켜오고 있다.

더불어 다양한 언어와 환경의 경험들이 웹 상태머신의 패러다임에 영향을 주고 있다.

* Flux
  * Uni-Direction Data Flow
* Redux
* React
  * [Context Provider](https://reactjs.org/docs/context.html)
  * [Hooks](https://reactjs.org/docs/hooks-intro.html)
* Vuex
  * Action
  * Getter
  * Mutation
  * Module
  * Computed
* Saga
  * [What is saga?](https://engineering.universe.com/what-is-redux-saga-c1252fc2f4d1)
* GraphQL
* Observable
  * Rx
  * MobX
    * TFRP(transparently applying functional reactive programming)

---

* We **have to** understand about general state machine - https://en.wikipedia.org/wiki/Finite-state_machine

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

### User Analysis

* 사용자 분석 전략
* 퍼널(funnel) 디자인 방법

### Logging & Auditing

* for Debug
* for Tracing
  * Node.js
    * Morgan
  * Web Application
    * Sentry - [sentry.io](https://sentry.io)
  * Mobile

### Security

대부분의 보안은 프론트엔드 즉 브라우저 영역에서 발생하는 경우는 그다지 중요도고 높지 않게 느낀다.
과거도 현재도, 이 섹션에서는 보안의 중요성, 필요성에 대한 정보보다 보안 취약점이 발생할 수 있는
다양한 위험 요소를 인식하고 예방할 수 있는 방법들에 대해 크게 2가지 영역 Node.js, Browser 다루는 것을 목적으로 한다.

Node.js 의 경우 서버 프로그래밍을 넘어서 웹 애플리케이션에 여러 영향을 주고 있다.
더불어 시스템을 제약없이 엑세스 할 수 있기 때문에 단순히 웹 보안을 넘어서 시스템 보안의 취약점까지
발생할 수 있다.

#### Node.js

* 10 npm Security Best practices - https://snyk.io/blog/ten-npm-security-best-practices/
* npm audit - https://docs.npmjs.com/cli/audit
* nsp - https://www.npmjs.com/package/nsp

#### Browser

Google Web Fundmental - https://developers.google.com/web/fundamentals/security?hl=ko
* Content Security Policy - https://developers.google.com/web/fundamentals/security/csp?hl=ko

### Performance

* This! Good start point - https://www.smashingmagazine.com/2019/01/front-end-performance-checklist-2019-pdf-pages/
* PWA
* SEO
* Bundling
  * Code Splitting
  * Tree Shaking
* Minify
* NginX Configuration
  * This can help your server improve the SPA(Single Page Application) and web site's performance and security, while also ensuring that resources are served with the correct content-type and are accessible, if needed, even cross-domain.
  * [Configuration your web server to prevent caching](https://github.com/vuejs-templates/pwa/blob/development/docs/prevent_caching.md)
  * [Caching best practices & max-age gotchas](https://jakearchibald.com/2016/caching-best-practices/)
  * [HTML5 Boilerplate Nginx Configuration](https://github.com/h5bp/server-configs-nginx)
* Tools
  * Lighthouse - https://developers.google.com/web/tools/lighthouse/?hl=ko
  > Lighthouse 는 웹 앱의 품질 개선을 위한 오픈소스 자동화 도구


### Optimization

* Assets
  * Image
  * CSS

### The Design of Principles

* Design Ops
* Definition
  * token
  * element
  * component
  * pattern
  * template


#### Design System

* https://designsystemsrepo.com/design-systems/

#### Component Design

* Layout
  * Grid
* Motion & Animation
* Colors
  * Pattern
  * HEX
  * RGBA
  * HSLA
* Sizing

#### CSS

* Structured CSS
* Preprocessor
* CSS in JS


## Strategies & Methodologies

### Modularization

In every developer's life. We are considerating every day how to write high reusable code.

We **have to** understand about Separation of concerns (aka SoC) - https://en.wikipedia.org/wiki/Separation_of_concerns

* Common Regular Expression
  * Email
  * Name
  * Phone
  * Number Format
  * Time
  * Date
  * Zip Code

### DDD

### Etc

* Mobile Native Interfaces
* .well-known - https://www.mnot.net/blog/2010/04/07/well-known

## Diagram

## Contribute

## LICENSE