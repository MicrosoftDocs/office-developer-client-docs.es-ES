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
ms.openlocfilehash: c96585406b6104aeedbe46c35024a4f13bb0953e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397152"
---
# <a name="gotopage-function"></a>Función GOTOPAGE

Muestra la página que tiene el nombre *pagename* en la ventana actualmente activa. 
  
## <a name="syntax"></a>Sintaxis

GOTOPAGE ("** *pagename* **") 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _pagename_ <br/> |Obligatorio  <br/> |**String** <br/> |El nombre de la página a la que ir.  <br/> |
   
## <a name="remarks"></a>Observaciones

Si una ventana ya muestra la página, esa ventana se convierte en activa. Si *pagename* no existe, la aplicación intenta navegar a https:// *pagename* /. Si Visio actúa como un servidor en contexto, la función GOTOPAGE tiene ningún efecto. 
  
Puede utilizar la función HYPERLINK para buscar cualquier ruta de acceso DOS, UNC o dirección URL. 
  
En versiones anteriores de Visio, esta función se denominaba _GOTOPAGE. La versión 4.0 de Visio y posteriores aceptan cualquiera de las dos denominaciones. 
  

