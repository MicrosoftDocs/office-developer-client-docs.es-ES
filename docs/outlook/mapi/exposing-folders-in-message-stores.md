---
title: Mostrar carpetas en los almacenes de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9309e47-2a92-4576-9921-c89cc48472c2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 457620dd0f805e78d12fc8feba09f8fc8aedc554
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341352"
---
# <a name="exposing-folders-in-message-stores"></a>Mostrar carpetas en los almacenes de mensajes

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Cada proveedor de almacenes de mensajes debe presentar una interfaz [IMAPIFolder](imapifolderimapicontainer.md) de alto nivel a las aplicaciones cliente. La carpeta de alto nivel se corresponde con el almacén de mensajes completo; proporciona acceso a las carpetas que los usuarios ven como el contenido del almacén de mensajes. Además, la carpeta de alto nivel se utiliza a menudo como la carpeta predeterminada para recibir mensajes IPC y como la carpeta desde la que se envían los informes de lectura. Los proveedores de almacenes de mensajes también deben presentar un subárbol IPM (un conjunto de carpetas que se utilizan para contener mensajes IPM) a las aplicaciones cliente. 
  
Las aplicaciones cliente pueden abrir la carpeta de alto nivel llamando al método [IMsgStore::OpenEntry](imsgstore-openentry.md) con 0 y NULL para los parámetros _cbEntryId_ y _lpEntryId_, respectivamente. Sin embargo, en la mayoría de los casos, las aplicaciones cliente abren el conjunto de carpetas que contienen los mensajes IPM. 
  
Para obtener una lista de las carpetas IPM en el árbol de carpetas del almacén de mensajes, siga este procedimiento:
  
1. Utilice la sesión MAPI para llamar al método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md). 
    
2. Utilice el puntero de base de datos del mensaje resultante para llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) para la propiedad **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
3. Llame al método [IMsgStore::OpenEntry](imsgstore-openentry.md) con el identificador de entrada para obtener un puntero **IMAPIFolder**. 
    
4. Llame al método [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) para obtener una tabla del contenido de la carpeta. 
    
5. Llame al método [IMAPITable::QueryRows](imapitable-queryrows.md) para obtener una lista de las carpetas de la carpeta de alto nivel. 
    
Los clientes MAPI usan estas carpetas para obtener acceso a otros objetos de carpeta y objetos mensaje en el almacén de mensajes. **IMAPIFolder** y su interfaz primaria [IMAPIContainer](imapicontainerimapiprop.md) contienen los métodos que debe implementar el proveedor del almacén de mensajes para rellenar las carpetas con objetos de mensajes y responder a solicitudes de cliente para operar en los mensajes.
  
## <a name="see-also"></a>Vea también



[Implementar carpetas en los almacenes de mensajes](implementing-folders-in-message-stores.md)

