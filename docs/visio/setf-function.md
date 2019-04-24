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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325840"
---
# <a name="setf-function"></a>Función SETF

Establece la fórmula de una celda. 
  
## <a name="syntax"></a>Sintaxis

SETF (GETREF (* * *celda* * *), * * *fórmula* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _móviles_ <br/> |Obligatorio  <br/> |**String** <br/> |La celda cuya fórmula desea establecer.  <br/> |
| _formula_ <br/> |Obligatorio  <br/> |**String** <br/> |La fórmula que desea usar.  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando se evalúa, el resultado de la expresión de la _fórmula_ se convierte en la nueva fórmula en la _celda_. Si la _fórmula_ se encuentra entre comillas, la expresión entrecomillada se escribe en la _celda_. Para establecer la _celda_ en una cadena, escriba una _fórmula_ en tres conjuntos de Comillas. 
  
La celda de destino debe especificarse usando una referencia GETREF() o mediante una cadena para evitar las referencias circulares. Se aconseja utilizar GETREF ya que Microsoft Visio puede ajustar las referencias en el caso de que la forma se transfiera a otro documento distinto.
  
Si no se especifica la _celda_ mediante GETREF o como una cadena, la función devuelve un error y no se cambia la fórmula de la celda. Si la _fórmula_ contiene un error de sintaxis, la función devolverá un error y no se cambiará la fórmula de la _celda_ . 
  
## <a name="example-1"></a>Ejemplo 1

SETF (GETREF (Scratch. a1), 1,5 en \* 6 + 1 ft)
  
Establece la fórmula de Scratch.A1 y le da el valor 21 pulgadas.
  
## <a name="example-2"></a>Ejemplo 2

SETF (GETREF (Scratch. a1), "1,5 en \* 6 + 1 ft")
  
Establece la fórmula de la grieta. A1 a la expresión 1,5 en\*6 + 1 ft.
  
## <a name="example-3"></a>Ejemplo 3

SETF( GETREF(Scratch.A1); """Diga """"aaah""""""")
  
Establece la fórmula de Scratch.A1 como el valor de la cadena "Diga ""aaah""", que se convierte en Diga "aaah".
  

