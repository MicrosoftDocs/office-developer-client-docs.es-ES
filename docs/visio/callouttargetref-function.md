---
title: CALLOUTTARGETREF (función)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67cfd32-5911-d8e9-dd51-fd4885dd2b0d
description: Devuelve una referencia de hoja a la forma de destino de la forma de llamada.
ms.openlocfilehash: 1b0cb7c6737a810a0ade65f19afaff7bb4b9f616
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821681"
---
# <a name="callouttargetref-function"></a>Función CALLOUTTARGETREF

Devuelve una referencia de hoja a la forma de destino de la forma de llamada.
  
## <a name="version-information"></a>Información de versión

Versión añadida: Visio 2010
 
  
## <a name="syntax"></a>Sintaxis

CALLOUTTARGETREF()!
  
### <a name="return-value"></a>Valor devuelto

Referencia de ShapeSheet
  
## <a name="remarks"></a>Observaciones

Si la forma no es una forma de llamada, o si no está asociado con una forma de destino, CALLOUTTARGETREF devuelve #REF.
  
## <a name="example"></a>Ejemplo

CALLOUTTARGETREF()!Height 
  
Devuelve el valor de la celda Height de la forma que está asociada a la llamada. 
  

