---
keywords: Device-graph;수명 종료
title: 장치 그래프
description: Device Graph의 서비스 종료 계획에 대해 알아봅니다.
source-git-commit: 9b3106c730542e531bab4d0f9851b0aeac0553a2
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 2%

---

# Device Graph 사용 종료

>[!WARNING]
>
>**2025년 12월 31일**&#x200B;부터 교차 장치 분석 내의 Device Graph를 더 이상 사용할 수 없습니다. 현재 Device Graph 사용 가상 보고서 세트를 [필드 기반 메서드](https://experienceleague.adobe.com/ko/docs/analytics/components/cda/field-based-stitching)&#x200B;(으)로 전환하십시오.

교차 디바이스 분석은 개인 그래프를 사용하여 데이터를 함께 결합했습니다. 개인 그래프는 조직에 고유한 해시된 장치 ID의 저장소입니다. CDA는 Device Graph와 정기적으로 통신하여 장치들을 함께 연결합니다.

## Device Graph별 사전 요구 사항

Device Graph 방법을 사용하여 크로스 디바이스 분석을 구현하려는 경우 다음 조건을 충족해야 합니다.

>[!WARNING]
>
>모든 전제 조건을 충족하지 못하면 Cross-Device Analytics를 사용할 수 없거나 데이터 결합이 제대로 되지 않을 수 있습니다.

* 조직은 [Adobe Experience Platform ID 서비스 개인 그래프](https://business.adobe.com/kr/products/experience-platform/identity-service.html)를 사용해야 합니다. ID 서비스 사용 안내서의 [홈 페이지](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=ko)도 참조하세요.
* 구현은 최신 버전의 Experience Cloud ID 서비스(ECID)를 사용해야 합니다. ID 서비스 사용 안내서에서 [홈 페이지](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ko)를 참조하세요. Adobe Experience Platform에서 [태그](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=ko)를 사용하는 대부분의 구현에 이미 ID 서비스가 배포되어 있을 수 있습니다.
* 구현은 사용자가 로그인하거나 이메일을 여는 경우와 같이 개인을 식별할 수 있을 때마다 `setCustomerIDs` 함수(또는 그에 상응하는 SDK 함수)를 호출해야 합니다. 이 요구 사항은 모바일 앱(사용하는 경우)을 비롯한 모든 플랫폼에 적용됩니다. ID 서비스 사용 안내서에서 [`setCustomerIDs`](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/methods/setcustomerids.html?lang=ko)을(를) 참조하십시오.

## Device Graph에 관련된 제한 사항

* 기존 Analytics ID는 지원되지 않습니다. Experience Cloud ID가 있는 방문자만 결합됩니다.
* 조직에서 개인 그래프를 사용하는 경우 새 장치를 결합하는 데 최대 24시간이 걸립니다.
* 타사 장치 그래프는 지원되지 않습니다.

