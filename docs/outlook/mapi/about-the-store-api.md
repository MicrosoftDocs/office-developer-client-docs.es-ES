---
title: Información sobre la API del almacén
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: fb9b0a4c8ac1a2f41a0fddcd746dba5fc4bae1a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321752"
---
# <a name="about-the-store-api"></a>Información sobre la API del almacén

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La API de tienda proporciona funcionalidad de varios almacenes para almacenar proveedores. Proporciona las siguientes definiciones, tipos de datos, propiedades e interfaces.
  
Definiciones:
  
- [Constantes para la API de tienda](mapi-constants.md)
    
Tipos de datos:
  
- **[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**
    
- **[MSCAP_SELECTOR](mscap_selector.md)**
    
Propiedades con nombre:
  
- **[ArchiveSourceSupportMask](archivesourcesupportmask.md)**
    
- **[CrawlSourceSupportMask](crawlsourcesupportmask.md)**
    
- **[Mostrar tamaños de carpeta del servidor](display-server-folder-sizes-property.md)**
    
- **[Ocultar opción de actualización de reunión](hide-meeting-update-option-property.md)**
    
- **[Convertir en privado el tipo de tienda](make-store-type-private-property.md)**
    
- **[NoFolderScan](nofolderscan.md)**
    
> [!NOTE]
> Los proveedores de almacenamiento que no requieran ninguna de las funciones que ofrecen estas propiedades con nombre pueden omitirlos y no implementar la compatibilidad en la interfaz **IMAPIProp** . Como estas propiedades se proporcionan a partir de Microsoft Outlook 2003 Service Pack 1, agregarlos a un almacén en una versión anterior de Microsoft Outlook no tiene ningún efecto. Se omiten si no existen o si su valor es **false**. 
  
Propiedades:
  
- **[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**
    
- **[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**
    
- **[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**
    
- **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**
    
Interfaces:
  
- **[A ifoldersupport](ifoldersupportiunknown.md)**
    
- **[IMSCapabilities](imscapabilitiesiunknown.md)**
    
- **[IProxyStoreObject](iproxystoreobject.md)**
    
## <a name="registering-stores-for-indexing"></a>Registro de almacenes para la indización

El controlador de protocolo MAPI busca en el registro de Windows los almacenes que debe indizar para fines de búsqueda. Los proveedores de almacenamiento que deseen indizar deben registrarse en el registro de Windows. Para obtener más información sobre el registro de los proveedores de almacenamiento para la indización en Outlook 2013 o Outlook 2010, consulte [About registraTion Stores for Indexing](about-registering-stores-for-indexing.md).
  
## <a name="indexing-stores"></a>Indización de almacenes

Los proveedores de almacén MAPI pueden elegir permitir que el controlador del protocolo MAPI rastree e indizar mensajes en el almacén, o enviar notificaciones al indizador sólo cuando hay mensajes que se van a indizar. Para obtener más información acerca de la indexación basada en notificaciones, consulte [About Notification-based Store Indexing](about-notification-based-store-indexing.md).
  

