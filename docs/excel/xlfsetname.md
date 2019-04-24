---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- función xlfsetname [Excel 2007]
localization_priority: Normal
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e6327ccf2cd18e42c3ef9abe538e6f669e498352
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310279"
---
# <a name="xlfsetname"></a>xlfSetName

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Se usa para crear y eliminar nombres definidos asociados a la DLL.
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a>Parameters

_pxNameText_ (**xltypeStr**)
  
El nombre del rango, que debe cumplir con las limitaciones habituales en Microsoft Excel en nombres válidos.
  
_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef**o **xltypeInt**)
  
(Opcional). El valor, el conjunto de valores, la celda o el rango de celdas que _pxNameText_ se define como. Si se omite, se elimina el nombre. 
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

_pxRes_ (**xltypeBool** o **xltypeErr**)
  
TRUE si la operación se realizó correctamente o FALSE si no se pudo crear o eliminar el nombre. Devuelve #VALUE! Si uno o varios de los argumentos no son válidos.
  
## <a name="remarks"></a>Comentarios

Cuando se registra una función o un comando mediante **xlfRegister** con un argumento _PxFunctionText_ válido, Excel crea un nombre asociado al recurso dll. Cuando se descarga el archivo DLL, estos nombres deben eliminarse con la [función xlfSetName](xlfsetname.md). Sin embargo, debido a un problema conocido en Excel, esta operación de eliminación genera un error. Para obtener m�s informaci�n, consulte [Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).
  
### <a name="example"></a>Ejemplo

Consulte el código de la función **xlAutoClose** en `\SAMPLES\GENERIC\GENERIC.C`.
  
## <a name="see-also"></a>Vea también

- [Funciones esenciales y útiles XLM de API de C](essential-and-useful-c-api-xlm-functions.md)

