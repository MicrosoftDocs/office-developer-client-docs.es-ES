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
description: Muestra la página que tiene el nombre pagename en la ventana actualmente activa.
ms.openlocfilehash: 67f8a79b854fd6f2ae47e39877ffcdbe4a1be5cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822248"
---
# <a name="gotopage-function"></a>GOTOPAGE (función)

Muestra la página que tiene el nombre *pagename* en la ventana actualmente activa. 
  
## <a name="syntax"></a>Sintaxis

GOTOPAGE ("** *pagename* **") 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _pagename_ <br/> |Obligatorio  <br/> |**String** <br/> |El nombre de la página a la que ir.  <br/> |
   
## <a name="remarks"></a>Observaciones

Si una ventana ya muestra la página, esa ventana se convierte en activa. Si *pagename* no existe, la aplicación intenta vaya a http:// *pagename* /. Si Visio actúa como un servidor en contexto, la función GOTOPAGE tiene ningún efecto. 
  
Puede utilizar la función HYPERLINK para buscar cualquier ruta de acceso DOS, UNC o dirección URL. 
  
En versiones anteriores de Visio, esta función se denominaba _GOTOPAGE. La versión 4.0 de Visio y posteriores aceptan cualquiera de las dos denominaciones. 
  

