---
title: attConversationID y attParentID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bed36900-e44d-434b-a4f2-d10f2d6f70da
description: 'Última modificación: 12 de marzo de 2013'
ms.openlocfilehash: c5880aefe7c2dba2e5e4c5405aae2020bb86c711
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410052"
---
# <a name="attconversationid-and-attparentid"></a>attConversationID y attParentID

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La clave de la conversación de correo de Windows para trabajo en grupo 3,1 es una cadena de texto. El equivalente de MAPI es un valor binario. Para proporcionar compatibilidad con versiones anteriores, la implementación de TNEF convierte los datos binarios en texto y agrega un carácter null de terminación.
  
> [!NOTE]
> Las propiedades correspondientes de MAPI a las que se asignan estos atributos TNEF, PR_CONVERSATION_KEY y PR_PARENT_KEY, han quedado en desuso en Microsoft Exchange Server: uso de **PR_CONVERSATION_KEY**, el [PidTagConversationKey canónico Propiedad](pidtagconversationkey-canonical-property.md), sólo se conserva en Outlook para buscar **IPM. **Mensajes de MessageManager. 
  
## <a name="remarks"></a>Comentarios

La propiedad **PR_CONVERSATION_KEY** es el precursor contrario obsoleto del **PR_CONVERSATION_INDEX**, la [propiedad canónica PidTagConversationIndex](pidtagconversationindex-canonical-property.md) y **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic canónico ](pidtagconversationtopic-canonical-property.md), Que se debe usar en su lugar.
  
## <a name="see-also"></a>Ver también

- [Subárbol IPM](ipm-subtree.md)
- [Carpetas especiales de MAPI](mapi-special-folders.md)

