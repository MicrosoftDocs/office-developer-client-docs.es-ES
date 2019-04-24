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
description: Devuelve valueiftrue si expresiónLógica es TRUE. De lo contrario, devuelve valueiffalse.
ms.openlocfilehash: 8780bd3dd5ded1a950a5bf3f79333687f3b6843c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344768"
---
# <a name="if-function"></a>Función IF

Devuelve _valueiftrue_ si _expresiónLógica_ es true. De lo contrario, devuelve _valueiffalse_.
  
## <a name="syntax"></a>Sintaxis

IF (* * *expresiónLógica* * *, * * *valueiftrue* * *, * * *valueiffalse* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _expresiónLógica_ <br/> |Obligatorio  <br/> |**String** <br/> |Expresión que se va a evaluar.  <br/> |
| _valueiftrue_ <br/> |Obligatorio  <br/> |**Diferencias** <br/> |Valor que se va a devolver si _expresiónLógica_ es true.  <br/> |
| _valueiffalse_ <br/> |Obligatorio  <br/> |**Diferencias** <br/> | Valor que se va a devolver si _expresiónLógica_ es false.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Varía
  
## <a name="example"></a>Ejemplo

IF (height \> 1,25 en,5, 7)
  
Devuelve 5 si el alto de la forma es mayor de 1,25 pulgadas. Devuelve 7 si el alto de la forma es menor o igual que 1,25 pulgadas.
  

