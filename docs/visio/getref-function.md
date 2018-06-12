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
description: Hace referencia a una celda y no recalcula la fórmula cuando cambia de la celda que se hace referencia.
ms.openlocfilehash: 454314b1f156f560c237f22a45492978ca3c31ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822224"
---
# <a name="getref-function"></a>GETREF (función)

Hace referencia a una celda y no recalcula la fórmula cuando cambia de la celda que se hace referencia.
  
## <a name="syntax"></a>Sintaxis

GETREF (** *nombreDeCelda* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _nombreDeCelda_ <br/> |Obligatorio  <br/> |**String** <br/> |El nombre de la celda para obtener una referencia a.  <br/> |
   
## <a name="example"></a>Ejemplo

SETF(GETREF(PinX),5.1) 
  
Establece el valor 5,1 en la fórmula de la celda PinX. 
  

