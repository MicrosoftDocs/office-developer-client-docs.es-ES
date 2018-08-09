---
title: xlfGetDef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetdef
localization_priority: Normal
ms.assetid: 68f5edbd-9040-46d3-acd5-dd51ca82f6fa
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 030c4e501e8a9eb4b6ce29d7fe0e171324b50b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815746"
---
# <a name="xlfgetdef"></a>xlfGetDef

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Devuelve el nombre, como texto, que se define para un área determinada, un valor o una fórmula en un libro. En Excel, este valor se muestra en la columna **nombre** del cuadro de diálogo **Administrador de nombres** , que se muestra al hacer clic en **Administrador de nombres** en la sección **Nombres definidos** en la ficha **fórmulas** usar **xlfGetDef** para obtener el nombre que corresponde a una definición. Para obtener la definición de un nombre, use [xlfGetName](xlfgetname.md).
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a>Parámetros

_pxDefText_ (**xltypeStr**)
  
Puede ser cualquier cosa que se puede definir un nombre para hacer referencia a, incluida una referencia, un valor, un objeto o una fórmula.
  
Referencias deberán incluirse en el estilo F1C1, tales como `"R3C5"`. Si _pxDefText_ es un valor o una fórmula, no es necesario incluir el signo de igual que se muestra en la columna **Hace referencia a** en el cuadro de diálogo **Administrador de nombres** . Si hay más de un nombre para _pxDefText_, **xlfGetDef** devuelve el nombre de la primera. Si ningún nombre coincide con _pxDefText_, **xlfGetDef** devuelve el `#NAME?` valor de error. 
  
_pxDocumentText_ (**xltypeStr**)
  
Especifica la hoja que _pxDefText_ se encuentra en. Si _pxDocumentText_ se omite, se supone que ésta la hoja de cálculo activa. 
  
_pxTypeNum_ (**xltypeNum**)
  
Un número de 1 a 3 que especifica qué tipos de nombres se devuelven.
  
|**_pxTypeNum_**|**Devuelve**|
|:-----|:-----|
|1 u omitido  <br/> |Nombres normales.  <br/> |
|2  <br/> |Nombres ocultos.  <br/> |
|3  <br/> |Todos los nombres.  <br/> |
   
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

 _pxRes_ (**xltypeStr** o **xltypeErr**)
  
Devuelve el nombre asociado a la definición especificada.
  
## <a name="remarks"></a>Comentarios

En la siguiente tabla se enumera los cuatro ejemplos de los valores devueltos por una llamada a **xlfGetDef** con los argumentos especificados. 
  
|**Nombre definido en Excel**|**_pxDefText_**|**_pxDocumentText_**|**_pxTypeNum_**|**Valor devuelto**|
|:-----|:-----|:-----|:-----|:-----|
|El intervalo especificado en Sheet4 es denominado ventas.  <br/> |"R2C2:R9C6"  <br/> |"Sheet4"  <br/> |\<se omite\>  <br/> |"Ventas"  <br/> |
|El valor 100 en Sheet4 se define como constante.  <br/> |"100"  <br/> |"Sheet4"  <br/> |\<se omite\>  <br/> |"Constante"  <br/> |
|La fórmula especificada en Sheet4 se denomina SumTotal.  <br/> |"SUM(R1C1:R10C1)"  <br/> |"Sheet4"  <br/> |\<se omite\>  <br/> |"SumTotal"  <br/> |
|3 se define como el contador de nombre oculto en la hoja activa.  <br/> |"3"  <br/> |\<se omite\>  <br/> |2  <br/> |"Contador"  <br/> |
   
## <a name="see-also"></a>Vea también

- [xlfGetName](xlfgetname.md)
- [Funciones esenciales y útiles XLM de API de C](essential-and-useful-c-api-xlm-functions.md)

