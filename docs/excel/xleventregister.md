---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 00c222efce6925c3f691eb2b799adf687c22082c
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160282"
---
# <a name="xleventregister"></a>xlEventRegister

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Se usa para registrar un controlador de eventos. Se ha incluido en Excel 2010.
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a>Parámetros

 _pxProcedure_ (**xltypeStr**)
  
El nombre de la función del controlador de eventos tal como aparece en el código de DLL.
  
 _pxEvent_ (**xltypeInt**)
  
El evento controlado por la función designada en el parámetro _pxProcedure_ . 
  
A partir de Excel 2010, Excel admite los siguientes eventos:
  
|**Event**|**Descripción**|
|:-----|:-----|
|**xleventCalculationEnded** <br/> |Se produce cuando Excel completa un cálculo. Puede liberar los recursos asignados durante el cálculo después de este evento.  <br/> |
|**xleventCalculationCanceled** <br/> |Se produce cuando el usuario interrumpe el cálculo. El XLL debe detener todas las actividades asincrónicas. El evento CalculationEnded se genera inmediatamente después de este evento.  <br/> |
   
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Si se ejecuta correctamente, pxRes (**xltypeInt**) tiene un valor > 0. Si no se realiza correctamente, pxRes = = 0.
  
## <a name="see-also"></a>Vea también



[Funciones asincrónicas definidas por el usuario](asynchronous-user-defined-functions.md)

