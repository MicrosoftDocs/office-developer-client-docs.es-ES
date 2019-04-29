---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 869122954ffe3928dfea72b8fc9fb432b9979e42
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438767"
---
# <a name="xleventregister"></a>xlEventRegister

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Se usa para registrar un controlador de eventos. Se ha incluido en Excel 2010.
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a>Parameters

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

Si se ejecuta correctamente, devuelve **true** (**xltypeBool**). Si no se realiza correctamente, devuelve **false**.
  
## <a name="see-also"></a>Ver también



[Funciones asincrónicas definidas por el usuario](asynchronous-user-defined-functions.md)

