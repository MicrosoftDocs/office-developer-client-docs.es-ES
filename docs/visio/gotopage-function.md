---
title: GOTOPAGE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251432
localization_priority: Normal
ms.assetid: b131badf-1656-132e-0aae-eeedb917ba7a
description: Muestra la página que tiene el nombre pagename en la ventana activa.
ms.openlocfilehash: c96585406b6104aeedbe46c35024a4f13bb0953e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302971"
---
# <a name="gotopage-function"></a>Función GOTOPAGE

Muestra la página que tiene el nombre  *pagename*  en la ventana activa. 
  
## <a name="syntax"></a>Sintaxis

GOTOPAGE(" ** *pagename* ** ") 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _pagename_ <br/> |Obligatorio  <br/> |**String** <br/> |El nombre de la página a la que ir.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si ya hay una ventana que muestra la página, se activa esa ventana. Si  *el nombre de*  página no existe, la aplicación intenta navegar hasta https:// nombre de  *página*  /. Si Visio actúa como servidor local, la función GOTOPAGE no tiene ningún efecto. 
  
Puede utilizar la función HYPERLINK para buscar cualquier ruta de acceso DOS, UNC o dirección URL. 
  
En versiones anteriores de Visio, esta función se denominaba _GOTOPAGE. La versión 4.0 de Visio y posteriores aceptan cualquiera de las dos denominaciones. 
  

