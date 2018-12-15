## 요약

주요한 성능 개선만 적용하더라도 가시적인 성능 향상(렌도링 속도, 초기 페이지 표시 시점 등)이 보임
Lighthouse 를 통해 성능 향상에 대한 기준과 가이드가 동시에 제공되어 퍼포먼스 향상을 위한 활동을 하는데 용이함

## 추가

Webpack 번들링을 통해 Gzip Compression 을 할 경우 NginX 에서 Double Gzip Compression 이 발생하지 않게 하기 위해서 gzip_min_length 설정을 4MB 로 설정함
코드 스플리팅을 적용해서 초기 페이지 용량 -61KB / -18KB(gzip)

## 주의사항

T&A, 내예약 의 경우에는 기본 Service Worker 가 캐시 컨트롤이 우선 시 되기 때문에 index.html 과 service-worker.js 파일은 NginX 에서 no-cache 가 적용되어야 한다.

## 확인이 필요한 사항

NginX Gzip Compression Configuration with Webpack Gzip Compression : 웹 팩에서 Gzip 압축을 미리 선행하더라도 NginX 에서 gzip_* 설정들을 별도로 해주지 않으면 웹팩에서 미리 생성해 놓은 *.js.gz 파일을 서빙하지 않습니다.

더불어 확인되지 않은 사항은 만약 설정이 잘못되어 이미 웹팩 번들링 과정에서 생성해 놓은 *.js.gz 파일을 NginX 설정에 의해서 다시 한번 생성하는 과정이 생길 수 있다.

T&A, 내예약 서비스는 기본적으로 서비스 워커에 의해 캐시 컨트롤이 되고 있으나 iOS 는 11.3 부터 Service Worker 를 지원하기 때문에 그 이하 버젼에서는 NginX 에서 캐시 컨트롤이 되어야 한다.

1.png

주요작업 없음

3.png

* 이미지 클라우드너리 적용
* 번들링 의존성 최소화
* 이미지 레이지로딩

5.png

* webpack gzip compression
* rendering block 요소 제거

6.png

* Gzip 적용
* Nginx 캐시 컨트롤(정적 assets 캐시)
* Accessibility 향상

7.png

* Gzip 미적용 CSS

8.png

* JS, CSS 모두 NginX 캐시 적용
