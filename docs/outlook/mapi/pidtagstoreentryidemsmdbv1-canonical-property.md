---
title: Propiedad canónica PidTagStoreEntryIdEmsmdbV1
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 40161358-4d41-43cf-83c7-fdd843bec87b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 505ea9ba5d7105f20f335035e42286fdab1cb1aa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576326"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a>Propiedad canónica PidTagStoreEntryIdEmsmdbV1

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene el estilo antiguo del identificador de entrada de un almacén de mensajes de Microsoft Exchange Server 2010 o Exchange Server 2013 (Microsoft Outlook 2002 y versiones anteriores).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_STORE_ENTRYID_EMSMDB_V1  <br/> |
|Identificador:  <br/> |0x65F60102  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Propiedades de Id.  <br/> |
   
## <a name="remarks"></a>Comentarios

A partir de Microsoft Outlook 2003, el FQDN de servidor se integran en los identificadores de entrada, lo que evita RPC adicionales para las referencias. Sin embargo, esto realiza más identificadores de entrada y presenta más escenarios donde se debe usar el método **CompareEntryIDs** para determinar si la entrada dos identificadores son equivalentes. El PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) (propiedad) tiene acceso al formato anterior del identificador de entrada de Exchange Server usado por Microsoft Outlook 2002 (Microsoft Office XP) y versiones anteriores. Esto puede ahorrar espacio y reducir también la cantidad de llamadas **CompareEntryIDs** necesarios para determinar cuándo los identificadores de entrada son equivalentes. Tenga en cuenta que mediante los identificadores de entrada anteriores para abrir un buzón de correo puede provocar algunos RPC adicionales si se requiere una referencia. 
  
Para obtener acceso a la propiedad PR_STORE_ENTRYID_EMSMDB_V1 mientras está en modo en caché, se debe omitir la memoria caché de uso de la marca MAPI_NO_CACHE con el método [IMAPIProp::GetProps](imapiprop-getprops.md) . Si **PR_STORE_ENTRYID_EMSMDB_V1** no está disponible, el código debe volver a PR_STORE_ENTRYID. Sólo Outlook 2003 a través de Microsoft Outlook 2013 admite la propiedad PR_STORE_ENTRYID_EMSMDB_V1. 
  
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

