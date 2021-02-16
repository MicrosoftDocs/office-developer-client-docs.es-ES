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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414497"
---
# <a name="msoshade-function"></a>Función MSOSHADE

Modifica el color disminuyendo su luminosidad en el porcentaje especificado.
  
## <a name="version-information"></a>Información de versión

Versión añadida: Visio 2010
 
  
## <a name="syntax"></a>Sintaxis

MSOSHADE(** *color* **, ** *-deltaLum* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatorio  <br/> |**RVA** <br/> |Valor de color RGB estándar (rojo, verde, azul) o referencia a un color.  <br/> |
| _-deltaLum_ <br/> |Obligatorio  <br/> |**Integer** <br/> |El porcentaje cambia hacia blanco (-100%) o negro (100%) del valor  _de_ color.  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuanto más cerca  _esté el valor_ de color a blanco o negro, menor será el cambio a la sombra que produce un valor  _-deltaLum_ específico. 
  

