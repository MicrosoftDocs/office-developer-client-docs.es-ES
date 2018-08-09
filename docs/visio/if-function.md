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
description: Devuelve valorSiTrue en si expresiónLógica es TRUE. De lo contrario, devuelve valorSiFalse.
ms.openlocfilehash: 55938e8bd78c02badb98f90665c5c26cdd70f3b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822318"
---
# <a name="if-function"></a>Función IF

Devuelve _valorSiTrue en_ si _expresiónLógica_ es TRUE. De lo contrario, devuelve _valorSiFalse_.
  
## <a name="syntax"></a>Sintaxis

IF (** *expresiónLógica* **, ** *ValorSiVerdadero* **, ** *valorSiFalse* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _expresiónLógica_ <br/> |Obligatorio  <br/> |**String** <br/> |Expresión que se va a evaluar.  <br/> |
| _ValorSiVerdadero_ <br/> |Obligatorio  <br/> |**Varían** <br/> |Valor que para devolver si _expresiónLógica_ es true.  <br/> |
| _valorSiFalse_ <br/> |Obligatorio  <br/> |**Varían** <br/> | Valor que para devolver si _expresiónLógica_ es false.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Varies
  
## <a name="example"></a>Ejemplo

IF (Height \> 1,25 pda, 5, 7)
  
Devuelve 5 si el alto de la forma es mayor de 1,25 pulgadas. Devuelve 7 si el alto de la forma es menor o igual que 1,25 pulgadas.
  

