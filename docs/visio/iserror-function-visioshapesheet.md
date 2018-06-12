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
description: Devuelve TRUE si el valor de referenciaDeCelda es cualquier tipo de error; de lo contrario, devuelve FALSE. La función ISERROR se utiliza en las fórmulas que hacen referencia a otra celda.
ms.openlocfilehash: c93801f5d61e45be5d178027405ead3aa129654d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822374"
---
# <a name="iserror-function-visioshapesheet"></a>Función ISERROR (VisioShapeSheet)

Devuelve TRUE si el valor de _referenciaDeCelda_ es cualquier tipo de error; de lo contrario, devuelve FALSE. La función ISERROR se utiliza en las fórmulas que hacen referencia a otra celda. 
  
## <a name="syntax"></a>Sintaxis

ISERROR (** *referenciaDeCelda* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _referenciaDeCelda_ <br/> |Obligatorio  <br/> |**String** <br/> |Referencia a una celda.  <br/> |
   
## <a name="example-1"></a>Ejemplo 1

|**Cell**|**Formula**|**Valor devuelto**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=IsError(Scratch.a1)  <br/> |TRUE  <br/> |
   
Devuelve TRUE (verdadero) ya que #N/A! es un error que la función ISERROR reconoce. Se puede utilizar la función ISERR para encontrar todos los tipos de error con excepción del error #N/A!
  
## <a name="example-2"></a>Ejemplo 2

|**Cell**|**Formula**|**Valor devuelto**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |="Casa"  <br/> |#VALUE!  <br/> |
|Scratch.B1  <br/> |=IsError(Scratch.X1)  <br/> |TRUE  <br/> |
   
Devuelve TRUE (verdadero) ya que #VALUE! es un error que la función ISERROR reconoce. Para construir una expresión en función del error #VALUE! se debe utilizar la función ISERRVALUE.
  

