---
title: Adobe Mobile Services 서비스 종료 FAQ
description: Adobe Mobile Services의 서비스 종료 발표와 관련하여 자주 묻는 질문에 대한 답변을 얻으십시오.
exl-id: c5f44341-7b87-4530-b86e-17e2911a7959
source-git-commit: 343e0a727c570c9eec503d7903d0477134fc6189
workflow-type: ht
source-wordcount: '421'
ht-degree: 100%

---

# Adobe Mobile Services 서비스 종료 FAQ

Adobe Mobile Services의 종료일은 **2022년 12월 31일**&#x200B;입니다.

## 현재 상황

Mobile Services는 2022년 12월 31일에 서비스가 종료되었습니다. 모바일 중심 UI, 획득, 딥 링크, 인앱 메시지, 푸시 알림 및 지리적 위치를 지원하는 Mobile Services는 이 날짜 이후에 더 이상 지원되지 않습니다.

## 포함 사항 및 제외 사항

이 서비스 종료에는 [mobilemarketing.adobe.com](https://mobilemarketing.adobe.com)의 독립형 플랫폼인 Adobe Mobile Services만 포함됩니다. 이 인터페이스를 사용하는 Mobile 버전 4 SDK는 2021년 8월 31일에 종료되었습니다.

이 서비스 종료에는 Adobe Experience Platform Mobile SDK의 일부인 모바일 앱용 Adobe Analytics가 포함되지 않습니다. 인앱 동작, 수명 주기 분석, 메시지 상호 작용 추적 및 대상자 프로필을 포함하는 이러한 기능은 Adobe에서 계속 지원됩니다.

## 기능이 만료되는 이유

Adobe가 모바일 마케팅 기능을 계속 확장함에 따라 이전에 Mobile Services에서 사용할 수 있었던 기능은 Adobe Experience Cloud 솔루션에서 출시되거나 Adobe Exchange 프리미어 파트너를 통해 제공됩니다. 이러한 전환을 통해 더욱 강력하고 유연한 모바일 마케팅 기능이 제공될 예정입니다.

## Mobile Services에서 생성된 기존 처리 규칙에 나타나는 결과

Mobile Services UI에서 생성된 [처리 규칙](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/processing-rules/processing-rules.html)은 Mobile Services 서비스 종료일 이전에 Adobe Analytics로 자동 마이그레이션됩니다. 마이그레이션된 Adobe Analytics의 다른 처리 규칙과 유사하게 작동하며 이러한 처리 규칙을 자유롭게 보거나 편집할 수 있습니다. 이 마이그레이션에는 사용자 작업이 필요하지 않습니다.

모바일 서비스가 종료된 후 모든 처리 규칙 논리는 일반적으로 [컨텍스트 데이터 변수](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/contextdata.html?lang=ko-KR) 사용을 포함하여 Adobe Analytics 내에서 독점적으로 처리됩니다.

## 사용할 수 있는 전환 옵션

Adobe는 조직의 사용 사례에 따라 세 가지 전환 경로를 제공합니다.

1. **인앱 메시지 및 푸시 알림**: Adobe는 메시지 워크플로를 Adobe Journey Optimizer로 전환할 수 있습니다. 이 제품을 사용하면 조직이 모바일 메시지를 포함하여 전체 고객 여정에서 경험을 최적화하고 개인화할 수 있습니다.
1. **획득 및 딥 링크**: 획득 및 딥 링크는 Adobe Exchange 프리미어 파트너 프로그램을 통해 제공됩니다. Adobe의 파트너십 팀은 요구 사항에 가장 적합한 솔루션을 찾을 수 있도록 적절한 파트너를 소개할 수 있습니다.
1. **Places Service**: Places Service는 무료 지리적 위치 기능을 제공합니다. [Places Service 설명서](https://experienceleague.adobe.com/docs/places/using/home.html?lang=ko-KR)를 참조하십시오.

## 질문 접수 창구

자세한 내용은 [Adobe Mobile Services 서비스 종료 Spark 페이지](https://spark.adobe.com/page/C6D30y09zaRpD/)를 참조하십시오. 추가적인 문의 사항이 있으면 Adobe 담당자에게 문의하십시오.
