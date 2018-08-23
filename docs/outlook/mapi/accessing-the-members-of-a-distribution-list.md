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
ms.openlocfilehash: a32552343fa90dfbbb3571f50846976a5f5f5edd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595366"
---
# <a name="accessing-the-members-of-a-distribution-list"></a>Obtener acceso a los miembros de una lista de distribución

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 **Para obtener a los miembros de una lista de distribución**
  
1. Crear una matriz de etiqueta de la propiedad tamaño con las propiedades de los miembros que desea recuperar, como la **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) y **PR_DISPLAY_TYPE** ([ PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).
    
2. Llame a [IAddrBook::OpenEntry](iaddrbook-openentry.md) para abrir la lista de distribución. 
    
3. Llamar al método **IABContainer::GetContentsTable** de la lista de distribución para obtener acceso a su tabla de contenido. 
    
4. Llame a [HrQueryAllRows](hrqueryallrows.md) para recuperar todas las filas de la tabla que representa a los miembros de la lista de distribución. 
    

