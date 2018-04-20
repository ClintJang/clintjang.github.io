---
layout: post
title:  "iOS SwiftGen 라이브러리 사용 방법"
date:   2018-04-09 12:12:12 +0900
categories: 
---

# [SwiftGen 셈플 소스 링크](https://github.com/ClintJang/sample-swiftgen) 
- 상세한 내용은 [여기 링크](https://github.com/ClintJang/sample-swiftgen)를 클릭하세요. 

# SwiftGen 이란?

> SwiftGen은 코드를 자동으로 만들어줍니다.!! 한번 익히면 편리해요~
- [SwiftGen](https://github.com/SwiftGen/SwiftGen) : 어떻게 사용하는 것일까요? 라이브러리 링크는 클릭하시면 됩니다.
- SwiftGen은 auto-generate 됩니다. 우리의 소스를 안전한 유형으로 자동으로 변경해 주어서 작업 노가다?를 줄이면서 타입의 안정성을 보장해 주는 도구입니다.
 
# 개발하기에 앞서서 버전을 확인해보았습니다.
| 버전 정보를 보니 특별한 것이 있습니다. 하나의 라이브러리에 3가지 라이브러리 정보가 표시가 되네요. !!!
<pre><code>
$ swiftgen --version
  SwiftGen v5.2.1 (Stencil v0.9.0, StencilSwiftKit v2.3.0, SwiftGenKit v2.1.1)
</code></pre>
- [Stencil](https://stenciljs.com/) : 스텐실은.. magical!, reusable!! 이라하네요. 매직컬하게 재사용이 가능한 웹 컴퍼넌트 컴파일러라고 합니다.
- [StencilSwiftKit](https://github.com/SwiftGen/StencilSwiftKit) : Swift 코드 생성 전용 스텐실 노드와 필터들을 추가로 가져 오는 프레임 워크입니다.
- [SwiftGenKit](https://github.com/SwiftGen/SwiftGenKit) : SwiftGen의 프레임 워크로 다양한 리소스를 분석해서 스텐실 컨텍스트로 변환합니다.
	- 이 저장소는 기본 SwiftGen 저장소에 병합되었다고 합니다.

# 설치 방법은?
[link](https://github.com/SwiftGen/SwiftGen)를 클릭해서 "Install"부분을 하세요. 간단하게는 아래의 내용대로 하시면 됩니다.
<pre><code>
ex) 
install

$ brew update
$ brew install swiftgen

confirm
$ swiftgen ...
</code></pre>

# 이해는 뭐니뭐니해도 셈플이지요~
> 위에 셈플 링크를 눌러서 이동하시면.. 다양한 테스트 케이스를 보실 수 있습니다.
- String(Localization), font, color, asset, storyboard 에 대하여 여러가지로 만들어본 테스트 케이스를 보실 수 있습니다. 


# 결론적인 생각
> 현재 외국이나 앞서가는 개발업체들은 SwiftGen을 이용해서 개발 효율을 높이고 있는 것 같습니다. 한번 사용해 보시면 어떨까요?

> 만약 빌드때 느리다면, 빌드시점에서 사용하지 않고, 수정이 있을 때, 별도로 쉘에서 스크립트 명령어로 실행하는 식으로 관리할 수도 있습니다. 어짜피 자산 파일들은 자주 변경되는 부분은 아니니깐요.

- [iOSSampleApp](https://github.com/igorkulman/iOSSampleApp) 이런 식으로 하나의 프로젝트 단위 패키지가 가능합니다.
