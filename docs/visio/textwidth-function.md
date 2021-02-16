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
ms.openlocfilehash: 43848bba4d24a0c31a3a084d123cd56140bf0709
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422036"
---
# <a name="textwidth-function"></a>Función TEXTWIDTH

Devuelve el ancho del texto compuesto de una forma. 
  
## <a name="syntax"></a>Sintaxis

TEXTWIDTH(** *shapename! TheText* ** ** *[,maximumwidth]* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _shapename!theText_ <br/> |Obligatorio  <br/> |**String** <br/> |Una referencia a la celda llamada TheText de la forma de destino.  _shapename!_ es el nombre de la forma de la que desea recuperar el texto.  <br/> |
| _maximumwidth_ <br/> |Opcional  <br/> |**Numérico** <br/> |Ancho máximo del bloque de texto.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

String
  
## <a name="remarks"></a>Comentarios

La función TEXTWIDTH se utiliza habitualmente para ajustar el ancho de una forma en función del texto que contiene.
  
Si  _sheetN!_ se omite, la forma predeterminada es la forma actual. 
  
Si  _se especifica maximumwidth,_ el resultado es la línea de texto más larga que cabe dentro  _de maximumwidth_. Si  _se omite maximumwidth,_ el resultado es el ancho total del texto. 
  
## <a name="example"></a>Ejemplo

TEXTWIDTH(TheText) 
  
Devuelve la longitud total del texto que hay dentro de la forma actual. 
  

