---
title: PAGENAME (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251577
localization_priority: Normal
ms.assetid: 12e45f46-e773-9445-4c7f-c726ab648671
description: Devuelve el nombre de la página como una cadena.
ms.openlocfilehash: 530707530d60955f460d6a747024b98ebdd5ab62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822721"
---
# <a name="pagename-function"></a>Función PAGENAME

Devuelve el nombre de la página como una cadena.
  
## <a name="syntax"></a>Sintaxis

PAGENAME (** *IdIdiomaOpc* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _IdIdiomaOpc_ <br/> |Opcional  <br/> |**Número** <br/> |Se usa para especificar un idioma para la cadena devuelta por la función. Use 0 (valor predeterminado) para especificar el idioma local. Use 750 para especificar un idioma universal.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

String
  
## <a name="remarks"></a>Observaciones

Si el código de idioma indicado no es válido, se utiliza el idioma local.
  

