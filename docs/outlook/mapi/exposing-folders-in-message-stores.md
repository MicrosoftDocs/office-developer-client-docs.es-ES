---
title: Exposici�n de las carpetas de almacenes de mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9309e47-2a92-4576-9921-c89cc48472c2
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 62f50ed7925305eca7432da17130d2be0365ef03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582598"
---
# <a name="exposing-folders-in-message-stores"></a>Exposici�n de las carpetas de almacenes de mensaje

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Cada proveedor de almac�n de mensajes debe presentar una interfaz de [IMAPIFolder](imapifolderimapicontainer.md) de nivel superior a las aplicaciones cliente. La carpeta de nivel superior se corresponde con el almac�n de todo el mensaje; proporciona acceso a las carpetas que los usuarios ven como el contenido del almac�n de mensajes. Adem�s, la carpeta de nivel superior se usa a menudo como el valor predeterminado de recepci�n carpeta para los mensajes IPC y como la carpeta desde la que se env�an los informes de lectura. Los proveedores de almac�n de mensajes tambi�n deben presentar un sub�rbol IPM, un conjunto de carpetas que se usa para contener los mensajes de IPM: a las aplicaciones cliente. 
  
Las aplicaciones cliente pueden abrir la carpeta de nivel superior mediante una llamada al m�todo de [IMsgStore::OpenEntry](imsgstore-openentry.md) con 0 y NULL para los par�metros  _cbEntryId_ y  _lpEntryId_, respectivamente. Sin embargo, en la mayor�a de los casos, las aplicaciones cliente de abran el conjunto de carpetas que contienen los mensajes de IPM. 
  
Para obtener una lista de carpetas en el �rbol de carpetas del almac�n de mensaje IPM, utilice el procedimiento siguiente:
  
1. Utilice la sesi�n de MAPI para llamar al m�todo [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) . 
    
2. Use el puntero resultante de base de datos de mensaje para llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) para la propiedad **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
3. Llame al m�todo [IMsgStore::OpenEntry](imsgstore-openentry.md) con el identificador de entrada para obtener un puntero de **IMAPIFolder**. 
    
4. Llame al m�todo [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) para obtener una tabla de contenido de la carpeta. 
    
5. Llame al m�todo [IMAPITable:: QueryRows](imapitable-queryrows.md) para ver una lista de las carpetas en la carpeta de nivel superior. 
    
Los clientes MAPI utilizan estas carpetas para obtener acceso a otros objetos folder y objetos de mensaje en el almac�n de mensajes. **IMAPIFolder**y su interfaz primaria [IMAPIContainer](imapicontainerimapiprop.md), contienen los m�todos que debe implementar el proveedor de almac�n de mensajes para rellenar las carpetas con objetos de mensaje y responder a las solicitudes de cliente para funcionar en los mensajes.
  
## <a name="see-also"></a>Vea también



[Implementar carpetas en los almacenes de mensajes](implementing-folders-in-message-stores.md)

