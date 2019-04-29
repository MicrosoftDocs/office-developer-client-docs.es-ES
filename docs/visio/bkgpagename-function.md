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
description: Devuelve un nombre de página de fondo como una cadena.
ms.openlocfilehash: 3b628315052117fe853c8f9c0fc36572de25d871
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410318"
---
# <a name="bkgpagename-function"></a>Función BKGPAGENAME

Devuelve un nombre de página de fondo como una cadena.
  
## <a name="syntax"></a>Sintaxis

BKGPAGENAME (* * *ididiomaopc* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _Ididiomaopc_ <br/> |Opcional  <br/> |**Numérico** <br/> |Se usa para especificar un idioma para la cadena devuelta por la función. Use 0 (valor predeterminado) para especificar el idioma local. Use 750 para especificar un idioma universal.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Cadena
  
## <a name="remarks"></a>Comentarios

Si la página para la que se usa la función no tiene una página de fondo, se devuelve\<la cadena\>"sin fondo". 
  
Si el código de idioma indicado no es válido, se utiliza el idioma local. 
  

