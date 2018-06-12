---
title: PATHLENGTH (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: Devuelve la longitud de la ruta de acceso definida en la sección de geometría especificada.
ms.openlocfilehash: 37cabbde9fc0782bc1fde46f3065d0c945c9dada
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822735"
---
# <a name="pathlength-function"></a>PATHLENGTH (función)

Devuelve la longitud de la ruta de acceso definida en la sección de geometría especificada.
  
## <a name="version-information"></a>Información de versión

Versión agregada: Visio 2010 
  
## <a name="syntax"></a>Sintaxis

PATHLENGTH (** *sección* ** ** *[, segmento]* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obligatorio  <br/> |**String** <br/> |Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).  <br/> |
| _segmento_ <br/> |Opcional  <br/> |**Integer** <br/> |Segmento basado en 1 de la ruta de acceso que se va a medir.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

 **Double**
  
## <a name="remarks"></a>Notas

Si no existe _section_ ni _segment_ , Microsoft Visio devuelve #REF!. 
  
Si incluye un valor _segment_ , PATHLENGTH devuelve la longitud de ese segmento solo. 
  

