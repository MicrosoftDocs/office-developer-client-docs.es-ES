---
title: TRIM (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027318
localization_priority: Normal
ms.assetid: 6f2d84fd-27eb-4c2f-a2e1-43d20e0c78be
description: Quita todo el espacio del texto, excepto los espacios individuales entre palabras.
ms.openlocfilehash: b396572041e880451ceb1ec6f0508528c0807bfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823450"
---
# <a name="trim-function"></a>Función TRIM

Quita todo el espacio del texto, excepto los espacios individuales entre palabras. 
  
## <a name="syntax"></a>Sintaxis

TRIM (** *texto* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatorio  <br/> |**String** <br/> |El texto cuyos espacios se desea eliminar.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

String
  
## <a name="remarks"></a>Observaciones

La función TRIM puede ser útil para tratar el texto proveniente de otra aplicación que presente un espaciado irregular.
  
## <a name="example"></a>Ejemplo

TRIM ("1 de enero de 2003") 
  
Devuelve "1 de enero, 2003". 
  

