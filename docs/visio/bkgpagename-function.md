---
title: BKGPAGENAME (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253219
localization_priority: Normal
ms.assetid: f6e410ef-54d5-9c08-926b-97a2a9786622
description: Devuelve un nombre de la página de fondo como una cadena.
ms.openlocfilehash: 290fa62242298b3c513bf2870df37204fab31bf3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821659"
---
# <a name="bkgpagename-function"></a>BKGPAGENAME (función)

Devuelve un nombre de la página de fondo como una cadena.
  
## <a name="syntax"></a>Sintaxis

BKGPAGENAME (** *IdIdiomaOpc* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _IdIdiomaOpc_ <br/> |Opcional  <br/> |**Numérico** <br/> |Se usa para especificar un idioma para la cadena devuelta por la función. Use 0 (valor predeterminado) para especificar el idioma local. Use 750 para especificar un idioma universal.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Cadena
  
## <a name="remarks"></a>Notas

Si la página para la que se utiliza la función no tiene una página de fondo, la cadena "\<ningún fondo\>" se devuelve. 
  
Si el código de idioma indicado no es válido, se utiliza el idioma local. 
  

