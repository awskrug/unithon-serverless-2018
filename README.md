# 개요
* 본 실습서는 1차번역본인 https://github.com/awskrug/aws-serverless-workshops/tree/master/WebApplication 을 개선한 2차 번역본입니다.(한글화된 콘솔 화면 스크린샷으로 변경, 사용 용어 번역) 
* 원문(영문)을 참조하시려면 https://github.com/awslabs/aws-serverless-workshops 을 참고해 주세요.

1차 번역에 참여해 주신 AWSKRUG 멤버분들에게 감사를 표합니다 :)




# Wildrydes 서버리스 웹 애플리케이션 워크샵
본 워크샵에서는 사용자가 [Wild Rydes](http://www.wildrydes.com/) 서비스를 통해 현재 있는 위치에서 유니콘 호출 및 탑승을 할 수 있는 스타트업 아이디어를 구현한다는 시나리오로 함께 웹 애플리케이션을 만들어 배포해 봅니다. 이 서비스는 사용자에게 HTML 기반 사용자 인터페이스를 제공하여, 사용자가 원하는 위치를 표시하고 유니콘 요청을 하면, 가까운 유니콘을 보내기기 위해 RESTful 웹 서비스로 백엔드를 제공합니다. 또한, 사용자가 유니콘 타기를 요청하기 전에 기본적으로 회원 가입을 하고 로그인 할 수있는 기능을 제공합니다.

응용 프로그램 아키텍처는 [AWS Lambda](https://aws.amazon.com/lambda/), [Amazon API Gateway](https://aws.amazon.com/api-gateway/), [Amazon S3](https://aws.amazon.com/s3/), [Amazon DynamoDB](https://aws.amazon.com/dynamodb/), [Amazon Cognito](https://aws.amazon.com/cognito)를 활용합니다. Amazon S3는 HTML, CSS, JavaScript 및 사용자에게 전달되는 이미지 파일을 비롯한 정적 웹 리소스를 호스팅합니다. 웹 브라우저에서 실행되는 JavaScript는 Lambda 및 API 게이트웨이를 사용하여 작성된 공용 백엔드 API에서 데이터를 보내고받습니다. Amazon Cognito는 백엔드 API를 보호하기 위해 사용자 관리 및 인증 기능을 제공합니다. 마지막으로, DynamoDB는 API의 Lambda 함수로 데이터를 저장할 수 있는 데이터베이스 기능을 제공합니다.

전체 아키텍처의 그림은 아래 다이어그램을 참조하십시오.

![Wild Rydes 웹 애플리케이션 아키텍처](images/wildrydes-complete-architecture.png)

아래 필수 준비를 하고 나서, [Lab 1. 정적 웹 호스팅 설정](1_StaticWebHosting/README-ko.md) 모듈 페이지를 방문하여 워크샵을 시작하십시오.

## 필수 준비
### AWS 계정
본 워크샵을 진행하려면 AWS 기본 계정을 준비해야 합니다. AWS IAM, S3, DynamoDB, Lambda, API Gateway 및 Cognito에 접근할 수 있어야 하며, 본 가이드는 한명이 하나의 AWS 계정을 사용한다고 가정합니다. 다른 사람과 계정을 공유하려고하면 특정 리소스에 대해 충돌이 발생하므로 권장하지 않습니다.

본 워크샵의 일환으로 시작하는 모든 리소스는 AWS 계정이 12개월 미만인 경우, 제공하는 AWS 프리티어로 충분히 가능합니다. 프리티어를 넘어서는 경우, 과금일 될 수도 있습니다. 따라서, 새로운 실습용 계정을 만드시길 권장합니다. 자세한 내용은 [AWS 프리 티어 페이지](https://aws.amazon.com/free/)를 참조하십시오.

### 웹 브라우저
웹 애플리케이션 UI를 테스트 할 때 Chrome 또는 Firefox의 최신 버전을 사용하는 것이 좋습니다.

### 텍스트 에디터
구성 파일을 사소한 업데이트를하기 위해 로컬 텍스트 편집기가 필요합니다.

## 실습 모듈
* [Lab 1. 정적 웹 호스팅 설정](1_StaticWebHosting)
* [Lab 2. 사용자 관리](2_UserManagement)
* [Lab 3. 서버리스 백엔드](3_ServerlessBackend)
* [Lab 4. RESTful APIs](4_RESTfulAPIs)

워크샵을 마친 후에는 [자원 삭제 가이드](9_CleanUp)에 따라 생성 된 모든 리소스를 삭제할 수 있습니다.
