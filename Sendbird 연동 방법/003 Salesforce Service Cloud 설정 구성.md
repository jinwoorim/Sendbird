# Salesforce Service Cloud 설정 구성

## 1. Salesforce Service Cloud에서 개체 만들기 ( Sendbird_Setting__c)

- 개체를 만들려면 Sendbird Lightning User 권한이 필요. 

<img src = "https://github.com/user-attachments/assets/4bc54d93-cc54-4cdb-81a7-7dce2b296f6c"/>

- Developer Console에서 Anonymous 창에서 밑에 코드 실행

<img src = "https://github.com/user-attachments/assets/8fe26107-3c0d-4de0-8c53-9f1f2976d25c"/>

``` java

Sendbird__Setting__c setting = new Sendbird__Setting__c(
    Sendbird__ApplicationId__c = 'YOUR_APPLICATION_ID',
    Sendbird__ApiToken__c = 'YOUR_API_TOKEN'
);
insert setting;

```

- 개체가 잘 만들어졌는지 확인 쿼리

```java

SELECT FIELDS(ALL) FROM Sendbird__Setting__c LIMIT 1

```

## 2. 원격 사이트 등록

- 원격 사이트 설정 > 새로만들기
- Remote Site URL에 Sendbird Dashboard에서 Application Id 넣어주기

<img src = "https://github.com/user-attachments/assets/ce8d851f-b7b9-4a9a-ac64-59f21c2b31ec"/>

## 3. 옴니채널 설정

- 설정 > 옴니채널 설정 > 옴니채널 활성화 체크
- 설정 > 서비스 채널 > 새로만들기

<img src = "https://github.com/user-attachments/assets/a6739ad8-521d-4bcd-b4d8-463687aeb864"/>

- 설정 > 현재상태 > 새로만들기

<img src = "https://github.com/user-attachments/assets/1863bbc7-d760-4c0c-894a-32d39bb4d39f"/>

- 설정 > 프로필 > 시스템관리자 > '서비스 현재 상태 액세스가 활성화됨'에 추가

<img src = "https://github.com/user-attachments/assets/5e70d346-f451-4dde-aa38-7f119cb4e492"/>

- 설정 > 라우팅 구성 > 새로만들기

<img src = "https://github.com/user-attachments/assets/34e785b7-f626-47ac-86e4-1b44b37ccdbb"/>

- 설정 > 대기열 > 새로만들기

<img src = "https://github.com/user-attachments/assets/53b4b9d1-4cac-4db0-99a8-c9c4cda148f7"/>

- 설정 > 사례 할당 규칙 > 새로만들기

<img src = "https://github.com/user-attachments/assets/e8ff0e5b-64c5-4acd-9a26-c12a46b69f02"/>

- 설정 > 프로필 > 시스템 관리자 > 활성화된 사용자 정의 권한 > Supervisor Setting 빼기 

## 4. UI 구성 요소 추가

- 설정 > 앱 관리자 > 서비스 콘솔

<img src = "https://github.com/user-attachments/assets/8438d98f-e0dc-46b6-86f6-0113005778ae"/>

- Sendbird Chat Panel 노출

<img src = "https://github.com/user-attachments/assets/9ea5b76c-1970-4aa2-84c5-89f70f2bfa73"/>

