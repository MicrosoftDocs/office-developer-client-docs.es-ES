---
title: SETATREFEVAL (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1042150
localization_priority: Normal
ms.assetid: b3f3a0a0-7b14-0b71-d247-ada81b93b66b
description: Se usa en el parámetro expresión_definida de la función SETATREF para indicar que expresión_definida debe evaluarse antes de asignar al parámetro referencia en SETATREF.
ms.openlocfilehash: 0826ef9ca91e180576c0b2611452758b238736a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823120"
---
# <a name="setatrefeval-function"></a>Función SETATREFEVAL

Se usa en el parámetro _expresión_definida_ de la función SETATREF para indicar que _expresión_conjunto_ debe evaluarse antes de asignar al parámetro _referencia_ en SETATREF. 
  
## <a name="syntax"></a>Sintaxis

SETATREFEVAL (** *expr* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _expr_ <br/> |Obligatorio  <br/> |**Varían** <br/> | Una expresión que se evalúa cuando la función SETATREF redirige _expresión_definida_ a otra celda.  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando se asigna el parámetro *expresión_definida* de la función SETATREF a una celda que se hace referencia, Microsoft Visio escribe *expresión_definida* en la celda como expresión de forma predeterminada. Sin embargo, si cualquier parte del parámetro *expresión_conjunto* se ajusta mediante la función SETATREFEVAL, Visio evalúa la expresión y reemplaza la función SETATREFEVAL con el resultado anterior a la resolución de la expresión SETATREF. 
  
## <a name="example"></a>Ejemplo

Para conocer un ejemplo, vea el tema que trata la función [SETATREF](setatref-function.md). 
  

