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
ms.openlocfilehash: c8bccbfeb7f04745a66831618deff490bc651b02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415155"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a>Propiedad canónica PidTagStoreEntryIdEmsmdbV1

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el estilo anterior (Microsoft Outlook 2002 y versiones anteriores) del identificador de entrada de un almacén de mensajes de Microsoft Exchange Server 2010 o Exchange Server 2013.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_STORE_ENTRYID_EMSMDB_V1  <br/> |
|Identificador:  <br/> |0x65F60102  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Propiedades de identificador  <br/> |
   
## <a name="remarks"></a>Comentarios

A partir de Microsoft Outlook 2003, los FQDN del servidor se integraban en los identificadores de entrada, lo que evitaba RPC adicionales para las referencias. Sin embargo, esto hace que los identificadores de entrada sean más largos e introduce más escenarios en los que se debe usar el método **CompareEntryIDs** para determinar si dos identificadores de entrada son equivalentes. La propiedad PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1) obtiene acceso al formato anterior del identificador de entrada de Exchange Server usado por Microsoft Outlook 2002 (Microsoft Office XP) y las versiones anteriores. Esto puede ahorrar espacio y reducir también el número de llamadas **CompareEntryIDs** necesarias para determinar cuándo los identificadores de entrada son equivalentes. Tenga en cuenta que el uso de los identificadores de entrada más antiguos para abrir un buzón de correo puede incurrir en algunas RPC adicionales si se requiere una referencia. 
  
Para obtener acceso a la propiedad PR_STORE_ENTRYID_EMSMDB_V1 mientras se está en el modo en caché, debe omitir la memoria caché mediante la marca MAPI_NO_CACHE con el método [IMAPIProp:: GetProps](imapiprop-getprops.md) . Si **PR_STORE_ENTRYID_EMSMDB_V1** no está disponible, el código debe volver a PR_STORE_ENTRYID. Solo Outlook 2003 a través de Microsoft Outlook 2013 admite la propiedad PR_STORE_ENTRYID_EMSMDB_V1. 
  
## <a name="see-also"></a>Ver también



[Propiedad canónica PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

