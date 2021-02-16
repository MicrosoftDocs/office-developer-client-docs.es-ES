---
title: FORMATEX (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251590
localization_priority: Normal
ms.assetid: d375c971-fee2-baa3-dc4f-a26018e70e8a
description: Devuelve el resultado de la expresión evaluada en srcUnit como una cadena con formato según el formato expresado en dstUnit.
ms.openlocfilehash: e341cbcb16cc273f0413f98c195f77ad08946ab1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430969"
---
# <a name="formatex-function"></a>Función FORMATEX

Devuelve el resultado de la expresión evaluada en srcUnit como una cadena con formato según el formato expresado en dstUnit.
  
## <a name="syntax"></a>Sintaxis

FORMATEX(** *expression* **," ** *format* ** ",[ ** *srcUnit* ** ],[ ** *dstUnit* ** ],[ ** *langID* ** ][, ** *calID* ** ]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatorio  <br/> |**String** <br/> |Combinación de constantes, operadores, funciones y referencias a celdas de ShapeSheet que da como resultado un valor.  <br/> |
| _format_ <br/> |Obligatorio  <br/> |**String** <br/> |Imagen de formato usada para dar formato a la cadena. Para obtener más información acerca del formato de imágenes, vea [Acerca del formato de imágenes.](about-format-pictures.md)  <br/> |
| _srcUnit_ <br/> |Opcional  <br/> |**String** <br/> | Unidades usadas para evaluar expresión (pda, cm, etc.).  <br/> |
| _dstUnit_ <br/> |Opcional  <br/> |**String** <br/> |Unidades usadas para el resultado de expresión (pda, cm, etc.).  <br/> |
| _langID_ <br/> |Opcional  <br/> |**Number** <br/> |El idioma utilizado para dar formato a las imágenes de fecha y hora de Microsoft Office System.  <br/> |
| _calID_ <br/> |Opcional  <br/> |**Number** <br/> |El calendario usado para dar formato a las imágenes de fecha y hora de Microsoft Office System.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

String
  
## <a name="remarks"></a>Comentarios

El tipo de la expresión y el especificado en el formato de imagen controlan el comportamiento de la cadena devuelta. El valor de formato debe ser adecuado para el tipo de expresión.
  
El argumento unidadesDeOrigen se utiliza para dar la escala adecuada a los resultados de la expresión que carecen de tipo, por ejemplo 3 + 4. Si el resultado de expresión tiene un tipo explícito, como 3 m + 8 m, no se tiene en cuenta el valor de unidadesDeOrigen.
  
El argumento unidadesDeDestino se utiliza para especificar las unidades que se usan en el resultado con formato. Si no se especifican las unidadesDeDestino, se utilizan las unidades del resultado de la expresión.
  
Devuelve un error si el resultado de la expresión y el tipo esperado en formato son distintos, si hay errores de sintaxis en formato o si no se reconocen las unidades especificadas como unidadesDeOrigen o unidadesDeDestino.
  
## <a name="example"></a>Ejemplo

FORMATEX(5,5; "0,00 u", "cm", "ft") 
  
Devuelve 0,18 pies. 
  

