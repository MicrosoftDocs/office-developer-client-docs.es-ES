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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303888"
---
# <a name="xlfgetname"></a>xlfGetName

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Devuelve la definición de un nombre tal como aparece en la columna se **refiere a** del cuadro de diálogo **Administrador de nombres** , que se muestra al hacer clic en **Administrador de nombres** en la sección **nombres definidos** de la ficha **fórmulas** . Si la definición contiene referencias, se proporcionan como referencias de estilo F1C1. Use **xlfGetName** para comprobar el valor definido por un nombre. Para obtener el nombre que corresponda a una definición, use [xlfGetDef](xlfgetdef.md).
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a>Parameters

_pxNameText_ (**xltypeStr**)
  
Puede ser un nombre definido en la hoja; una referencia externa a un nombre definido en el libro activo; por ejemplo, `"!Sales"`; o una referencia externa a un nombre definido en un libro abierto en particular, por ejemplo `"[Book1]SHEET1!Sales"`,.  _pxNameText_ también puede ser un nombre oculto. 
  
_pxInfoType_ (**xltypeBool**)
  
Especifica el tipo de información que se va a devolver sobre el nombre. Si es **false** o se omite, se devuelve la definición. Si es **true**, devuelve **true** si el nombre está definido sólo para la hoja, **false** si el nombre está definido para todo el libro. 
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

_pxRes_ (**xltypeStr**, **xltypeBool**o **xltypeErr**)
  
Dependiendo del valor pasado para _pxInfoType_, devuelve la definición del nombre especificado (**XltypeStr**) o **true** o **false** (**xltypeBool**).
  
## <a name="remarks"></a>Comentarios

Si la casilla de verificación **proteger hoja y contenido de celdas bloqueadas** está activada en el cuadro de diálogo **proteger hoja** para proteger el libro que contiene el nombre, `#N/A` **xlfGetName** devuelve el valor de error. Para ver el cuadro de diálogo **proteger hoja** , haga clic en **proteger hoja** en la sección **cambios** de la ficha **revisar** . 
  
En la tabla siguiente se muestran tres ejemplos de los valores devueltos por una llamada a **xlfGetDef** con el argumento _pxNameText_ especificado. 
  
|**Definición en Excel**|**_pxNameText_**|**Valor deVuelto**|
|:-----|:-----|:-----|
|El nombre sales en una hoja se define como el número 523.  <br/> |Lín  <br/> |"= 523"  <br/> |
|El beneficio del nombre de la hoja activa se define como la fórmula = ventas-costes.  <br/> |"! Beneficios  <br/> |"= Costos de ventas"  <br/> |
|La base de datos de nombres de la hoja activa se define como el rango a1: F500.  <br/> |"! Base  <br/> |"= F1C1: R500C6"  <br/> |
   
## <a name="see-also"></a>Vea también

- [xlfGetDef](xlfgetdef.md)
- [Funciones esenciales y útiles XLM de API de C](essential-and-useful-c-api-xlm-functions.md)

