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
ms.openlocfilehash: 63bfc6e94950a621c2367b2d35d25e3de48b344f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815725"
---
# <a name="xlfgetname"></a>xlfGetName

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Devuelve la definición de un nombre tal como aparece en la columna **se refiere a** del cuadro de diálogo **Administrador de nombres** , que se muestra al hacer clic en **Administrador de nombres** en la sección **Nombres definidos** en la ficha **fórmulas** . Si la definición contiene referencias, se les da como referencias de estilo F1C1. Utilice **xlfGetName** para comprobar el valor definido por un nombre. Para obtener el nombre que corresponde a una definición, utilice [xlfGetDef](xlfgetdef.md).
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a>Parámetros

_pxNameText_ (**xltypeStr**)
  
Puede ser un nombre definido en la hoja; una referencia externa a un nombre definido en el libro activo, por ejemplo, `"!Sales"`; o una referencia externa a un nombre definido en un libro abierto determinado, por ejemplo, `"[Book1]SHEET1!Sales"`.  _pxNameText_ también puede ser un nombre oculto. 
  
_pxInfoType_ (**xltypeBool**)
  
Especifica el tipo de información para volver sobre el nombre. Si **es FALSE** o se omite, se devuelve la definición. Si **es TRUE**, devuelve **TRUE** si el nombre está definido para sólo la hoja, **FALSE** si no se define el nombre de todo el libro. 
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

_pxRes_ (**xltypeStr**, **xltypeBool**o **xltypeErr**)
  
Según el valor que se pasa para _pxInfoType_, devuelve la definición del nombre especificado (**xltypeStr**), o **es TRUE** o **FALSE** (**xltypeBool**).
  
## <a name="remarks"></a>Comentarios

Si se ha seleccionado la casilla de verificación **Proteger hoja y contenido de celdas bloqueadas** en el cuadro de diálogo **Proteger hoja** para proteger el libro que contiene el nombre, **xlfGetName** devuelve el `#N/A` valor de error. Para ver el cuadro de diálogo **Proteger hoja** , haga clic en **Proteger hoja** en la sección de **cambios** de la ficha **Revisar** . 
  
En la siguiente tabla se enumera los tres ejemplos de los valores devueltos por una llamada a **xlfGetDef** con el argumento especificado _pxNameText_ . 
  
|**Definición en Excel**|**_pxNameText_**|**Valor devuelto**|
|:-----|:-----|:-----|
|El nombre de ventas en una hoja se define como el número 523.  <br/> |"Ventas"  <br/> |"= 523"  <br/> |
|El beneficio de nombre de la hoja activa se define como la fórmula = costos de ventas.  <br/> |"! Beneficio"  <br/> |"= Costos de ventas"  <br/> |
|El nombre de la base de datos de la hoja activa se define como el intervalo de A1:F500.  <br/> |"! Base de datos"  <br/> |"= R1C1:R500C6"  <br/> |
   
## <a name="see-also"></a>Vea también

- [xlfGetDef](xlfgetdef.md)
- [Funciones esenciales y útiles XLM de API de C](essential-and-useful-c-api-xlm-functions.md)

