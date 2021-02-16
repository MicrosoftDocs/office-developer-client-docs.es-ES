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
ms.openlocfilehash: 85fbe66d4e458ac4e42c9eb3c65b9a3a1d8211df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425963"
---
# <a name="bound-function"></a>Función BOUND

Restringe el valor de una celda a un intervalo o conjunto de intervalos.
  
## <a name="syntax"></a>Sintaxis

BOUND (** *value* **, ** *type* **, ** *ignore* **, ** *value1* **, ** *value2* ** ** * [,ignore(n), value1(n), value2(n),...] * ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _value_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |Valor actual que se ha de restringir.  <br/> |
| _type_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |Indica si la restricción es inclusiva (0), exclusiva (1) o está deshabilitada (2).  <br/> |
| _ignore_ <br/> |Obligatorio  <br/> |**Boolean** <br/> | TRUE para omitir el rango; FALSE para restringir el valor de la celda al rango.  <br/> |
| _value1_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |Primer valor de un intervalo.  <br/> |
| _value2_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |Segundo valor de un intervalo.  <br/> |
   
## <a name="remarks"></a>Comentarios

Use la función BOUND para restringir el valor de una celda entre un límite superior y uno inferior, por ejemplo, para controlar objetos que no deben estirarse más allá de una altura máxima o mínima. La restricción puede ser inclusiva o exclusiva con respecto a los intervalos. Si el valor actual no debe restringirse, establezca el parámetro  _de_ tipo en 2 (deshabilitado). 
  
Puede definir varios intervalos si proporciona varias repeticiones de los parámetros _ignore_, _value1_ y _value2._ Use el  _parámetro ignore_ para deshabilitar las restricciones de un intervalo determinado. 
  
La fórmula que contiene la función BOUND no se sobrescribe cuando cambia su valor; en su lugar, la fórmula se conserva y el nuevo valor se coloca en el  _parámetro de_ valor. 
  
## <a name="example-1"></a>Ejemplo 1

En este ejemplo se usa la función BOUND para forzar a un controlador a mantenerse en el interior del cuadro delimitador de una forma. 
  
Controls.X1 = BOUND(Width \* 0.5, 0, FALSE, Width \* 0, Width \* 1)
  
Controls.Y1 = BOUND(Height \* 0.5, 0, FALSE, Height \* 0, Height \* 1)
  
## <a name="example-2"></a>Ejemplo 2

En este ejemplo se usa la función BOUND para restringir el ancho de una forma a 2, 4 ó 6 pulgadas. 
  
Width = BOUND(; 0; FALSE; 2 in; 2 in; FALSE; 4 in; 4 in; FALSE; 6 in; 6 in)
  

