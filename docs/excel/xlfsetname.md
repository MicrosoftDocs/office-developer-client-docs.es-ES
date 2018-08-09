---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- xlfSetName (función) [excel 2007]
localization_priority: Normal
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 48ce927f6bcb328a90779948a660cf9d0b460205
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815726"
---
# <a name="xlfsetname"></a>xlfSetName

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Se usa para crear y eliminar nombres definidos asociados con el archivo DLL.
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a>Parámetros

_pxNameText_ (**xltypeStr**)
  
El nombre del rango, que debe cumplir con las limitaciones de Microsoft Excel habituales sobre los nombres válidos.
  
_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef**o **xltypeInt**)
  
(Opcional). El valor, un conjunto de valores, celda o rango de celdas que _pxNameText_ se define como. Si se omite, se elimina el nombre. 
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

_pxRes_ (**xltypeBool** o **xltypeErr**)
  
Es TRUE si la operación se ha realizado correctamente o FALSE si no se pudo crea o elimina el nombre. ¡Devuelve #VALUE! Si uno o varios de los argumentos no es válido.
  
## <a name="remarks"></a>Comentarios

Cuando una función o un comando se registra mediante **xlfRegister** con un argumento válido _pxFunctionText_ , Excel crea un nombre asociado con el recurso de archivo DLL. Cuando se descarga el archivo DLL, se deben eliminar dichos nombres de uso de la [función xlfSetName](xlfsetname.md). Sin embargo, debido a un problema conocido en Excel, esta operación de eliminación se produce un error. Para obtener m�s informaci�n, consulte [Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).
  
### <a name="example"></a>Ejemplo

Vea el código para la función **xlAutoClose** en `\SAMPLES\GENERIC\GENERIC.C`.
  
## <a name="see-also"></a>Vea también

- [Funciones esenciales y útiles XLM de API de C](essential-and-useful-c-api-xlm-functions.md)

