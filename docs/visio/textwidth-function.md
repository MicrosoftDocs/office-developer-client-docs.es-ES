---
title: TEXTWIDTH, función (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251505
localization_priority: Normal
ms.assetid: a9b8efcf-edc0-ad99-deae-21df16c58807
description: Devuelve el ancho del texto compuesto de una forma.
ms.openlocfilehash: d96b9489c08ce38205f8e9ad91e361fcb643c39c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823381"
---
# <a name="textwidth-function"></a>Función TEXTWIDTH

Devuelve el ancho del texto compuesto de una forma. 
  
## <a name="syntax"></a>Sintaxis

TEXTWIDTH (** *nombreDeForma! TheText* ** ** *[, valor]* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _nombreDeForma! theText_ <br/> |Obligatorio  <br/> |**String** <br/> |Una referencia a la celda llamada TheText en la forma de destino.  _¡nombreDeForma!_ es el nombre de la forma desde la que desea recuperar el texto.  <br/> |
| _valor_ <br/> |Opcional  <br/> |**Numeric** <br/> |Ancho máximo del bloque de texto.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

String
  
## <a name="remarks"></a>Observaciones

La función TEXTWIDTH se utiliza habitualmente para ajustar el ancho de una forma en función del texto que contiene.
  
Si _hojaN!_ es se omite, la forma predeterminada es la forma actual. 
  
Si se especifica _anchoMáximo_ , el resultado es la línea más larga de texto que cabe dentro de _anchoMáximo_. Si se omite el _valor_ , el resultado es el ancho total del texto. 
  
## <a name="example"></a>Ejemplo

TheText 
  
Devuelve la longitud total del texto que hay dentro de la forma actual. 
  

