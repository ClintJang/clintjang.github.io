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


# jekyll 자주 사용하는 명령어
> 자주 사용하는 명령어를 메모해 봅니다.

- ./_site 에 현재 폴더의 내용으로 사이트를 생성합니다
```
> jekyll build
```

- 수동은 귀찮으니... 이걸 실행시켜 놓고 수정하죠. 
- ./_site 에 현재 폴더의 내용으로 사이트를 생성하고, 변경사항을 감지하면 자동으로 다시 생성합니다.
```
> jekyll build --watch
```

- 개발용 서버가 http://localhost:4000/ 에서 구동됩니다
```
> jekyll serve
```

> 이렇게 로컬에 띄워놓고 만지작 만지막 소스를 조금씩 수정해 보고 있습니다. 

# jekyll 에 GA를 적용할 수 있습니다. 
> 구글 통계를 적용해서 몇번 사람들이 들어오긴 하는 구나 .. 라는 통계를 볼 수 있죠.. 셋팅한지 시간이 지나서.. 링크보고 해서 쉽게 했던 기억이 있습니다.

- 링크 1 : https://rextarx.github.io/jekyll/2017/02/03/Applying_Google_Analytics_to_a_blog_using_Jekyll/
- 링크 2 : http://hochulshin.com/google-analytics-jekyll-theme/
- 링크 3 : http://loustler.io/etc/github_pages_blog_google_analytics/

# jekyll 에 theme
> 제길의 테마를 바꿔야 하나 고민하고 있습니다. 

- http://jekyllthemes.org/ : 아직 고민중입니다. 시간될 때 조금씩 찾아보고 바꾸는 방법을 익혀 볼까 합니다. (아직)