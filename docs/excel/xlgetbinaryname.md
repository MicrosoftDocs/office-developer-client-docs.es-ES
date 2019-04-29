---
title: xlGetBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetBinaryName
keywords:
- función xlgetbinaryname [Excel 2007]
localization_priority: Normal
ms.assetid: 66af3f78-65b5-42e0-82f9-ffd639d41751
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6d063213e3f83451e8a072e71f0878174214f73e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412467"
---
# <a name="xlgetbinaryname"></a>xlGetBinaryName

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Se usa para devolver un controlador para los datos guardados por la [función xlDefineBinaryName](xldefinebinaryname.md). Los datos con un nombre binario definido se guardan con el libro y se puede tener acceso a ellos por su nombre en cualquier momento. Para obtener más información, vea "limitación de ámbito de nombre binario" en [problemas conocidos de desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a>Parameters

_pxRes_ (**xltypeBigData** o **xltypeErr**)
  
Bigdatala estructura que especifica los datos recuperados o un error es que no se pueden recuperar los datos o no se ha definido el nombre. Cuando se devuelve la función, el miembro **hdata** de la**XLOPER12** **XLOPER**/ contiene un controlador para los datos con nombre.  _pxRes_ debe liberarse en una llamada a **xlFree** cuando ya no se requiera. 
  
_pxName_ (**xltypeStr**)
  
Una cadena que especifica el nombre de los datos.
  
## <a name="remarks"></a>Comentarios

Microsoft Excel es propietario del identificador de memoria devuelto en **hdata**. En Windows, el identificador es un identificador de memoria global (asignado por la función **GlobalAlloc** ). 
  
## <a name="see-also"></a>Ver también

- [xlDefineBinaryName](xldefinebinaryname.md)
- [Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

