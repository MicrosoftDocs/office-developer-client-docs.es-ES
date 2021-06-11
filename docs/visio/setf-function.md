---
title: SETF (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251496
localization_priority: Normal
ms.assetid: fcf415c1-171f-b75f-6e40-2bbdbe8b1cfb
description: Establece la fórmula de una celda.
ms.openlocfilehash: 63050de92394ebbdce6cfe053e15347ca3ce5c7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425977"
---
# <a name="setf-function"></a>Función SETF

Establece la fórmula de una celda. 
  
## <a name="syntax"></a>Sintaxis

SETF( GETREF(** *cell* ** ), ** *formula* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _celda_ <br/> |Obligatorio  <br/> |**String** <br/> |Celda cuya fórmula se debe establecer.  <br/> |
| _formula_ <br/> |Obligatorio  <br/> |**String** <br/> |La fórmula que desea usar.  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando se evalúa, el resultado de la expresión en  _la fórmula_ se convierte en la nueva fórmula de la  _celda_. Si  _la_ fórmula está entre comillas, la expresión entrecomillada se escribe en la  _celda_. Para establecer  _la celda_ en una cadena, escriba la  _fórmula_ entre tres conjuntos de comillas. 
  
La celda de destino debe especificarse usando una referencia GETREF() o mediante una cadena para evitar las referencias circulares. Se aconseja utilizar GETREF ya que Microsoft Visio puede ajustar las referencias en el caso de que la forma se transfiera a otro documento distinto.
  
Si  _la_ celda no se especifica mediante GETREF o como una cadena, la función devuelve un error y no se cambia la fórmula de ninguna celda. Si  _la_ fórmula contiene un error de sintaxis, la función devuelve un error y no se cambia la fórmula  _de_ la celda. 
  
## <a name="example-1"></a>Ejemplo 1

SETF( GETREF(Scratch.A1), 1,5 en \* 6 + 1 ft)
  
Establece la fórmula de Scratch.A1 y le da el valor 21 pulgadas.
  
## <a name="example-2"></a>Ejemplo 2

SETF( GETREF(Scratch.A1), "1,5 in \* 6 + 1 ft")
  
Establece la fórmula de Scratch. A1 a la expresión 1,5 en \* 6+1 pies.
  
## <a name="example-3"></a>Ejemplo 3

SETF( GETREF(Scratch.A1); """Diga """"aaah""""""")
  
Establece la fórmula de Scratch.A1 como el valor de la cadena "Diga ""aaah""", que se convierte en Diga "aaah".
  

