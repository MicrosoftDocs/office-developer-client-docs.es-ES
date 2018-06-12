---
title: Función ROUND (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251491
localization_priority: Normal
ms.assetid: a374fe7d-7302-5365-81ab-64f5474d9d5c
description: Redondea un número a la precisión representada por númeroDeDígitos.
ms.openlocfilehash: 2457bdf6b46a2bb44b203497f02cc9b2ff034847
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823014"
---
# <a name="round-function-visioshapesheet"></a>Función ROUND (VisioShapeSheet)

Redondea un número a la precisión representada por *númeroDeDígitos* . 
  
## <a name="syntax"></a>Sintaxis

ROUND (** *número* **, ** *númeroDeDígitos* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatorio  <br/> |**Número** <br/> |El número que desea redondear.  <br/> |
| _igual_ <br/> |Obligatorio  <br/> |**Número** <br/> |El número de posiciones decimales de precisión.  <br/> |
   
## <a name="remarks"></a>Observaciones

Si _es mayor que 0,_ _número_ se redondea dejando el _númeroDeDígitos_ a la derecha del separador decimal. Si es _igual_ a 0, _número_ se redondeará al entero. Si _es menor que 0,_ _número_ se redondea dejando el _númeroDeDígitos_ a la izquierda del separador decimal. 
  
## <a name="example-1"></a>Ejemplo 1

ROUND(123.654,2)
  
Devuelve 123,65.
  
## <a name="example-2"></a>Ejemplo 2

ROUND(123.654,0)
  
Devuelve 124.
  
## <a name="example-3"></a>Ejemplo 3

ROUND(123.654,-1)
  
Devuelve 120.
  

