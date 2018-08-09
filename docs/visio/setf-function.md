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
ms.openlocfilehash: a1e6a12014a77a20c0968b3ed2f7bc25badad8ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823127"
---
# <a name="setf-function"></a>Función SETF

Establece la fórmula de una celda. 
  
## <a name="syntax"></a>Sintaxis

SETF (GETREF (** *celda* **), ** *fórmula* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _celda_ <br/> |Obligatorio  <br/> |**String** <br/> |La celda cuya fórmula desea establecer.  <br/> |
| _formula_ <br/> |Obligatorio  <br/> |**String** <br/> |La fórmula que desea usar.  <br/> |
   
## <a name="remarks"></a>Observaciones

Cuando se evalúa, el resultado de la expresión en la _fórmula_ se convierte en la nueva fórmula de _celda_. Si la _fórmula_ está entre comillas, la expresión entrecomillada se escribe en la _celda_. Para establecer la _celda_ en una cadena, escriba la _fórmula_ en tres conjuntos de comillas dobles. 
  
La celda de destino debe especificarse usando una referencia GETREF() o mediante una cadena para evitar las referencias circulares. Se aconseja utilizar GETREF ya que Microsoft Visio puede ajustar las referencias en el caso de que la forma se transfiera a otro documento distinto.
  
Si no se especifica _celda_ mediante GETREF o como una cadena, la función devuelve un error y se cambia la fórmula de la celda no. Si la _fórmula_ contiene un error de sintaxis, la función devuelve un error y no se cambia la fórmula de la _celda_ . 
  
## <a name="example-1"></a>Ejemplo 1

SETF (GETREF(Scratch.A1), 1,5 pda \* 6 + 1 ft)
  
Establece la fórmula de Scratch.A1 y le da el valor 21 pulgadas.
  
## <a name="example-2"></a>Ejemplo 2

SETF (GETREF(Scratch.A1), "1,5 pda \* 6 + 1 ft")
  
Establece la fórmula de cero. A1 a la expresión 1,5 en\*6 + 1 ft.
  
## <a name="example-3"></a>Ejemplo 3

SETF( GETREF(Scratch.A1); """Diga """"aaah""""""")
  
Establece la fórmula de Scratch.A1 como el valor de la cadena "Diga ""aaah""", que se convierte en Diga "aaah".
  

