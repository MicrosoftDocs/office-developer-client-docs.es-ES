---
title: IF (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251442
localization_priority: Normal
ms.assetid: 66771ad3-0fb3-68ff-81da-d1162d37c05a
description: Devuelve valueiftrue si logicalexpression es TRUE. De lo contrario, devuelve valueiffalse.
ms.openlocfilehash: 8780bd3dd5ded1a950a5bf3f79333687f3b6843c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405474"
---
# <a name="if-function"></a>Función IF

Devuelve  _valueiftrue_ si  _logicalexpression_ es TRUE. De lo contrario, devuelve  _valueiffalse_.
  
## <a name="syntax"></a>Sintaxis

IF(** *logicalexpression* **, ** *valueiftrue* **, ** *valueiffalse* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _logicalexpression_ <br/> |Obligatorio  <br/> |**String** <br/> |Expresión que se va a evaluar.  <br/> |
| _valueiftrue_ <br/> |Obligatorio  <br/> |**Varía** <br/> |Valor que se devuelve  _si logicalexpression_ es true.  <br/> |
| _valueiffalse_ <br/> |Obligatorio  <br/> |**Varía** <br/> | Valor que se devuelve si  _logicalexpression_ es false.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Varía
  
## <a name="example"></a>Ejemplo

IF(Height \> 1.25 in,5,7)
  
Devuelve 5 si el alto de la forma es mayor de 1,25 pulgadas. Devuelve 7 si el alto de la forma es menor o igual que 1,25 pulgadas.
  

