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
description: Se usa en el set_expression de la función SETATREF para indicar que set_expression debe evaluarse antes de asignar al parámetro de referencia en SETATREF.
ms.openlocfilehash: a11a7485e04d4deb31e9497476bb198d675bc68f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432985"
---
# <a name="setatrefeval-function"></a>Función SETATREFEVAL

Se usa en _el set_expression_ de la función SETATREF para indicar que set_expression debe  evaluarse antes de asignar al parámetro de referencia en SETATREF.  
  
## <a name="syntax"></a>Sintaxis

SETATREFEVAL(** *expr* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _expr_ <br/> |Obligatorio  <br/> |**Varía** <br/> | Expresión que se evalúa cuando la función SETATREF redirige set_expression  _a_ otra celda.  <br/> |
   
## <a name="remarks"></a>Comentarios

Al asignar el parámetro set_expression de la función SETATREF *a* una celda a  la que se hace referencia, Microsoft Visio escribe set_expression en la celda como expresión de forma predeterminada. Sin embargo, si la función SETATREFEVAL ajusta alguna parte del parámetro *set_expression,* Visio evalúa la expresión y reemplaza la función SETATREFEVAL por su resultado antes de resolver la expresión SETATREF. 
  
## <a name="example"></a>Ejemplo

Para conocer un ejemplo, vea el tema que trata la función [SETATREF](setatref-function.md). 
  

