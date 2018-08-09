---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d837d87c479f70f0184a7cf1612dea5ab8c99e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815729"
---
# <a name="xleventregister"></a>xlEventRegister

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Se usa para registrar un controlador de eventos. Introdujo en Excel 2010.
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a>Parámetros

 _pxProcedure_ (**xltypeStr**)
  
El nombre de la función de controlador de eventos tal como se muestra en el código del archivo DLL.
  
 _pxEvent_ (**xltypeInt**)
  
El evento controlado por la función designada en el parámetro _pxProcedure_ . 
  
A partir de Excel 2010, Excel admite los siguientes eventos:
  
|**Evento**|**Descripción**|
|:-----|:-----|
|**xleventCalculationEnded** <br/> |Se produce cuando Excel completa un cálculo. Puede liberar cualquier recurso asignado durante el cálculo después de este evento.  <br/> |
|**xleventCalculationCanceled** <br/> |Se produce cuando el usuario los cálculos interrumpe el cálculo. El XLL debe detener cualquier actividad asincrónica. El evento CalculationEnded se produce inmediatamente después de este evento.  <br/> |
   
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Si se realiza correctamente, devuelve **TRUE** (**xltypeBool**). Si no lo consigue, devuelve **FALSE**.
  
## <a name="see-also"></a>Vea también



[Funciones asincrónicas definidas por el usuario](asynchronous-user-defined-functions.md)

