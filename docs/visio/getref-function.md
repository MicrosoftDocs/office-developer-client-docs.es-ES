---
title: GETREF (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251884
localization_priority: Normal
ms.assetid: 25c9f817-d22b-28c9-1339-dc9f27d0dd41
description: Hace referencia a una celda y no actualiza la fórmula cuando cambia la celda a la que se hace referencia.
ms.openlocfilehash: 38f3c8b4f34ed2b3d3711be5faed6b0d317e907a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424332"
---
# <a name="getref-function"></a>Función GETREF

Hace referencia a una celda y no actualiza la fórmula cuando cambia la celda a la que se hace referencia.
  
## <a name="syntax"></a>Sintaxis

GETREF(** *cellname* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _cellname_ <br/> |Obligatorio  <br/> |**String** <br/> |Nombre de la celda a la que se debe obtener una referencia.  <br/> |
   
## <a name="example"></a>Ejemplo

SETF(GETREF(PinX),5.1) 
  
Establece el valor 5,1 en la fórmula de la celda PinX. 
  

