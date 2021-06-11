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
ms.openlocfilehash: 014db553156849d84bd07e0e416f8cb3fefb4e0b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422001"
---
# <a name="xlfgetdef"></a>xlfGetDef

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Devuelve el nombre, como texto, que se define para un área, un valor o una fórmula determinados de un libro. En Excel, este valor se muestra en la  columna Nombre del cuadro de diálogo  Administrador de  nombres, que se muestra al hacer clic en Administrador de nombres en la sección Nombres definidos de la ficha **Fórmulas.**  Use **xlfGetDef para** obtener el nombre que corresponde a una definición. Para obtener la definición de un nombre, use [xlfGetName](xlfgetname.md).
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a>Parameters

_pxDefText_ (**xltypeStr**)
  
Puede ser cualquier cosa a la que se pueda definir un nombre al que hacer referencia, incluida una referencia, un valor, un objeto o una fórmula.
  
Las referencias deben especificarse en estilo R1C1, como  `"R3C5"` . Si  _pxDefText_ es un valor o una fórmula, no es necesario incluir el signo igual que se muestra en la columna **Hace** referencia a en el cuadro de diálogo Administrador **de** nombres. Si hay más de un nombre para  _pxDefText_, **xlfGetDef** devuelve el primer nombre. Si ningún nombre coincide  _con pxDefText_, **xlfGetDef** devuelve el  `#NAME?` valor de error. 
  
_pxDocumentText_ (**xltypeStr**)
  
Especifica la hoja en la que _está pxDefText._ Si  _se omite pxDocumentText,_ se supone que es la hoja activa. 
  
_pxTypeNum_ (**xltypeNum**)
  
Número del 1 al 3 que especifica qué tipos de nombres se devuelven.
  
|**_pxTypeNum_**|**Devuelve**|
|:-----|:-----|
|1 u omitido  <br/> |Solo nombres normales.  <br/> |
|2  <br/> |Solo nombres ocultos.  <br/> |
|3  <br/> |Todos los nombres.  <br/> |
   
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

 _pxRes_ (**xltypeStr** o **xltypeErr**)
  
Devuelve el nombre asociado a la definición especificada.
  
## <a name="remarks"></a>Comentarios

En la tabla siguiente se enumeran cuatro ejemplos de los valores devueltos por una llamada a **xlfGetDef** con los argumentos especificados. 
  
|**Nombre definido en Excel**|**_pxDefText_**|**_pxDocumentText_**|**_pxTypeNum_**|**Valor devuelto**|
|:-----|:-----|:-----|:-----|:-----|
|El intervalo especificado en Sheet4 se denomina Ventas.  <br/> |"R2C2:R9C6"  <br/> |"Sheet4"  <br/> |\<omitido\>  <br/> |"Ventas"  <br/> |
|El valor 100 de Sheet4 se define como Constante.  <br/> |"100"  <br/> |"Sheet4"  <br/> |\<omitido\>  <br/> |"Constante"  <br/> |
|La fórmula especificada en Sheet4 se denomina SumTotal.  <br/> |"SUM(R1C1:R10C1)"  <br/> |"Sheet4"  <br/> |\<omitido\>  <br/> |"SumTotal"  <br/> |
|3 se define como el nombre oculto Contador en la hoja activa.  <br/> |"3"  <br/> |\<omitido\>  <br/> |2  <br/> |"Contador"  <br/> |
   
## <a name="see-also"></a>Vea también

- [xlfGetName](xlfgetname.md)
- [Funciones esenciales y útiles XLM de API de C](essential-and-useful-c-api-xlm-functions.md)

