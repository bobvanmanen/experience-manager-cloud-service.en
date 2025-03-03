---
title: Current Maintenance Release Notes of [!DNL Adobe Experience Manager] as a Cloud Service.
description: Current Maintenance Release Notes of [!DNL Adobe Experience Manager] as a Cloud Service.
---

# Maintenance Release Notes {#maintenance-release-notes}

The following section outlines the technical release notes for the current maintenance release of Experience Manager as a Cloud Service.

## Release 11382 {#release-11382}
 
Summarized below are the continuous improvements for maintenance release 11382, which was publicly released on March 28, 2023. This maintenance release is an update from previous maintenance release 11289.

Feature enablement for this maintenance release will provide you with the full feature set. See the [current release notes](/help/release-notes/release-notes-cloud/release-notes-current.md) for full details.

>[!IMPORTANT]
>
> A discrepancy can be noted on the CloudManager UI, showing "2023.3.11382", while the official release is "2023.02". This is due to the delayed activation of the 2023.02 features.
> We are working on fixing this for upcoming releases.

### Known Issues {#known-issues-11382}

- SITES-12573 - GraphQL queries using variables inside of a filter will fail if one variable is not specified. Please do not update to this release shall you use GraphQL with AEM as a Cloud Service.
- SKYOPS-51970 - Identified regression of the FACT version used in the buildImage step, leading to un-matching user mapping.
- GRANITE-44542 - Issues have been reported for customers who did not specify a package nodetype (by providing a .content.xml with jcr:primaryType) for folders included in the package filter. This caused these folders to be treated as nt:folder, creating issues in various cases.
- SKYOPS-56928 - Apache HTTPD regression might cause 404 errors. If you experience those issues, for safety reasons, it is recommended to rollback to the previous version and to avoid any pipeline running during that time period.

### Fixed Issues {#fixed-issues-11382}

- ASSETS-21023 - Fixed Smart Crop rendition, where customers could observe a Null Pointer exception on the Publisher instance of all AEM environments when  tried to access these renditions through the API.
- SKYOPS-49280 - When installing a config or bundle update using RDE into Publish the result may not be observable because the Publish dispatcher cache isn't invalidated

#### Sites {#sites-issues-11382}

- SITES-7796 - Ability for content author to publish the Master Content Fragment and its respective Variations when exporting to target
- SITES-97 - GraphQL: Pagination & Sorting, hybrid filtering

>[!NOTE]
>
> In SITES-97, some improvements have been made in the GraphQL implementation that might cause unexpected behavior. See [AEM GraphQL changes regarding handling of null values](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-21792.html) for more information.

#### Assets {#assets-issues-11382}

- ASSETS-20076 - Add support for video watermarking that matches the current image watermarking support
- ASSETS-21428 - Added exclusions for CSS changes

#### Forms {#forms-issues-11382}

- CQ-4351502 - Updating service user mapping to allow read access in Sites

#### Platform {#platform-issues-11382}

- SITES-11040 - Conditional enablement of GraphQL persisted query caching in dispatcher

### Embedded Technologies {#embedded-tech-11382}

|Technology|Version|Link|
|---|---|---|
|AEM OAK |1.44-T20221206170501-6d59064 |[Oak API 1.44.0 API](https://www.javadoc.io/doc/org.apache.jackrabbit/oak-api/1.44.0/index.html)| 
|AEM SLING API |Version 2.27.0 |[Apache Sling API 2.27.0 API](https://www.javadoc.io/doc/org.apache.sling/org.apache.sling.api/latest/index.html)|
|AEM HTL|Version 1.4.20-1.4.0 |[HTML Template Language Specification](https://github.com/adobe/htl-spec)|
|AEM Core Components|Version 2.21.2|[AEM WCM Core Components](https://github.com/adobe/aem-core-wcm-components)|
