---
title: Adobe Analytics 1.4 API 서비스 종료
description: Adobe Analytics 1.4 API 및 WSSE 인증은 2026년 8월 31일에 사용이 종료되었습니다. 영향을 받는 항목과 Analytics 2.0 API로 마이그레이션하는 방법에 대해 알아봅니다.
source-git-commit: 4056ba0953e81a279d25b15449c7b41a4a5eb7f9
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 1%
---
# Adobe Analytics 1.4 API 서비스 종료

**2026년 8월 31일**&#x200B;부터 Adobe은 Adobe Analytics 1.4 API 및 WSSE 인증을 중단했습니다. 이 버전의 API를 사용하는 모든 끝점에 더 이상 액세스할 수 없으며, 이에 빌드된 통합이 작동하지 않습니다.

Adobe Analytics 1.4 API는 보고, 분류, 데이터 피드, 세그먼트, 계산된 지표, 데이터 소스 및 보고서 세트 구성과 같은 광범위한 작업을 제공했습니다. 이 API는 세그먼트 및 계산된 지표와 같은 구성 요소 보고 및 관리를 포함하여 Adobe Analytics 사용자 인터페이스에서 사용할 수 있는 거의 모든 작업을 수행할 수 있는 [Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0)&#x200B;(으)로 대체되었습니다. 아직 업그레이드해야 하는 통합이 있는 경우 [Adobe Analytics 2.0 API로 마이그레이션](https://developer.adobe.com/analytics-apis/docs/2.0/guides/migration)에 대한 안내서를 따르십시오.

## 서비스 종료에 도달한 사항

이러한 서비스 종료는 다음 1.4 API 기능에 직접적인 영향을 줍니다. 영향을 받는 각 워크플로우를 [Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0)&#x200B;(으)로 마이그레이션:

* 보고(Data Warehouse, 실시간, 경로 지정 및 요약 보고서 포함)
* 보고서 세트 구성 및 관리
* 분류
* 세그먼트
* 계산된 지표
* 데이터 소스
* 데이터 피드
* 책갈피 및 회사(엔드포인트) 메서드

또한 **Adobe Analytics WSSE 인증**&#x200B;을 삭제합니다(아래 [WSSE 인증](#wsse-authentication) 참조).

>[!IMPORTANT]
>
>이 서비스 종료는 데이터 수집에 영향을 주지 *않습니다*. 태그(이전의 Adobe Launch), 웹 SDK 및 AppMeasurement과 같은 태그 지정 솔루션은 영향을 받지 않습니다. [데이터 삽입 API](#data-insertion-api)도 *사용되지 않음*&#x200B;됩니다. 그러나 1.4 데이터 소스 또는 분류 API를 사용하여 데이터를 향상시키는 경우 이러한 워크플로우를 Adobe Analytics 2.0 API로 마이그레이션해야 합니다.

## WSSE 인증

WSSE 인증은 Analytics 1.4 API에서 지원되는 레거시 인증 프로토콜입니다. [Adobe Developer Console](https://developer.adobe.com/console/home)에 제공된 OAuth 기반 인증 옵션으로 대체되었습니다. WSSE 인증을 사용한 프로젝트는 Adobe Developer Console에서 프로비저닝된 것으로 자격 증명을 업데이트해야 합니다.

마이그레이션하려면 [Adobe Developer Console](https://developer.adobe.com/console/home)에 로그인하고 Analytics 2.0 API 통합을 위한 프로젝트를 만드십시오. **OAuth 사용자** 또는 **OAuth 서버 간** 인증 방법을 선택하십시오.

## 데이터 삽입 API

데이터 삽입 API가 이 서비스 종료의 **not** 부분입니다. 이 설명서는 다른 서버측 수집 방법과 함께 [Adobe Analytics 데이터 수집 API](https://developer.adobe.com/analytics-collection-apis/) 사이트로 이동되었습니다.

* [데이터 삽입 API](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/): 한 번에 하나의 히트에 해당하는 이벤트 데이터를 쿼리 문자열(이미지 요청) 또는 XML `POST`(으)로 보냅니다.
* [대량 데이터 삽입 API](https://developer.adobe.com/analytics-collection-apis/methods/bulk-data-insertion/): 서버 호출 데이터의 배치를 파일로 업로드합니다. Adobe에서는 새로운 서버측 구현에 Bulk Data Insertion API를 사용하는 것이 좋습니다.

## 자주 묻는 질문

+++이 경우 Analytics API에 대한 기존 Adobe Developer 프로젝트에 영향을 줍니까?

Analytics 1.4 API를 사용하는 모든 기존 프로젝트가 영향을 받습니다. 이러한 통합은 [Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0/)&#x200B;(으)로 마이그레이션해야 합니다.

+++

+++Analytics API를 사용하는 다른 제품 또는 애플리케이션과 Adobe 자격 증명을 공유했습니다. 영향을 받습니까?

해당 제품 또는 애플리케이션이 WSSE 자격 증명을 사용하거나 Analytics 1.4 API를 호출하는 경우 영향을 받으며 마이그레이션해야 합니다. 마이그레이션 계획 및 타임라인에 대한 자세한 내용은 제품 또는 애플리케이션 공급업체에 문의하십시오.

+++

+++내 프로젝트에서 사용하는 API는 어떻게 확인할 수 있습니까?

프로젝트가 호출하는 기본 URL은 사용하는 API 버전을 결정합니다. Adobe Analytics 1.4 API는 다음 기본 URL을 사용했습니다.

* `https://api.omniture.com`
* `https://api3.omniture.com`
* `https://api4.omniture.com`
* `https://api5.omniture.com`

[Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0/)에서는 다음 기본 URL을 사용합니다.

* `https://analytics.adobe.io`

API 프로젝트가 `api*.omniture.com`을(를) 호출하는 경우, 중단된 Adobe Analytics 1.4 API를 사용하고 2.0 API로 마이그레이션해야 합니다.

+++

+++이러한 서비스 종료가 데이터 수집에 영향을 줍니까?

아니요. 이 서비스 종료는 Tags, Web SDK, AppMeasurement 또는 Data Insertion API와 같은 직접 데이터 수집에는 영향을 주지 **않습니다**. 그러나 1.4 데이터 소스 또는 분류 API를 사용하여 데이터를 향상시키는 경우 이러한 워크플로우를 Adobe Analytics 2.0 API로 마이그레이션해야 합니다.

+++

이 서비스 종료에 대해 이 페이지에서 답변하지 않은 추가 질문이 있는 경우 Adobe 계정 팀에 문의하십시오.
