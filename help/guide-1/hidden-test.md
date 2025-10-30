---
title: 숨겨진 테스트
description: 숨겨진 테스트입니다.
hide: true
hidefromtoc: true
landing-page-breadcrumb-title: Test AEM 6.5
landing-page-name: experience-manager-65
feature: Annotations
exl-id: e6e5ba1c-98a5-4d7d-9913-426df31bc7a3
source-git-commit: db7157a0c773bd673ffaf3f8298af1eeb7e2684a
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 4%

---

# 숨겨진 테스트

숨겨진 테스트입니다. v2 렌더링에서 제대로 작동하는지 확인하기 위해 이 `[`을(를) 추가합니다.

Bob은 스프린트 데모를 위해 이곳에 있었고, Lakshay가 프로덕션으로 무대를 옮긴 후에 다시 한번 왔습니다.

매트는 여기 있었어요 - 10월 28일

Slack 알림? 30일.

## 잘못된 테이블

**원본**

| 작업 | 설명 |
| -----------| ---------- |  
| [Analytics용 Experience Cloud ID 서비스 구현](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-analytics.html?lang=ko) | 또한 Adobe에서는 추가 [고객 ID](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html?lang=ko)을(를) 설정하는 것이 좋습니다. 이러한 ID는 각 방문자와 연결되며 Experience Cloud의 현재 및 향후 기능을 활성화합니다. |
| 기존 `s_code`을(를) 버전 H.27.3 이상으로 업데이트하거나 기존 `AppMeasurement.js`을(를) 버전 1.4 이상으로 업데이트합니다. | 이러한 파일은 Analytics 관리 도구의 [코드 관리자](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/code-manager-admin.html?lang=ko)에서 다운로드할 수 있습니다. [에 대한 자세한 정보가 필요한 경우 &#x200B;](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html?lang=ko#js)JavaScript 구현`AppMeasurement.js` 가이드를 사용할 수 있습니다. |

**추가 공백 두 개**

| 작업 | 설명 |
| -----------| ---------- |  
| [Analytics용 Experience Cloud ID 서비스 구현](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-analytics.html?lang=ko) | 또한 Adobe에서는 추가 [고객 ID](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html?lang=ko)을(를) 설정하는 것이 좋습니다. 이러한 ID는 각 방문자와 연결되며 Experience Cloud의 현재 및 향후 기능을 활성화합니다. |
| 기존 `s_code`을(를) 버전 H.27.3 이상으로 업데이트하거나 기존 `AppMeasurement.js`을(를) 버전 1.4 이상으로 업데이트합니다. | 이러한 파일은 Analytics 관리 도구의 [코드 관리자](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/code-manager-admin.html?lang=ko)에서 다운로드할 수 있습니다. [에 대한 자세한 정보가 필요한 경우 &#x200B;](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html?lang=ko#js)JavaScript 구현`AppMeasurement.js` 가이드를 사용할 수 있습니다. |

**추가 공백은 있지만 헤더 분할자 이후는 아님**

| 작업 | 설명 |
| -----------| ---------- |
| [Analytics용 Experience Cloud ID 서비스 구현](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-analytics.html?lang=ko) | 또한 Adobe에서는 추가 [고객 ID](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html?lang=ko)을(를) 설정하는 것이 좋습니다. 이러한 ID는 각 방문자와 연결되며 Experience Cloud의 현재 및 향후 기능을 활성화합니다. |
| 기존 `s_code`을(를) 버전 H.27.3 이상으로 업데이트하거나 기존 `AppMeasurement.js`을(를) 버전 1.4 이상으로 업데이트합니다. | 이러한 파일은 Analytics 관리 도구의 [코드 관리자](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/code-manager-admin.html?lang=ko)에서 다운로드할 수 있습니다. [에 대한 자세한 정보가 필요한 경우 &#x200B;](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html?lang=ko#js)JavaScript 구현`AppMeasurement.js` 가이드를 사용할 수 있습니다. |

## 상대 링크

* [개요](overview.md)
* [Search&amp;Promote](search-promote.md)
* [소셜](social.md)

## 명시적 딥링크

[개요 추가(루트)](/help/guide-1/overview.md#additional-products)

[추가 정보 개요](overview.md#additional-products)

## 가리킨 텍스트 테스트 {#this-is-a-heading-anchor}

가리킨 텍스트 없음

```
![alt text](assets/maui-flip.jpg)
```

![대체 텍스트](assets/maui-flip.jpg)


예 가리키기 텍스트

```
![alt text](assets/maui-flip.jpg "Hover text")
```

![대체 텍스트](assets/maui-flip.jpg "가리킨 텍스트")

## 슬라이드

구문:

```
>[!SLIDE](analyze-project)
https://experienceleague-stage.adobe.com/en/slides/analyze-project
```

렌더링됨:

<!--
>[!SLIDE](analyze-project)
-->

Bob: 주제 위치 항목을 테스트하면 슬라이드 주석을 제거합니다.
