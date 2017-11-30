---
layout: post
title:  "코코아팟츠에 자신의 라이브러리 등록하기"
date:   2017-10-18 21:00:00 +0900
categories: 
---

## 코코아팟츠에 자신의 라이브러리 등록하기 (Register your own library in CocoaPods )
- 2017년 10월 18일 테스트 진행했던 과정을 정리한 것입니다. (October 18, 2017 This is a summary of the testing process.)


# Good Link
- video : https://www.youtube.com/watch?v=gNMNeqXKnzw
... Thanks!

- link 1 : https://guides.cocoapods.org/making/index.html
- link 2 : https://magi82.github.io/ios-regist-cocoapods/


# Install the latest version of cocoapods
최신 코코아팟츠가 설치는 되어잇을 것이다.. 
안되어 있다면 : sudo gem install cocoapods --pre
헉 베타의 에러도 있으니 : sudo gem install cocoapods

# Go Go!
1. pod lib create 프로젝트명 : Demo Application이 생성된다.
 - http://guides.cocoapods.org/making/using-pod-lib-create.html : 여기를 참고 하라고 알려줌
 - 질문에 답은.. swfit, yes, none, no.. 통상 이리 하게 된다. 처음에 저도 같은 선택을 했음.
2. 그리고 github에 프로젝트를 생성한다.
3. 이후 터미널에서 생성한 레파지토리에 프로젝트를 추가한다.
<pre><code>
…or create a new repository on the command line

echo "# 프로젝트명" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/ClintJang/프로젝트명.git
git push -u origin master
…or push an existing repository from the command line

git remote add origin https://github.com/ClintJang/프로젝트명.git
git push -u origin master

</code></pre>
<pre><code>
.. 실제

3.1. cd 프로젝트명의 폴더
3.2. git remote add origin https://github.com/ClintJang/프로젝트명.git
3.3. git add .
3.4. git commit -m "Create project via pod"
3.5. git push -u origin master
3.6. 잘 올라갔는 지 레파지 토리 확인

</code></pre>
4. 다시 example의 xcode 실행파일로 돌아와서 Podspec Metadata폴더안의 프로젝트명.podspec를 수정한다.

5. pod lib lint 프로젝트명.podspec : 오류가 있는 지 검증한다.
<pre><code>
5.1. pod lib lint --verbose : 과정을 보려면
5.2. pod lib lint --verbose --no-clean : 클린 빌드 하려면
5.3. pod lib lint --allow-warnings : 경고는 무시하려면

5.4. 프로젝트 passed validation : 이 메시지를 봐야된다.
5.4.1. 잘 되었는 지 확인은 다른 프로젝트에서 pod를 추가해 보면 된다.
5.4.2. podfile에 pod '프로젝트명', :path => '경로/경로/프로젝트명'
5.4.3. 해당 콘솔에서 pod install

</code></pre>
6. git status : 반영할 것이 있는 지 확인한다.
<pre><code>
6.1. git add . : 추가
6.2. git status :  녹색 확인
6.3. git commit -m "해당 수정내역"
6.4. git status : 이젠 없을 것임...

</code></pre>
7. git tag 0.1.0 -a 버전 정보를 맞춘다. 
<pre><code>
7.1. 작성할 내용 추가하고 esc :x로 나온다.
7.1.1. 귀찮으면 git tag 0.1.0 : 까지 한다.
7.2. git status 로 상태를 확인한다. push 할 것이 있을 것이다...
7.3. 혹은 그냥 github site에서 release Tap을 찾아서 거기서 직접 작성해서 같은 버전을 추가한다.!!!
7.4. 잘 적용되면 git tag 로 확인 

</code></pre>

8. git push --tags
<pre><code>
8.1.  * [new tag]         0.1.0 -> 0.1.0 메시지를 확인해야된다.

</code></pre>
9. pod trunk register 메일주소 '이름' --description='상세'
<pre><code>
9.1. 반드시 메일에서 가서 웹 링크를 클릭해야됩니다!!!!!!! 그리고 

</code></pre>
10. pod trunk push
<pre><code>
10.1. 경고가 많으시다면... pod trunk push --allow-warnings

</code></pre>
아래의 메시지를 보시면 성공!!! (If you see the message below, you will succeed !!!)
 🎉  Congrats

 🚀  프로젝트명("Project Name") (0.1.0) successfully published
 📅  October 18th, 15:34
 🌎  https://cocoapods.org/pods/프로젝트명("Project Name")
 👍  Tell your friends!
 
 
 # end
 - Fun day!
