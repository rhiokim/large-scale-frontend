# Vritual DOM

## Prologue

자바스크립트 애플리케이션 패턴도 이제 꽤 큰 이야기꺼리가 되어가고 있다. 그만큼 많은 발전과 기록을 남겨왔다.

Dynamic Web Application 을 만들기 위해 DOM Manipulation 을 직접하고 W3C DOM Specification 을
인쇄해 볼때가 2007년 이였다.

Prototype.js, Script.aculo.us 그리고 jQuery 를 1세대라고 하면 Backbone, Knockout 과 같은
MVC, MVVM 과 같이 당시 소프트웨어 공학에서 먼저 발전한 언어들의 이상적인 애플리케이션 디자인 패턴들이
자바스크립트 애플리케이션 개발에도 그대로 계승되고 있었다.

이를 계기로 비동기 이벤트와 데이터를 이상적으로 분리하고 다루는 방법들을 포함 SPA(Single Page Application)
개발 시 마주치는 여러가지 문제를 해결하기 위한 방법들이 관심을 받게 되었다.

이 시작은 2010 년으로 구글에서도 Angular 1.x 를 출시하면서 DI(Dependency Injection), Directive 가
포함되면서 복잡도 높은 웹 애플리케이션 구축을 도와주고 있었다.

물론 2013년 Facebook 에서 React 를 출시하고 얼마 지나지 않은 시간까지...

(중략)

* React 탄생 배경
* 모던 SPA Framework, Libs 의 특징

여기서 다루고 싶은 이야기는 사실 모던 라이브러리들이 해결하고자 하는 복잡한 웹 애플리케이션의 다양한 문제점 중
상태 관리와 프리젠테이션 영역의 알고리즘에 대해서이다.

그중 특히 실무에서는 깊게 다룰일이 없는 DOM Manipulation 즉 Virtual DOM 에 대해서이다.

Virtual DOM 의 기본은 Compile 기술의 흐름과 거의 비슷하고 모던 자바스크립트가 다양한 문제를 해결하는
근본적인 방식에서도 살펴볼 수 있다.

Babel, Typescript 가 대표적인 예이다. DOM 을 다루지는 않지만 이들은 Virtual Syntax Tree 를 DOM
처럼 다룬다고 보면된다. (약간 다를 수 있어서 부연설명을 해야하는데 여기서는 귀찮다.)

아래의 링크들은 Virtual DOM 에서 가장 핵심 알고리즘인 DOM Element, Object Diff 그리고 변경점을
반영하기 위한 Patch Operation 에 대한 고민과 해법에 대해서 깊에 이해할 수 있는 내용들이다.

## A Virtual DOM and diffing algorithm

A JavaScript DOM model supporting element creation, diff computation and patch operations for efficient re-rendering

* https://github.com/Matt-Esch/virtual-dom

## Virtual DOM and diffing algorithm

* https://gist.github.com/Raynos/8414846

## React's diff algorithm

* https://calendar.perfplanet.com/2013/diff/

## How Virtual-DOM and diffing works in React

* https://medium.com/@gethylgeorge/how-virtual-dom-and-diffing-works-in-react-6fc805f9f84e

## ETC

늘 마크다운 엔진도 Virtual DOM 이 다뤘던 알고리즘에 대한 니즈가 강하게 요구되고 성능에서도 기대할 수
있는 것들이 많은데, 여기서는 다룰 내용이 아니여서 그냥 여기까지...