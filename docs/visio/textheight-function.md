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
description: Devuelve el alto del texto compuesto en una forma donde ninguna línea de texto supere MaximumWidth.
ms.openlocfilehash: 7455f58f14f9a4a0ae1fcd5375dba5d5860d3852
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427412"
---
# <a name="textheight-function"></a>Función TEXTHEIGHT

Devuelve el alto del texto compuesto en una forma donde ninguna línea de texto supere _MaximumWidth_. 
  
## <a name="syntax"></a>Sintaxis

TEXTHEIGHT (* * *nombredeforma! TheText* * * * * *[, MaximumWidth]* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _nombredeforma! TheText_ <br/> |Obligatorio  <br/> |**String** <br/> |Una referencia a la celda llamada TheText de la forma de destino.  _nombredeforma!_ es el nombre de la forma desde la que desea recuperar el texto.  <br/> |
| _MaximumWidth_ <br/> |Opcional  <br/> |**Numérico** <br/> |Ancho máximo del bloque de texto.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Cadena
  
## <a name="remarks"></a>Comentarios

El valor que se devuelve incluye el alto del texto, los espacios que le preceden y le siguen, el espaciado entre líneas del texto y los márgenes superior e inferior del bloque de texto. Esta función se utiliza habitualmente para ajustar el alto de una forma en función del texto que contiene.
  
## <a name="example"></a>Ejemplo

TEXTHEIGHT(TheText,(Width - 0,5 pda)) 
  
Devuelve el alto del texto cuando se ajusta al ancho de la forma menos 0,5 pulgadas. 
  

