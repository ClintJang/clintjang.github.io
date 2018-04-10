---
layout: post
title:  "iOS ProcessInfo Class 설명 및 셈플소스링크"
date:   2018-04-04 12:12:12 +0900
categories: 
---

# [ProcessInfo 셈플 소스 링크](https://github.com/ClintJang/sample-swift-progressinfo) 
- 상세한 내용은 [여기 링크](https://github.com/ClintJang/sample-swift-progressinfo)를 클릭하세요.

# Apple's ProcessInfo Class
- [ProcessInfo](https://developer.apple.com/documentation/foundation/processinfo) : 프로세스 정보 에이전트는 인수, 환경 변수, 호스트 이름 및 프로세스 이름과 같은 정보를 리턴 할 수 있습니다. processInfo 클래스 메소드는 현재 프로세스 (즉, 객체가 메시지를 보낸 프로세스)에 대한 공유 에이전트를 반환합니다.
- 활용 요소가 많습니다. 활용한다면?
- iOS 2.0+


# Samples 
- 상단의 [셈플 링크](https://github.com/ClintJang/sample-swift-progressinfo)로 이동해 주세요~ 
> 개발 중 빌드를 많이 합니다. 그때마다 내가 원하는 속성의 분기 처리를 코드 레벨에서 변경하는 것도 좋은 방법이지만 아래 셈플과 같은 방법이 있습니다. 

> 오브젝티드 씨에서는 전처리문(컴파일 이전에 미리 처리될 수 있는..)이 있어서 Test URL 분기라던가, 테스트 시에만 보이게 하고 싶은 설정들의 분기가 잘 이용만 하면 편리했는 데, Swift는 그런 부분이 조금 아쉬웠습니다... 
> (active compilation flag.. 등등 기타 유용한 다른 방법도 많이 있습니다.)
>> 셈플 01은 배포(아카이브) 시에는 적용이 안되니 주의하세요~. 테스트에 무척 유용합니다.
>> 셈플 02는 어떤 키와 값들이 있는 지 로그를 찍고 결과 정보를 확인해 보았습니다.

샘플 소스의 테스트 부분
- ViewController.swift
<pre><code>
    @IBOutlet weak var testLabel: UILabel!
    
    override func viewDidLoad() {
        super.viewDidLoad()
        
        // Samples Case 01
        useArgumentsPassedOnLaunch()
        
        // Samples Case 02
        printProcessInfoEnvironmentKeyAndValue()
        
    }
    
    func useArgumentsPassedOnLaunch() {
        // TEST Setting 1
        if ProcessInfo.processInfo.arguments.contains("TEST_SELF_VIEW_BACKGROUND_COLOR") {
            self.view.backgroundColor = #colorLiteral(red: 0.4666666687, green: 0.7647058964, blue: 0.2666666806, alpha: 1)
        }
        
        // TEST Setting 2
        if ProcessInfo.processInfo.arguments.contains("TEST_SELF_LABEL_TEXT") {
            testLabel.text = "TEST"
        }
    }
    
    func printProcessInfoEnvironmentKeyAndValue() {
        // View key and value log
        for (key, value) in ProcessInfo.processInfo.environment {
            print(">>>> \(key): \(value)")
        }
    }
</code></pre>
