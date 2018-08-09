---
title: NOT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251469
localization_priority: Normal
ms.assetid: 65873b32-2406-7c33-8e68-802461f467b2
description: Devuelve TRUE (1) si expresiónLógica es FALSE. De lo contrario, devuelve FALSE (0).
ms.openlocfilehash: e2359aaab18469cd4f272f71aca8d899a12b2120
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822681"
---
# <a name="not-function"></a>Función NOT

Devuelve TRUE (1) si _expresiónLógica_ es FALSE. De lo contrario, devuelve FALSE (0). 
  
## <a name="syntax"></a>Sintaxis

NO (** *expresiónLógica* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _expresiónLógica_ <br/> |Obligatorio  <br/> |**String** <br/> |La expresión lógica por evaluar.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Boolean
  
## <a name="example"></a>Ejemplo

NO (alto \> 0,75 pda) 
  
Devuelve 1 si Height es menor o igual que 0,75 pulgadas. Devuelve 0 si Height es mayor que 0,75 pulgadas. 
  

