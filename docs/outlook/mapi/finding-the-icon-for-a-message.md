---
title: Buscar el icono de un mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80a97c3d-4bca-4819-9da4-ca0fbf3a686f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b351cc68e3c3d9f9c01acb4b3d0e52158e302d7a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409156"
---
# <a name="finding-the-icon-for-a-message"></a>Buscar el icono de un mensaje

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 **Para buscar el icono asociado a un mensaje**
  
1. Llame al método [IMAPIProp:: GetProps](imapiprop-getprops.md) del mensaje para recuperar su propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).
    
2. Llame a [MAPIOpenFormMgr](mapiopenformmgr.md) para recuperar un puntero de interfaz **IMAPIFormMgr** . Pase el puntero **IMAPISession** en el parámetro _pSession_ . 
    
3. Llamar a [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) para recuperar un puntero de interfaz **IMAPIFormInfo** . 
    
4. Use el puntero **IMAPIFormInfo** para llamar [a IMAPIProp:: GetProps](imapiprop-getprops.md) y recuperar las propiedades **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) y/o **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). 
    

