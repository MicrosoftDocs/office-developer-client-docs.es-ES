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
description: 'Devuelve TRUE si el valor de referenciaDeCelda es el tipo de error #N/A! (no disponible); de lo contrario, devuelve FALSE. La función ISERRNA se usa en fórmulas que hacen referencia a otra celda.'
ms.openlocfilehash: 8a398eca6da659a6b8f29e4ef8e31b18abf56fde
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357263"
---
# <a name="iserrna-function"></a>Función ISERRNA

Devuelve TRUE si el valor de _referenciaDeCelda_ es el tipo de error #N/a! (no disponible); de lo contrario, devuelve FALSE. La función ISERRNA se usa en fórmulas que hacen referencia a otra celda. 
  
## <a name="syntax"></a>Sintaxis

ISERRNA (* * *referenciaDeCelda* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _referenciaDeCelda_ <br/> |Obligatorio  <br/> |**String** <br/> |Referencia a una celda.  <br/> |
   
## <a name="example-1"></a>Ejemplo 1

|**Cell**|**Formula**|**Valor devuelto**|
|:-----|:-----|:-----|
|Scratch. a1  <br/> |="5 +3"  <br/> |8,5  <br/> |
|Scratch. B1  <br/> |= ISERRNA (Scratch. a1)  <br/> |FALSE  <br/> |
   
Devuelve FALSE (falso), ya que el valor devuelto está disponible.
  
## <a name="example-2"></a>Ejemplo 2

|**Cell**|**Formula**|**Valor devuelto**|
|:-----|:-----|:-----|
|Scratch. a1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch. B1  <br/> |= ISERRNA (Scratch. a1)  <br/> |TRUE  <br/> |
   
Devuelve TRUE (verdadero) ya que el valor devuelto es un error del tipo #N/A!
  

