---
title: POW (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251483
localization_priority: Normal
ms.assetid: c6519c55-5f98-ed0d-95b1-5443d0d23c0b
description: Devuelve un número elevado a la potencia de un exponente.
ms.openlocfilehash: 48870c679251a666a5756b2b684d262fe059eee0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822855"
---
# <a name="pow-function"></a>POW (función)

Devuelve un número elevado a la potencia de un exponente.
  
## <a name="syntax"></a>Sintaxis

POW (** *número* **, ** *exponente* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatorio  <br/> |**Número** <br/> |El número para elevar la potencia del exponente.  <br/> |
| _exponente_ <br/> |Obligatorio  <br/> |**Número** <br/> |El exponente.  <br/> |
   
## <a name="remarks"></a>Observaciones

_Número_ y _exponente_ pueden ser que no son enteros, y pueden ser negativos. Si _número_ no es 0 y _exponente_ es 0, esta función devuelve 1. Si _número_ es 0 y _exponente_ es negativo, esta función devuelve 0,0. Si tanto _número_ como _exponente_ son 0 o si _número_ es negativo y _exponente_ no es un entero, esta función devuelve 0,0. Si tanto _número_ como _exponente_ son negativos, esta función devuelve -1. #IND. 
  
## <a name="example"></a>Ejemplo

POW(5;2) 
  
Devuelve 25. 
  

