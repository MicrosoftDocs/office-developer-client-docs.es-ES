---
title: MSOTINT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: Modifica el color aumentando su luminosidad en el porcentaje especificado.
ms.openlocfilehash: d63b90d0cd6fcb35e23a8efa4ca9e13e2838bc21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335199"
---
# <a name="msotint-function"></a>Función MSOTINT

Modifica el color aumentando su luminosidad en el porcentaje especificado.
  
## <a name="version-information"></a>Información de versión

Versión añadida: Visio 2010
 
  
## <a name="syntax"></a>Sintaxis

MSOTINT (* * *color* * *, * * *deltaLum* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatorio  <br/> |**RVA** <br/> |Valor de color RGB estándar (rojo, verde, azul) o referencia a un color.  <br/> |
| _deltaLum_ <br/> |Obligatorio  <br/> |**Integer** <br/> |El cambio porcentual hacia el blanco (-100%) o negro (100%) del valor de _color_ .  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuanto más se aproxime el valor de _color_ a blanco o negro, menor será el cambio en el tinte generado por un valor de _deltaLum_ específico. 
  

