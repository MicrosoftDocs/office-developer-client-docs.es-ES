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
ms.openlocfilehash: 512c686a9e5afeadacd8edccedba2c257df48f71
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567814"
---
# <a name="finding-the-icon-for-a-message"></a>Buscar el icono de un mensaje

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 **Para buscar el icono asociado a un mensaje**
  
1. Llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) del mensaje para recuperar su propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).
    
2. Llame a [MAPIOpenFormMgr](mapiopenformmgr.md) para recuperar un puntero de interfaz **IMAPIFormMgr** . Pase el puntero **IMAPISession** en el parámetro _pSession_ . 
    
3. Llame a [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) para recuperar un puntero de interfaz **IMAPIFormInfo** . 
    
4. Use el puntero **IMAPIFormInfo** para llamar a [IMAPIProp::GetProps](imapiprop-getprops.md) y recuperar el **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) y las propiedades de **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). 
    

