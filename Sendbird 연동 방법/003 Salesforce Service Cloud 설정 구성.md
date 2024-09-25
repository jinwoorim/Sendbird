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
