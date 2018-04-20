# clintjang.github.io
ClintJang Blog

# jekyll window에 셋팅하기
> [제킬](https://jekyllrb-ko.github.io/)은 참 편하게 [github 홈페이지](https://pages.github.com/)를 생성해 주는 것 같습니다. 

Mac에서는 쉽게 제킬로 홈페이지를 만들어서 올릴 수 있는 데, 윈도우즈는 조금 번거롭습니다. 과정을 간략히 메모했습니다. 

## RubyInstallers 사이트를 이용해서 Ruby 와 devkit 설치하기
> https://rubyinstaller.org/downloads/

위 사이트에 들어가서 WITH DEVKIT 를 선택해서 다운로드 합니다.
정확히는 모르겠지만, Ruby gem 을 이용하기 위해서라 이해하고 있습니다. 
- 관련 설치를 가능한한 다 합니다.

설치 과정에 패치 설정을 한다는 체크가 있다는 데, 전 그런 창이 뜨지 않더군요. (막눌렀나 -_ -;;) <br />
그래서 직접 경로 설정을 해주었습니다. <br />
다 아시겠지만...  <br />
내 PC -> 오른쪽버튼 -> 속성 -> 시스템 속성 으로 들어가서 고급에 환경 변수 버튼을 클릭합니다.  <br />
이후에 path를 편집해서 아래의 내용을 추가합니다. <br />

```
C:\Ruby{ 설치폴더명, 버전에 따라 이름이 다름 }\bin
```

## 명령프로롬트 를 실행 
> Windows 검색에서 cmd를 치시면 되죠?

- gem이 동작하는 지 확인합니다. 
```
> gem 
```

- 이제 템플릿을 만들어 봅시다. jekyll을 설치하고
```
> gem install jekyll
```

```
> jekyll new my-awesome-site

or

> jekyll new 원하는명칭
```

- 폴더 안으로 이동해서 
```
> cd my-awesome-site
```

- 그리고 실행
```
> jekyll serve
```

## 추가로
여기서 전 오류가 발생해서 추가로.
- builder 설치
```
> gem install builder
```
- builder install

```
> builder install
```


