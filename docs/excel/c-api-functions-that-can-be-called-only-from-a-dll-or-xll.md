---
title: Funciones de la API de C que se pueden llamar solo desde una DLL o XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- funciones [Excel 2007], API de c llamada desde dll o XLL
localization_priority: Normal
ms.assetid: 87c9e75b-c364-4428-a169-010886313b85
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e6d2d3c824c482e3726cdaefa869393002a80f44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301655"
---
# <a name="c-api-functions-that-can-be-called-only-from-a-dll-or-xll"></a>Funciones de la API de C que se pueden llamar solo desde una DLL o XLL

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
La API de C proporciona 15 funciones de devolución de llamada de Microsoft Excel a las que solo se puede llamar mediante las funciones **Excel4**, **Excel4v**, **Excel12**o **Excel12v** (o una de estas funciones de forma indirecta mediante las funciones de Framework **Excel **o **Excel12f**). Esto significa que solo se puede llamar desde una DLL o XLL.
  
## <a name="in-this-section"></a>En esta sección

[xlAbort](xlabort.md)
  
[xlAsyncReturn](xlasyncreturn.md)
  
[xlCoerce](xlcoerce.md)
  
[xlDefineBinaryName](xldefinebinaryname.md)
  
[xlDisableXLMsgs](xldisablexlmsgs.md)
  
[xlEnableXLMsgs](xlenablexlmsgs.md)
  
[xlEventRegister](xleventregister.md)
  
[xlFree](xlfree.md)
  
[xlGetBinaryName](xlgetbinaryname.md)
  
[xlGetHwnd](xlgethwnd.md)
  
[xlGetInst](xlgetinst.md)
  
[xlGetInstPtr](xlgetinstptr.md)
  
[xlGetName](xlgetname.md)
  
[xlRunningOnCluster](xlrunningoncluster.md)
  
[xlSet](xlset.md)
  
[xlSheetId](xlsheetid.md)
  
[xlSheetNm](xlsheetnm.md)
  
[xlStack](xlstack.md)
  
[xlUDF](xludf.md)
  
## <a name="see-also"></a>Vea también



[Funciones de devolución de llamada de API de C de Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)

