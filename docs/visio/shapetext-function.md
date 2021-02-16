---
title: SHAPETEXT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251788
localization_priority: Normal
ms.assetid: 87ea5e8f-c3e0-009f-4bf8-8c34fbdb83a6
description: Obtiene el texto de una forma.
ms.openlocfilehash: bb9b1fbe5900cd051828ed6c7ff07546567c1b23
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419348"
---
# <a name="shapetext-function"></a>Función SHAPETEXT

Obtiene el texto de una forma. 
  
## <a name="syntax"></a>Sintaxis

SHAPETEXT (** *shapename! TheText* ** ** *[,flag]* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _shapename! TheText_ <br/> |Obligatorio  <br/> ||Una referencia a la celda llamada TheText de la forma de destino.  _Shapename!_ es el nombre de la forma de la que desea recuperar el texto.  <br/> |
| _flag_ <br/> |Opcional  <br/> |**Numérico** <br/> |Un bit que especifica el formato del texto. La marca predeterminada (0) muestra el texto exactamente como se muestra en la forma.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

String
  
## <a name="remarks"></a>Comentarios

En la función SHAPETEXT, puede usar cualquier combinación de las siguientes marcas.
  
|**Flag**|**Descripción**|
|:-----|:-----|
|0  <br/> |Mostrar el texto exactamente como se muestra en la forma.  <br/> |
|1   <br/> |Incluir guiones.  <br/> |
|2   <br/> |No incluir el texto expandido en los campos.  <br/> |
|4   <br/> |Convertir los tabuladores en un espacio.  <br/> |
|8   <br/> |Convertir los tabuladores en varios espacios.  <br/> |
|16   <br/> |Convertir los retornos de carro y las nuevas líneas en espacios.  <br/> |
|32  <br/> |Convertir las comillas tipográficas en comillas normales.  <br/> |
|64  <br/> |Convertir los espacios en blanco contiguos en un solo espacio.  <br/> |
   
## <a name="example-1"></a>Ejemplo 1

SHAPETEXT(sheetN!theText)
  
Devuelve el texto de la forma llamada hojaN exactamente como se muestra en la forma.
  
## <a name="example-2"></a>Ejemplo 2

SHAPETEXT(theText)
  
Devuelve el texto de la forma actual exactamente como se muestra en la forma.
  
## <a name="example-3"></a>Ejemplo 3

SHAPETEXT(theText, 84)
  
Devuelve el texto de la forma actual. Además, convierte los espacios en blanco contiguos en un solo espacio (64), los retornos de carro y las nuevas líneas en espacios (16), y los tabuladores en un solo espacio (4). La suma de dichas marcas es 84.
  

