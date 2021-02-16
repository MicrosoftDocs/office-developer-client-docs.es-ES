---
title: xlfGetName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetname
localization_priority: Normal
ms.assetid: 65780435-aaa2-47af-b44f-07be7aa769ee
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fdee0146ae2199097828e98abb96ffe43a64fc80
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436632"
---
# <a name="xlfgetname"></a>xlfGetName

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Devuelve la definición de un nombre tal como  aparece en la columna Hace referencia  al cuadro  de diálogo Administrador de nombres, que se muestra al hacer clic en Administrador de nombres en la sección Nombres definidos de la ficha **Fórmulas.**  Si la definición contiene referencias, se las da como referencias de estilo R1C1. Use **xlfGetName para** comprobar el valor definido por un nombre. Para obtener el nombre que corresponde a una definición, use [xlfGetDef](xlfgetdef.md).
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a>Parámetros

_pxNameText_ (**xltypeStr**)
  
Puede ser un nombre definido en la hoja; una referencia externa a un nombre definido en el libro activo, por ejemplo, ; o una referencia externa a un nombre definido en un libro abierto  `"!Sales"` concreto, por ejemplo,  `"[Book1]SHEET1!Sales"` .  _pxNameText_ también puede ser un nombre oculto. 
  
_pxInfoType_ (**xltypeBool**)
  
Especifica el tipo de información que se debe devolver sobre el nombre. Si **es FALSE** o se omite, se devuelve la definición. Si **es TRUE**, devuelve **TRUE** si el nombre se define solo para la hoja, **FALSE** si el nombre está definido para todo el libro. 
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

_pxRes_ (**xltypeStr**, **xltypeBool** o **xltypeErr**)
  
Dependiendo del valor pasado para  _pxInfoType_, devuelve la definición del nombre especificado (**xltypeStr**), o **TRUE** o **FALSE** (**xltypeBool**).
  
## <a name="remarks"></a>Comentarios

Si se ha seleccionado **la** casilla proteger la  hoja de cálculo y el contenido de las celdas bloqueadas en el cuadro de diálogo Proteger hoja para proteger el libro que contiene el nombre, **xlfGetName** devuelve el `#N/A` valor de error. Para ver el cuadro **de diálogo Proteger hoja,** haga clic **en Proteger hoja** en la **sección Cambios** de la **ficha** Revisar. 
  
En la tabla siguiente se enumeran tres ejemplos de los valores devueltos por una llamada a **xlfGetDef con** el argumento  _pxNameText_ especificado. 
  
|**Definición en Excel**|**_pxNameText_**|**Valor devuelto**|
|:-----|:-----|:-----|
|El nombre Ventas de una hoja se define como el número 523.  <br/> |"Ventas"  <br/> |"=523"  <br/> |
|El nombre Profit de la hoja activa se define como la fórmula =Sales-Costs.  <br/> |"! Profit"  <br/> |"=Sales-Costs"  <br/> |
|El nombre Base de datos de la hoja activa se define como el rango A1:F500.  <br/> |"! Base de datos"  <br/> |"=R1C1:R500C6"  <br/> |
   
## <a name="see-also"></a>Consulte también

- [xlfGetDef](xlfgetdef.md)
- [Funciones esenciales y útiles XLM de API de C](essential-and-useful-c-api-xlm-functions.md)

