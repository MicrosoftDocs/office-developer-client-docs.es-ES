---
title: xlDefineBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlDefineBinaryName
keywords:
- función xlDefineBinaryName [excel 2007]
localization_priority: Normal
ms.assetid: e3e8f91b-cc31-4f09-9941-f950ae96820a
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 14515cc262ea398a9f200c0de3a1f6b64c758b3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815716"
---
# <a name="xldefinebinaryname"></a>xlDefineBinaryName

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Utilizado para asignar el almacenamiento persistente para un **xltypeBigData** **XLOPER**/ **XLOPER12**. Datos con un nombre definido binario se guardan con el libro y pueden tener acceso por su nombre en cualquier momento. Para obtener más información, vea "Limitación binarios de ámbito de nombre" de [Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a>Parámetros

 _pxName_ (**xltypeStr**)
  
Una cadena que especifica el nombre de los datos. La cadena está sujeto a los mismos nombres definidos como de restricciones de nomenclatura.
  
 _pxData_ (**xltypeBigData**)
  
Estructura de Bigdata especifica los datos que se almacenan. Cuando se llama a esta función, el miembro **lpbData** de la estructura **bigdata** debe apuntar a los datos para el que se define el nombre y el miembro **cbData** debe contener la longitud de los datos en bytes. 
  
Si el argumento de _pxData_ no está especificado (**xltypeMissing**), se elimina la asignación con nombre especificada por _pxName_ . 
  
## <a name="see-also"></a>Vea también



[xlGetBinaryName](xlgetbinaryname.md)


[Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md)

