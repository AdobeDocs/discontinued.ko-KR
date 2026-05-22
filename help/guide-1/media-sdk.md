---
title: Adobe Media SDK(버전 1.x 및 2.x) 사용 종료 FAQ
description: Adobe Media SDK 버전 1.x 및 2.x(이전 비디오 하트비트 라이브러리)의 서비스 종료에 대해 자주 묻는 질문에 대한 답변을 얻으십시오.
source-git-commit: d014c200dd926ccf0116faa50c4bffb1d234e926
workflow-type: tm+mt
source-wordcount: '1046'
ht-degree: 0%

---


# Adobe Media SDK(버전 1.x 및 2.x) 사용 종료 FAQ

Adobe Media SDK **2.x는 2021년 8월 31일**&#x200B;에 지원이 종료되었습니다. VHL(비디오 하트비트 라이브러리) **1.x는 더 이상 사용되지 않습니다**. 몇 년 동안 지원되지 않습니다.

## 현재 상황

나중에 Media SDK으로 이름이 변경된 원래 비디오 하트비트 라이브러리(VHL)는 오디오 및 비디오 분석에 대한 클라이언트측 추적을 제공했습니다. Adobe은 추적 기능을 보다 새롭고 더 강력한 구현으로 전환했습니다.

* **Media SDK 3.x(Analytics 전용):**&#x200B;이(가) 현재 지원됩니다. 미디어 컬렉션 API를 사용하여 미디어를 추적합니다. 아직 Edge Network으로 이동할 수 없는 기존 2.x 사용자에게 권장됩니다.
* **Edge Network용 Streaming Media(권장):** 현재 권장 구현입니다. Adobe Experience Platform Web SDK, Mobile SDK 또는 Media Edge API를 사용하여 Edge Network을 통해 미디어 데이터를 보내므로 Adobe Analytics, Customer Journey Analytics, Real-Time CDP 및 Adobe Journey Optimizer에서 사용할 수 있습니다.

## 서비스 종료에 포함되는 항목은 무엇이며 포함되지 않는 항목은 무엇입니까?

**서비스 종료(더 이상 지원되지 않음):**

* 비디오 하트비트 라이브러리(VHL) 1.x — 모든 플랫폼(Android, iOS, JavaScript, Apple TV, Chromecast, Roku, TVML)
* Media SDK 2.x — Android, iOS, JavaScript

**수명이 종료되지 않음(계속 지원됨):**

* Media SDK 3.x — JavaScript, Chromecast, Roku(Analytics 전용)
* Edge Network용 스트리밍 미디어 - 지원되는 모든 플랫폼

## 버전 1.x 및 2.x가 사용되지 않는 이유는 무엇입니까?

버전 3.0부터 Media SDK은 Media Collection API를 직접 사용하도록 재설계되어 위임 패턴이 필요하지 않고 추적기 생성을 단순화했습니다. 이전 1.x 및 2.x SDK는 이후 교체된 하트비트 서버 아키텍처에 의존했습니다.

Adobe은 또한 기존 하트비트 SDK에서 지원하지 못했던 여러 다운스트림 Adobe 애플리케이션을 제공할 수 있는 단일 데이터 수집 파이프라인을 제공하기 위해 Edge Network 구현을 도입했습니다.

## 보관된 설명서는 어디에서 찾을 수 있습니까?

레거시 설명서는 GitHub에 보관되었으며 참조할 수 있습니다.

| 버전 | 상태 | 보관된 설명서 |
|---|---|---|
| 1.x (비디오 하트비트 라이브러리) | 사용되지 않음 | [`video-heartbeat` GitHub 저장소](https://github.com/Adobe-Marketing-Cloud/video-heartbeat/tree/master/docs) |
| 2.x (Media SDK) | 2021년 8월 31일 지원 종료 | [`media-sdks` GitHub 저장소](https://github.com/Adobe-Marketing-Cloud/media-sdks/blob/master/docs/2.x/README.md) |

## 전환 선택 사항은 무엇입니까?

**옵션 1: Media SDK 3.x(Analytics 전용)로 마이그레이션**

2.x를 사용하고 Adobe Analytics만 사용하는 경우 3.x로 마이그레이션하는 것이 가장 간단한 경로입니다. 전체 API 비교 및 코드 예는 [2.x에서 3.x로 마이그레이션 안내서](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/media-sdk/setup/migrate-js-2x-to-3x.html)를 참조하십시오.

**옵션 2: Edge Network용 Streaming Media로 마이그레이션(권장)**

새로운 구현의 경우 또는 여러 Adobe 애플리케이션에서 데이터를 사용하려는 경우 Adobe Experience Platform Edge Network을 사용하십시오.

* [Media Edge 웹 SDK](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/edge-web-sdk.html)
* [Media Edge Mobile SDK](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/edge-mobile-sdk.html)
* [Media Edge API](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/implementation-edge-api.html)

## FAQ

+++**Roku 및 Chromecast SDK에 대한 지원이 영향을 받습니까?**

아니요. Roku 및 Chromecast SDK는 Media SDK 3.x(Analytics 전용)의 일부로 계속 사용 및 지원됩니다. 이 수명 종료에는 1.x 및 2.x 버전만 포함됩니다.

+++

+++**Media Analytics JavaScript SDK 구현이 영향을 받습니까?**

아니요. Media Analytics용 JavaScript SDK을 사용하는 고객은 독립형 SDK 또는 태그 확장 프로그램을 계속 사용할 수 있습니다.

+++

+++**아직 Media SDK 2.x에 있습니다. 어떻게 해야 합니까?**

Adobe은 모든 새 프로젝트에 대해 Edge Network 구현으로 마이그레이션할 것을 권장합니다. 중간 단계가 필요한 경우 [JavaScript SDK 2.x에서 3.x로 마이그레이션](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/media-sdk/setup/migrate-js-2x-to-3x.html)한 다음 Edge Network으로 이동할 계획을 세우십시오.

+++

+++**지원되는 구현으로 마이그레이션하기 위한 작업 수준은 무엇입니까?**

마이그레이션 작업은 각 고객의 구현에 따라 다르며, 상황에 따라 다릅니다. 마이그레이션 설명서를 검토한 후 추가 지원을 받으려면 컨설팅 또는 고객 지원 센터에 문의하십시오.

* [Mobile Edge SDK을 사용하여 Streaming Media 구현 - Android 및 iOS](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/edge-mobile-sdk.html)
* [JavaScript SDK 2.x에서 3.x로 마이그레이션](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/media-sdk/setup/migrate-js-2x-to-3x.html)

+++

+++**Adobe Experience Platform 태그를 태그 관리 시스템으로 사용해야 합니까?**

모바일 앱 구현의 경우, Experience Platform 태그는 웹용 태그 관리 시스템으로 사용되지 않습니다. SDK 확장을 구성하려면 태그 UI가 필요합니다. 이는 Adobe Mobile Services UI를 사용하여 Mobile v4 SDK을 구성하는 방법과 유사합니다. 태그는 사용자가 선택한 확장에 따라 사용자 지정된 설치 지침을 제공합니다.

+++

+++**이러한 지원이 tvOS용 SDK에 영향을 줍니까?**

예. tvOS(버전 10+)의 경우 권장되는 구현은 Adobe Experience Platform Mobile SDK을 사용하여 Edge Network용 스트리밍 미디어로 마이그레이션하는 것입니다. 자세한 내용은 [모바일 Edge SDK을 사용하여 스트리밍 미디어 구현](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/edge-mobile-sdk.html)을 참조하십시오.

+++

+++**이러한 지원이 Fire TV 및 Android TV용 SDK에 영향을 줍니까?**

예. Fire TV 및 Android TV의 경우 권장되는 구현은 Adobe Experience Platform Mobile SDK을 사용하여 Edge Network용 스트리밍 미디어로 마이그레이션하는 것입니다. 자세한 내용은 [모바일 Edge SDK을 사용하여 스트리밍 미디어 구현](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/edge-mobile-sdk.html)을 참조하십시오.

+++

+++**Mobile v4 SDK 서비스 종료 정보는 어디에서 찾을 수 있습니까?**

[Mobile Services 사용 종료 FAQ](mobile-services.md)를 참조하세요. Mobile Services 플랫폼 및 Mobile v4 SDK는 2022년 12월 31일에 사용이 종료되었습니다.

+++

+++**질문이 있는 경우 어디로 이동할 수 있습니까?**

마이그레이션 지원은 Adobe 계정 팀이나 Adobe 고객 지원 센터에 문의하십시오.

+++

>[!MORELIKETHIS]
>
>* [스트리밍 미디어 구현 개요](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/overview.html?lang=ko)
>* [Edge Network용 스트리밍 미디어](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/implementation-edge.html?lang=ko)
>* [Media SDK 3.x — JavaScript 설정](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/media-sdk/setup/web-implementation.html?lang=ko)
