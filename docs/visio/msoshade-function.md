---
title: MSOSHADE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: Modifica el color disminuyendo su luminosidad en el porcentaje especificado.
ms.openlocfilehash: 207893552c7378589d4a648bf29ed88fcfd15224
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283713"
---
# <a name="msoshade-function"></a>Función MSOSHADE

Modifica el color disminuyendo su luminosidad en el porcentaje especificado.
  
## <a name="version-information"></a>Información de versión

Versión añadida: Visio 2010
 
  
## <a name="syntax"></a>Sintaxis

MSOSHADE (* * *color* * *, * * *-deltaLum* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatorio  <br/> |**RVA** <br/> |Valor de color RGB estándar (rojo, verde, azul) o referencia a un color.  <br/> |
| _-deltaLum_ <br/> |Obligatorio  <br/> |**Integer** <br/> |El cambio porcentual hacia el blanco (-100%) o negro (100%) del valor de _color_ .  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuanto más se aproxime el valor de _color_ a blanco o negro, menor será el cambio de la sombra producido por un valor _de deltaLum_ específico. 
  

