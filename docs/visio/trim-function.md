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
description: Quita todo el espacio del texto, excepto los espacios individuales que hay entre palabras.
ms.openlocfilehash: b947c9500012d0ceefe3e8044be387f7b810dda9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435722"
---
# <a name="trim-function"></a>Función TRIM

Quita todo el espacio del texto, excepto los espacios individuales que hay entre palabras. 
  
## <a name="syntax"></a>Sintaxis

TRIM (* * *Text* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatorio  <br/> |**String** <br/> |El texto cuyos espacios se desea eliminar.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Cadena
  
## <a name="remarks"></a>Comentarios

La función TRIM puede ser útil para tratar el texto proveniente de otra aplicación que presente un espaciado irregular.
  
## <a name="example"></a>Ejemplo

TRIM ("1 de enero de 2003") 
  
Devuelve "1 de enero, 2003". 
  

