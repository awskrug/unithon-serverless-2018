# 워크샵 정리 가이드(리소스 삭제)

이 페이지는 이전 모듈에서 작성된 자원을 정리하는 지시 사항을 제공합니다.

## 리소스 정리 지침

### 1. 모듈 4 정리방법
모듈 4에서 작성된 REST API 를 삭제하십시오. Amazon API Gateway 콘솔에서 API를 선택할 때 **Actions** 드롭 다운 메뉴에 **Delete API** 옵션이 있습니다.

<details>
<summary><strong>단계별 지침 (자세한 내용을 보려면 펼쳐주세요)</strong></summary><p>

1. AWS Management 콘솔에서, **서비스** 를 클릭한 다음 Application Services 에서 **API Gateway** 를 선택하십시오.

1. 모듈 4에서 작성한 API 를 선택하십시오.

1. **작업** 드롭 다운 메뉴를 펼쳐서 **API 삭제** 를 선택하십시오.

1. 메시지가 표시되면 API 이름을 입력하고 **API 삭제** 를 선택하십시오.

</p></details>


### 2. 모듈 3 정리방법
모듈 3에서 작성한 AWS Lambda 함수, IAM 역할 및 Amazon DynamoDB 테이블 삭제

<details>
<summary><strong>단계별 지침 (자세한 내용을 보려면 펼쳐주세요)</strong></summary><p>

#### Lambda Function

1. AWS Management 콘솔에서, **서비스** 를 클릭한 다음 Compute 에서 **Lambda** 를 선택하십시오.

1. 모듈 3 에서 만든 `RequestUnicorn` 함수를 선택하십시오.

1. **작업** 드롭 다운 메뉴에서, **삭제** 을 선택하십시오.

1. 확인 메시지가 나타나면 **삭제** 를 선택하십시오.

#### IAM Role

1. AWS Management 콘솔에서, **서비스** 를 클릭한 다음 Security, Identity & Compliance 에서 **IAM** 을 선택하십시오.

1. 네비게이션 메뉴에서 **역할** 을 선택하십시오.

1. `WildRydesLambda` 를 필터 입력칸에 넣으십시오.

1. 모듈 3에서 작성한 역할(role)을 선택하십시오.

1. 오른쪽 상단의 **역할 삭제** 를 선택하십시오.

1. 확인 메시지가 나타나면 **예, 삭제** 를 선택하십시오.

#### DynamoDB 테이블

1. AWS Management 콘솔에서 **서비스** 를 클릭한 다음 Databases 에서 **DynamoDB** 를 선택하십시오.

1. 네비게이션 메뉴에서 **테이블** 를 선택하십시오.

1. 모듈 3 에서 생성한 **Rides** 테이블을 선택하십시오.

1. **테이블 삭제** 를 선택하십시오.

1. **이 테이블에 대한 모든 CloudWatch 알람 삭제** 체크박스를 선택한 뒤에 **삭제** 를 선택하십시오.

</p></details>

### 3. 모듈 2 정리방법
제공된 AWS CloudFormation 템플릿을 사용해서 모듈 2를 완성한 경우, AWS CloudFormation 콘솔을 사용해서 스택을 삭제하기만 하면 됩니다. 그렇지 않다면, 모듈 2 에서 생성한 Amazon Cognito 사용자 풀을 삭제하십시오.

<details>
<summary><strong>단계별 지침 (자세한 내용을 보려면 펼쳐주세요)</strong></summary><p>

1. AWS Management 콘솔에서 **서비스** 를 클릭한 다음 Mobile Services 에서 **Cognito** 를 선택하십시오.

1. **사용자 풀 관리** 를 선택하십시오.

1. 모듈 2 에서 만든 **WildRydes** 를 선택합니다.

1. 페이지 오른쪽 위 모서리에 있는 **풀 삭제** 를 선택하십시오.

1. `delete` 를 입력하고 확인 메시지가 나타나면 **풀 삭제** 를 선택하십시오.

</p></details>

### 4. 모듈 1 정리방법

<details>
<summary><strong>단계별 지침 (자세한 내용을 보려면 펼쳐주세요)</strong></summary><p>

1. AWS Management 콘솔에서 **서비스** 를 선택한 다음 Storage스에서 **S3** 를 선택하십시오.

1. 모듈 1 에서 작성한 버킷을 선택하십시오.

1. **버킷 삭제** 을 선택하십시오.

1. 확인 메시지가 나타나면 버킷의 이름을 입력하고 확인(confirm)을 선택하십시오.

</p></details>


### 5. CloudWatch Logs

<details>
<summary><strong>단계별 지침 (자세한 내용을 보려면 펼쳐주세요)</strong></summary><p>

1. AWS Management 콘솔 에서 **서비스** 를 클릭한 다음 **관리 도구** 에서 **CloudWatch** 를 선택하십시오.

1. 네비게이션 메뉴에서 **Logs** 를 선택하십시오.

1. **/aws/lambda/RequestUnicorn** 로그 그룹을 선택하십시오. 만약 계정에 로그 그룹이 여러개 있는 경우, 로그 그룹을 쉽게 찾으려면 **Filter** 입력칸에 `/aws/lambda/RequestUnicorn` 를 입력하면 됩니다.

1. **작업** 드롭 다운 메뉴에서 **로그 그룹 삭제** 를 선택하십시오.

1. 확인 메시지가 나타나면 **예, 삭제** 를 선택하십시오.

</p></details>
