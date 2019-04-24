---
title: Función ISERROR (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251452
localization_priority: Normal
ms.assetid: 4864ebc2-fee6-2415-7c59-e0af8611f8d6
description: Devuelve TRUE si el valor de referenciaDeCelda es algún tipo de error; de lo contrario, devuelve FALSE. La función ISERROR se usa en fórmulas que hacen referencia a otra celda.
ms.openlocfilehash: a07b2345858e36dc2e4514d7e4f0f0d653491b50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317895"
---
# <a name="iserror-function-visioshapesheet"></a>Función ISERROR (VisioShapeSheet)

Devuelve TRUE si el valor de _referenciaDeCelda_ es algún tipo de error; de lo contrario, devuelve FALSE. La función ISERROR se usa en fórmulas que hacen referencia a otra celda. 
  
## <a name="syntax"></a>Sintaxis

ISERROR (* * *referenciaDeCelda* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _referenciaDeCelda_ <br/> |Obligatorio  <br/> |**String** <br/> |Referencia a una celda.  <br/> |
   
## <a name="example-1"></a>Ejemplo 1

|**Cell**|**Formula**|**Valor devuelto**|
|:-----|:-----|:-----|
|Scratch. a1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch. B1  <br/> |= ISERROR (Scratch. a1)  <br/> |TRUE  <br/> |
   
Devuelve TRUE (verdadero) ya que #N/A! es un error que la función ISERROR reconoce. Se puede utilizar la función ISERR para encontrar todos los tipos de error con excepción del error #N/A!
  
## <a name="example-2"></a>Ejemplo 2

|**Cell**|**Formula**|**Valor devuelto**|
|:-----|:-----|:-----|
|Grietas. x1  <br/> |= "Casa"  <br/> |#VALUE!  <br/> |
|Scratch. B1  <br/> |= ISERROR (Scratch. x1)  <br/> |TRUE  <br/> |
   
Devuelve TRUE (verdadero) ya que #VALUE! es un error que la función ISERROR reconoce. Para construir una expresión en función del error #VALUE! se debe utilizar la función ISERRVALUE.
  

