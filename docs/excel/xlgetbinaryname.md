---
title: xlGetBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetBinaryName
keywords:
- xlgetbinaryname (función) [excel 2007]
localization_priority: Normal
ms.assetid: 66af3f78-65b5-42e0-82f9-ffd639d41751
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d2332967e798b43a350c0733cd7398e2a921add6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815732"
---
# <a name="xlgetbinaryname"></a>xlGetBinaryName

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Se usa para devolver un identificador de datos guardados por la [función xlDefineBinaryName](xldefinebinaryname.md). Datos con un nombre definido binario se guardan con el libro y pueden tener acceso por su nombre en cualquier momento. Para obtener más información, vea "Binario" nombre de la limitación del ámbito de [Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a>Parámetros

_pxRes_ (**xltypeBigData** o **xltypeErr**)
  
No se pudo recuperar la estructura de Bigdata especifica que los datos recuperados o un error es los datos o el nombre no se ha definido. Cuando se devuelve la función, el miembro **hdata** de la **XLOPER**/ **XLOPER12** contiene un controlador para los datos con nombre.  _pxRes_ se debe liberar en una llamada a **xlFree** cuando ya no es necesaria. 
  
_pxName_ (**xltypeStr**)
  
Una cadena que especifica el nombre de los datos.
  
## <a name="remarks"></a>Comentarios

Microsoft Excel posee el identificador de memoria devuelto en **hdata**. En Windows, el identificador es un identificador de memoria global (asignado por la función **GlobalAlloc** ). 
  
## <a name="see-also"></a>Vea también

- [xlDefineBinaryName](xldefinebinaryname.md)
- [Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

