---
title: BOUND (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60099
localization_priority: Normal
ms.assetid: 36374d78-1028-bd7f-6282-66555ee31306
description: Restringe el valor de una celda a un intervalo o conjunto de intervalos.
ms.openlocfilehash: 2f6228828fee8fa1831bb0d3a714fca068808652
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821703"
---
# <a name="bound-function"></a>Función BOUND

Restringe el valor de una celda a un intervalo o conjunto de intervalos.
  
## <a name="syntax"></a>Sintaxis

ENLAZADO (** *valor* **, ** *tipo* **, ** *Omitir* **, ** *valor1* **, ** *valor2* ** ** * [, omitir, value1(n), valor2,...] * **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _value_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |Valor actual que se ha de restringir.  <br/> |
| _type_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |Indica si la restricción es inclusiva (0), exclusiva (1) o está deshabilitada (2).
  <br/> |
| _Omitir_ <br/> |Obligatorio  <br/> |**Boolean** <br/> | TRUE omite el intervalo; FALSE restringe el valor de la celda al intervalo.  <br/> |
| _valor1_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |Primer valor de un intervalo.
  <br/> |
| _valor2_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |Segundo valor de un intervalo.  <br/> |
   
## <a name="remarks"></a>Observaciones

Utilice la función BOUND para restringir una celda valor superior y límite inferior, por ejemplo, para controlar objetos que no se extiende por encima o por debajo de un alto mínimo o máximo. La restricción puede ser exclusivo con respecto al intervalo o intervalos o ambos inclusive. Si el valor actual no debe restringirse, establezca el parámetro de _tipo_ en 2 (desactivado). 
  
Puede definir varios intervalos proporcionando varias apariciones de los parámetros de _Omitir_, _valor1_y _valor2_ . Use el parámetro _Omitir_ para desactivar las restricciones en un intervalo determinado. 
  
La fórmula que contiene la función BOUND no se sobrescribe cuando cambia su valor; en su lugar, la fórmula se mantiene y el nuevo valor se coloca en el parámetro _value_ . 
  
## <a name="example-1"></a>Ejemplo 1

En este ejemplo se usa la función BOUND para forzar a un controlador a mantenerse en el interior del cuadro delimitador de una forma. 
  
Controls.X1 = BOUND (Width\*0,5; 0; FALSE; Width\*0; Width\*1)
  
Controls.Y1 = BOUND (Height\*0,5; 0; FALSE; Height\*0; Height\*1)
  
## <a name="example-2"></a>Ejemplo 2

En este ejemplo se usa la función BOUND para restringir el ancho de una forma a 2, 4 ó 6 pulgadas. 
  
Width = BOUND(; 0; FALSE; 2 in; 2 in; FALSE; 4 in; 4 in; FALSE; 6 in; 6 in)
  

