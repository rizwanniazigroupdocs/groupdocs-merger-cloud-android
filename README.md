![](https://img.shields.io/badge/api-v1.0-lightgrey) [![GitHub license](https://img.shields.io/github/license/groupdocs-merger-cloud/groupdocs-merger-cloud-android)](https://github.com/groupdocs-merger-cloud/groupdocs-merger-cloud-android/blob/master/LICENSE)

# GroupDocs.Merger Cloud SDK for Android
This repository contains GroupDocs.Merger Cloud SDK for Android source code. This SDK allows you to work with GroupDocs.Merger Cloud REST APIs in your Android applications on Java language.

GroupDocs.Merger Cloud allows you to merge documents and manipulate document structure across wide range of supported document types - PDF, DOCX/DOC, PPTX/PPT, XLSX/XLS, VSDX/VSD, ODT, ODS, ODP, HTML, EPUB and many others. Merge several documents into one, split single document to multiple documents, reorder or replace document pages, change page orientation, manage document password and perform other manipulations with GroupDocs.Merger Cloud API.

## Cloud Document Merger Features

- Merge two or more documents into a single file.
- Merge specific pages from several different documents into a single file.
- Join page ranges from various documents into a single resultant file.
- Split a source document into many different files.
- Generate image representation of document pages as a preview.
- Create a document image preview of all pages, specific pages, or a page range.
- Move, remove, rotate, swap, and extract document pages.
- Change portrait or landscape orientation of the document pages.
- Set, update or remove the document password.
- Extract basic information about the document.

## New Features & Enhancements Version 20.12

- Made the GroupDocs.Merger Cloud image available at the DockerHub.

## Supported Document File Formats

- Microsoft Word: DOC, DOCX, DOCM, DOT, DOTX, DOTM, RTF
- Microsoft Excel: XLS, XLSX, XLSB, XLSM, XLT, XLTX, XLTM
- Microsoft PowerPoint: PPT, PPTX, PPS, PPSX
- Microsoft Visio: VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX
- Microsoft OneNote: ONE
- OpenOffice: ODT, OTT, ODP, OTP, ODS
- Markup: HTML, MHT
- Fixed Layout: PDF, XPS
- Other: TEX, EPUB, CSV, TSV, TXT

## Page Manipulation File Formats

The following file formats are supported for trimming, moving, swapping pages or changing page orientation:
- Microsoft Word: DOC, DOCX, DOCM, DOT, DOTX, DOTM, RTF
- Microsoft Excel: XLS, XLSX, XLSB, XLSM, XLT, XLTX, XLTM
- Microsoft PowerPoint: PPT, PPTX, PPS, PPSX
- Microsoft Visio: VSDX, VSDM, VSSX, VSSM, VSTX, VSTM, VDX, VSX, VTX
- Microsoft OneNote: ONE
- OpenOffice: ODT, OTT, ODP, OTP, ODS
- Markup: HTML, MHT
- Fixed Layout: PDF, XPS
- Other: TEX, EPUB

## Page Rotation File Formats

- Fixed Layout: PDF, XPS
- Other: TEX, EPUB


## Installation
Add Internet permission in the AndroidManifest.xml. Example:
```xml
<manifest xmlns:android="http://schemas.android.com/apk/res/android" package="<package name>">
    <uses-permission android:name="android.permission.INTERNET" />
    ...
```

Add following repository and dependency to your android module's build.gradle
after "apply plugin: 'com.android.application'" section:
```
repositories {
    maven {
        url "https://repository.groupdocs.cloud/repo/"
    }
}

...
dependencies {
    ...
    implementation 'com.groupdocs:groupdocs-merger-cloud:19.5'
}
```

## Getting Started

Please follow the [installation](#installation) instruction and use the following Java code:
## Get Supported File Formats for Merger

```java
// Get Client Id and Client Secret from https://dashboard.groupdocs.cloud
String MyClientId = "";
String MyClientSecret = "";

// Create instance of the API
Configuration configuration = new Configuration(MyClientId, MyClientSecret);
InfoApi infoApi = new InfoApi(configuration);

FormatsResult response = infoApi.getSupportedFileFormats();
for (Format format : response.getFormats()) {
	System.out.println(format.getFileFormat());
}
```

## Licensing
All GroupDocs.Merger Cloud SDKs are licensed under [MIT License](LICENSE).

## GroupDocs.Merger Cloud SDKs in Popular Languages

| .NET | Java | PHP | Python | Ruby | Node.js | Android |
|---|---|---|---|---|---|---|
| [GitHub](https://github.com/groupdocs-merger-cloud/groupdocs-merger-cloud-dotnet) | [GitHub](https://github.com/groupdocs-merger-cloud/groupdocs-merger-cloud-java) | [GitHub](https://github.com/groupdocs-merger-cloud/groupdocs-merger-cloud-php) | [GitHub](https://github.com/groupdocs-merger-cloud/groupdocs-merger-cloud-python) | [GitHub](https://github.com/groupdocs-merger-cloud/groupdocs-merger-cloud-ruby)  | [GitHub](https://github.com/groupdocs-merger-cloud/groupdocs-merger-cloud-node) | [GitHub](https://github.com/groupdocs-merger-cloud/groupdocs-merger-cloud-android) |
| [NuGet](https://www.nuget.org/packages/GroupDocs.merger-Cloud/) | [Maven](https://repository.groupdocs.cloud/webapp/#/artifacts/browse/tree/General/repo/com/groupdocs/groupdocs-merger-cloud) | [Composer](https://packagist.org/packages/groupdocscloud/groupdocs-merger-cloud) | [PIP](https://pypi.org/project/groupdocs-merger-cloud/) | [GEM](https://rubygems.org/gems/groupdocs_merger_cloud)  | [NPM](https://www.npmjs.com/package/groupdocs-merger-cloud) | [Maven](https://repository.groupdocs.cloud/webapp/#/artifacts/browse/tree/General/repo/com/groupdocs/groupdocs-merger-cloud-android) |

[Home](https://www.groupdocs.cloud/) | [Product Page](https://products.groupdocs.cloud/merger/android) | [Docs](https://docs.groupdocs.cloud/merger/) | [Demos](https://products.groupdocs.app/merger/family) | [API Reference](https://apireference.groupdocs.cloud/merger/) | [Examples](https://github.com/groupdocs-merger-cloud/groupdocs-merger-cloud-android) | [Blog](https://blog.groupdocs.cloud/category/merger/) | [Free Support](https://forum.groupdocs.cloud/c/merger) | [Free Trial](https://purchase.groupdocs.cloud/trial)
