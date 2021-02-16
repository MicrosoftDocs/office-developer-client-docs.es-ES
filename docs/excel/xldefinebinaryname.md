---
title: xlDefineBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlDefineBinaryName
keywords:
- Función xldefinebinaryname [excel 2007]
localization_priority: Normal
ms.assetid: e3e8f91b-cc31-4f09-9941-f950ae96820a
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3c7fc4f6b6fc7179c1ca84043895273b2781f8b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430255"
---
# <a name="xldefinebinaryname"></a>xlDefineBinaryName

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Se usa para asignar almacenamiento persistente para un **XLOPER XLOPER12** **xltypeBigData** /  . Los datos con un nombre binario definido se guardan con el libro y se puede tener acceso a los datos por nombre en cualquier momento. Para obtener más información, vea "Binary Name Scope Limitation" en [Problemas conocidos en el desarrollo de XLL de Excel.](known-issues-in-excel-xll-development.md)
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a>Parámetros

 _pxName_ (**xltypeStr**)
  
Cadena que especifica el nombre de los datos. La cadena está sujeta a las mismas restricciones de nomenclatura que los nombres definidos.
  
 _pxData_ (**xltypeBigData**)
  
Estructura bigdata que especifica los datos que se almacenarán. Cuando se llama a esta función, el miembro **lpbData** de la estructura **bigdata** debe apuntar a los datos para los que se define el nombre y el miembro **cbData** debe contener la longitud de los datos en bytes. 
  
Si no se especifica el argumento _pxData_ (**xltypeMissing**), se elimina la asignación con nombre especificada por _pxName._ 
  
## <a name="see-also"></a>Consulte también



[xlGetBinaryName](xlgetbinaryname.md)


[Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md)

