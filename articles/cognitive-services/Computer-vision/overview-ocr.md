---
title: What is Optical character recognition?
titleSuffix: Azure Cognitive Services
description: The optical character recognition (OCR) service extracts visible text in an image and returns it as structured strings.
services: cognitive-services
author: PatrickFarley
manager: nitinme

ms.service: cognitive-services
ms.subservice: computer-vision
ms.topic: overview
ms.date: 03/29/2021
ms.author: pafarley
ms.custom: "seodec18, devx-track-csharp"
---

# What is Optical character recognition?

The Optical character recognition (OCR) service allows you to extract printed or handwritten text from images, such as photos of license plates or containers with serial numbers, as well as from documents&mdash;invoices, bills, financial reports, articles, and more. It uses deep learning based models and works with text on a variety of surfaces and backgrounds.

The OCR APIs support extracting printed text in [several languages](./language-support.md). Follow a [quickstart](./quickstarts-sdk/client-library.md) to get started.

![OCR demos](./Images/ocr-demo.gif)

This documentation contains the following types of articles:
* The [quickstarts](./quickstarts-sdk/client-library.md) are step-by-step instructions that let you make calls to the service and get results in a short period of time. 
* The [how-to guides](./Vision-API-How-to-Topics/call-read-api.md) contain instructions for using the service in more specific or customized ways.
<!--* The [conceptual articles](Vision-API-How-to-Topics/call-read-api.md) provide in-depth explanations of the service's functionality and features.
* The [tutorials](./tutorials/storage-lab-tutorial.md) are longer guides that show you how to use this service as a component in broader business solutions. -->

## Supported languages
The OCR APIs support a total of 73 languages for print style text. Refer to the full list of [OCR-supported languages](./language-support.md#optical-character-recognition-ocr). Handwritten-style OCR is supported exclusively for English.

## Input requirements

The **Read** call takes images and documents as its input. They have the following requirements:

* Supported file formats: JPEG, PNG, BMP, PDF, and TIFF
* For PDF and TIFF files, up to 2000 pages (only first two pages for the free tier) are processed.
* The file size must be less than 50 MB (4 MB for the free tier) and dimensions at least 50 x 50 pixels and at most 10000 x 10000 pixels. 
* The PDF dimensions must be at most 17 x 17 inches, corresponding to legal or A3 paper sizes and smaller.

## Read API 

The Computer Vision [Read API](https://westcentralus.dev.cognitive.microsoft.com/docs/services/computer-vision-v3-1-ga/operations/5d986960601faab4bf452005) is Azure's latest OCR technology ([learn what's new](./whats-new.md)) that extracts printed text (in several languages), handwritten text (English only), digits, and currency symbols from images and multi-page PDF documents. It's optimized to extract text from text-heavy images and multi-page PDF documents with mixed languages. It supports detecting both printed and handwritten text in the same image or document.

![How OCR converts images and documents into structured output with extracted text](./Images/how-ocr-works.svg)


## Use the cloud API or deploy on-premise
The Read 3.x cloud APIs are the preferred option for most customers because of ease of integration and fast productivity out of the box. Azure and the Computer Vision service handle scale, performance, data security, and compliance needs while you focus on meeting your customers' needs.

For on-premise deployment, the [Read Docker container (preview)](./computer-vision-how-to-install-containers.md) enables you to deploy the new OCR capabilities in your own local environment. Containers are great for specific security and data governance requirements.

## OCR API

The legacy [OCR API](https://westcentralus.dev.cognitive.microsoft.com/docs/services/computer-vision-v3-1-ga/operations/56f91f2e778daf14a499f20d) uses an older recognition model, supports only images, and executes synchronously, returning immediately with the detected text. See the OCR column of [supported languages](./language-support.md#optical-character-recognition-ocr) for a list of supported languages.

## RecognizeText API

> [!WARNING]
> The Computer Vision 2.0 RecognizeText operations are in the process of being deprecated in favor of the new [Read API](#read-api) covered in this article. Existing customers should [transition to using Read operations](upgrade-api-versions.md).

## Data privacy and security

As with all of the Cognitive Services, developers using the Computer Vision service should be aware of Microsoft's policies on customer data. See the [Cognitive Services page](https://www.microsoft.com/trustcenter/cloudservices/cognitiveservices) on the Microsoft Trust Center to learn more.

## Next steps

- Get started with the [OCR REST API or client library quickstarts](./quickstarts-sdk/client-library.md).
- Learn about the [Read 3.1 REST API](https://westcentralus.dev.cognitive.microsoft.com/docs/services/computer-vision-v3-1-ga/operations/5d986960601faab4bf452005).
- Learn about the [Read 3.2 public preview REST API](https://westus.dev.cognitive.microsoft.com/docs/services/computer-vision-v3-2-preview-3/operations/5d986960601faab4bf452005) with support for a total of 73 languages.
