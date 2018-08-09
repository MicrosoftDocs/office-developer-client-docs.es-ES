---
title: Obtener acceso a los miembros de una lista de distribución
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f724cac8-2d5d-42bc-a15e-99f77a99ce21
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 21975482c458998cbe158a84d535f911156ac392
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816389"
---
# <a name="accessing-the-members-of-a-distribution-list"></a>Obtener acceso a los miembros de una lista de distribución

  
  
**Hace referencia a**: Outlook 
  
 **Para obtener a los miembros de una lista de distribución**
  
1. Crear una matriz de etiqueta de la propiedad tamaño con las propiedades de los miembros que desea recuperar, como la **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) y **PR_DISPLAY_TYPE** ([ PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).
    
2. Llame a [IAddrBook::OpenEntry](iaddrbook-openentry.md) para abrir la lista de distribución. 
    
3. Llamar al método **IABContainer::GetContentsTable** de la lista de distribución para obtener acceso a su tabla de contenido. 
    
4. Llame a [HrQueryAllRows](hrqueryallrows.md) para recuperar todas las filas de la tabla que representa a los miembros de la lista de distribución. 
    

