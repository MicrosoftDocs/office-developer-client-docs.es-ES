---
title: MSOTINT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: Modifica el color aumentando su luminosidad en el porcentaje especificado.
ms.openlocfilehash: 50e81b5202174c61905d3914c50feddcb05a91cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822694"
---
# <a name="msotint-function"></a>Función MSOTINT

Modifica el color aumentando su luminosidad en el porcentaje especificado.
  
## <a name="version-information"></a>Información de versión

Versión añadida: Visio 2010
 
  
## <a name="syntax"></a>Sintaxis

MSOTINT (** *color* **, ** *deltaLum* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatorio  <br/> |**RVA** <br/> |Valor de color RGB estándar (rojo, verde, azul) o referencia a un color.  <br/> |
| _deltaLum_ <br/> |Obligatorio  <br/> |**Integer** <br/> |El cambio de porcentaje hacia blanco (-100%) o negro (100%) desde el valor de _color_ .  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuanto más se aproxime el valor de _color_ blanco o negro, menor será el cambio al tono que es generada por un valor específico _deltaLum_ . 
  

