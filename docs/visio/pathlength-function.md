---
title: PATHLENGTH (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: Devuelve la longitud de la ruta de acceso definida en la sección de geometría especificada.
ms.openlocfilehash: e4f90c2bb886f54164bedab5f8d78fc528758414
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344418"
---
# <a name="pathlength-function"></a>Función PATHLENGTH

Devuelve la longitud de la ruta de acceso definida en la sección de geometría especificada.
  
## <a name="version-information"></a>Información de versión

Versión añadida: Visio 2010
 
  
## <a name="syntax"></a>Sintaxis

PATHLENGTH (* * *sección* * * * * *[, segmento]* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obligatorio  <br/> |**String** <br/> |Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).  <br/> |
| _sector_ <br/> |Opcional  <br/> |**Integer** <br/> |Segmento basado en 1 de la ruta de acceso que se va a medir.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

 **Doble**
  
## <a name="remarks"></a>Comentarios

Si la _sección_ o _segmento_ no existe, Microsoft Visio devuelve #REF!. 
  
Si incluye un valor de _segmento_ , PATHLENGTH solo devuelve la longitud de ese segmento. 
  

