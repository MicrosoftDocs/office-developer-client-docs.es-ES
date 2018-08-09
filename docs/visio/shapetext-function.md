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
ms.openlocfilehash: 53a0cb6e485ae2fd233792e1ebd9765426b7f798
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823193"
---
# <a name="shapetext-function"></a>Función SHAPETEXT

Obtiene el texto de una forma. 
  
## <a name="syntax"></a>Sintaxis

SHAPETEXT (** *nombreDeForma! TheText* ** ** *[, marca]* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _¡nombreDeForma! TheText_ <br/> |Obligatorio  <br/> ||Una referencia a la celda llamada TheText en la forma de destino.  _¡NombreDeForma!_ es el nombre de la forma desde la que desea recuperar el texto.  <br/> |
| _marca_ <br/> |Opcional  <br/> |**Numeric** <br/> |Un bit que especifica el formato del texto. La marca predeterminada (0) muestra el texto exactamente como se muestra en la forma.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

String
  
## <a name="remarks"></a>Observaciones

En la función SHAPETEXT, puede usar cualquier combinación de las siguientes marcas.
  
|**Flag**|**Descripción**|
|:-----|:-----|
|0  <br/> |Mostrar el texto exactamente como se muestra en la forma.  <br/> |
|1  <br/> |Incluir guiones.  <br/> |
|2  <br/> |No incluir el texto expandido en los campos.  <br/> |
|4  <br/> |Convertir los tabuladores en un espacio.  <br/> |
|8  <br/> |Convertir los tabuladores en varios espacios.  <br/> |
|16  <br/> |Convertir los retornos de carro y las nuevas líneas en espacios.  <br/> |
|32  <br/> |Convertir las comillas tipográficas en comillas normales.  <br/> |
|64  <br/> |Convertir los espacios en blanco contiguos en un solo espacio.  <br/> |
   
## <a name="example-1"></a>Ejemplo 1

SHAPETEXT(sheetN!TheText)
  
Devuelve el texto de la forma llamada hojaN exactamente como se muestra en la forma.
  
## <a name="example-2"></a>Ejemplo 2

SHAPETEXT(TheText)
  
Devuelve el texto de la forma actual exactamente como se muestra en la forma.
  
## <a name="example-3"></a>Ejemplo 3

SHAPETEXT(theText, 84)
  
Devuelve el texto de la forma actual. Además, convierte los espacios en blanco contiguos en un solo espacio (64), los retornos de carro y las nuevas líneas en espacios (16), y los tabuladores en un solo espacio (4). La suma de dichas marcas es 84.
  

