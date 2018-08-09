---
title: TEXTHEIGHT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251504
localization_priority: Normal
ms.assetid: 5a10892f-c8fa-c127-2f5a-564009ce5411
description: Devuelve el alto del texto compuesto de una forma donde ninguna línea de texto excede el ancho máximo.
ms.openlocfilehash: 9a80dafcf80a1dcba968a0f60465aae4e2a2758b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823383"
---
# <a name="textheight-function"></a>Función TEXTHEIGHT

Devuelve el alto del texto compuesto de una forma donde ninguna línea de texto excede el _ancho máximo_. 
  
## <a name="syntax"></a>Sintaxis

TEXTHEIGHT (** *nombreDeForma! TheText* ** ** *[, valor]* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _nombreDeForma! theText_ <br/> |Obligatorio  <br/> |**String** <br/> |Una referencia a la celda llamada TheText en la forma de destino.  _¡nombreDeForma!_ es el nombre de la forma desde la que desea recuperar el texto.  <br/> |
| _valor_ <br/> |Opcional  <br/> |**Numeric** <br/> |Ancho máximo del bloque de texto.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

String
  
## <a name="remarks"></a>Observaciones

El valor que se devuelve incluye el alto del texto, los espacios que le preceden y le siguen, el espaciado entre líneas del texto y los márgenes superior e inferior del bloque de texto. Esta función se utiliza habitualmente para ajustar el alto de una forma en función del texto que contiene.
  
## <a name="example"></a>Ejemplo

TEXTHEIGHT(TheText,(Width - 0,5 pda)) 
  
Devuelve el alto del texto cuando se ajusta al ancho de la forma menos 0,5 pulgadas. 
  

