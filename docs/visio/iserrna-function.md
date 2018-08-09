---
title: ISERRNA (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251451
localization_priority: Normal
ms.assetid: 6ee7dc3d-efe9-c862-f71d-034b3d9c3ec6
description: 'Devuelve TRUE si el valor de referenciaDeCelda es error del tipo #N/A! (no disponible); de lo contrario, devuelve FALSE. La función ISERRNA se utiliza en las fórmulas que hacen referencia a otra celda.'
ms.openlocfilehash: a471119265d77866e51ccc6bb556f2ce0095d31d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822372"
---
# <a name="iserrna-function"></a>Función ISERRNA

Devuelve TRUE si el valor de _referenciaDeCelda_ es error del tipo #N/A! (no disponible); de lo contrario, devuelve FALSE. La función ISERRNA se utiliza en las fórmulas que hacen referencia a otra celda. 
  
## <a name="syntax"></a>Sintaxis

ISERRNA (** *referenciaDeCelda* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _referenciaDeCelda_ <br/> |Obligatorio  <br/> |**String** <br/> |Referencia a una celda.  <br/> |
   
## <a name="example-1"></a>Ejemplo 1

|**Cell**|**Formula**|**Valor devuelto**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |="5 +3"  <br/> |"8"  <br/> |
|Scratch.B1  <br/> |=ISERRNA(Scratch.a1)  <br/> |FALSE  <br/> |
   
Devuelve FALSE (falso), ya que el valor devuelto está disponible.
  
## <a name="example-2"></a>Ejemplo 2

|**Cell**|**Formula**|**Valor devuelto**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=ISERRNA(Scratch.a1)  <br/> |TRUE  <br/> |
   
Devuelve TRUE (verdadero) ya que el valor devuelto es un error del tipo #N/A!
  

