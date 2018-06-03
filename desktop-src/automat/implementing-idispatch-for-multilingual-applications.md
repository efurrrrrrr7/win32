---
title: Implementing IDispatch for Multilingual Applications
description: When creating applications that will support multiple languages, you need to create separate type libraries for each supported language, as well as for versions of the IDispatch member functions that include dependencies for each language.
ms.assetid: 33f911b5-7e31-4c5e-943c-471875874b43
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# Implementing IDispatch for Multilingual Applications

When creating applications that will support multiple languages, you need to create separate type libraries for each supported language, as well as for versions of the [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) member functions that include dependencies for each language. In the example below, the Hello sample code has been modified to define LCIDs for both U.S. English and German.

 

 



