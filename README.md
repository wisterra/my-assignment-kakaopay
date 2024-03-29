# project for kakaopay

다음과 같은 내용을 고려하여 제작하였습니다.


### 모션구현
scrollmagic과 css3 animation 으로 구현했습니다.


### 맥락을 고려하는 마크업
스크린 리더로 읽거나 css를 불러올 수 없는 상황에서도 전체적인 내용 흐름을 파악을 하는데에 무리없도록 대응하였습니다.


### 비율확장 방식으로 디바이스 대응
모바일 작은 화면을 고려하여 화면을 채우는 방식은 viewport 설정의 두가지 방법으로 나눌 수 있습니다.

1. width=640px
2. width=device-width

**이번 제작에는 2번 방식으로 구현해보았습니다.**

*__1번 방식 width=640px__*
* 장점: 고정픽셀을 사용할 수 있고 빠르게 제작할 수 있습니다.
* 단점: input 등의 입력요소를 클릭하는 경우 화면이 확장될 수 있습니다. (입력 화면 지원을 위해 원래 사이즈로 돌아가는 현상)

*__2번 방식 device-width__*
* 주로 텍스트 비중이 높은 반응형 사이트에서 많이 활용합니다.
* 장점: 1번방식의 단점이 발생하지 않으며, 화면 모든 요소를 비율확장 방식으로 제공할 수 있습니다.
* 단점: 작업시간이 오래걸리고 코드가 복잡합니다.


### 성능 최적화
image 압축, css minified 처리
scss 마지막 세미콜론 제거
웹 진단 도구를 통한 성능 확인 (PageSpeed Insights <https://developers.google.com/speed/pagespeed/insights/?url=https%3A%2F%2Fwisterra.github.io%2Fkakaopay-project%2Fpage%2Fremittance%2Findex.html&tab=mobile> 테스트 사이트에서 구동성능 99% 확인)


### 파일 디렉토리 구조 고려
전체적인 폴더 구조를 실제 사이트에 들어갈때의 구조를 염두해 두고 공통 폴더와 이벤트용 폴더로 구획하였습니다.
scss 폴더에서도 재사용 가능성이 있는 요소들은 컴포넌트화 하였습니다.

