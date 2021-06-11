---
title: Información sobre la API del almacén
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: fb9b0a4c8ac1a2f41a0fddcd746dba5fc4bae1a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405558"
---
# <a name="about-the-store-api"></a>Información sobre la API del almacén

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La API de la Tienda proporciona funcionalidad de almacén varios a los proveedores de la tienda. Proporciona las siguientes definciones, tipos de datos, propiedades e interfaces.
  
Definiciones:
  
- [Constantes para la API de store](mapi-constants.md)
    
Tipos de datos:
  
- **[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**
    
- **[MSCAP_SELECTOR](mscap_selector.md)**
    
Propiedades con nombre:
  
- **[ArchiveSourceSupportMask](archivesourcesupportmask.md)**
    
- **[CrawlSourceSupportMask](crawlsourcesupportmask.md)**
    
- **[Tamaños de carpetas de servidor para mostrar](display-server-folder-sizes-property.md)**
    
- **[Ocultar opción de actualización de reunión](hide-meeting-update-option-property.md)**
    
- **[Hacer que el tipo de tienda sea privado](make-store-type-private-property.md)**
    
- **[NoFolderScan](nofolderscan.md)**
    
> [!NOTE]
> Los proveedores de almacenamiento que no requieren ninguna de las funciones ofrecidas por estas propiedades con nombre simplemente pueden omitirlas y no implementar la compatibilidad en la **interfaz IMAPIProp.** Dado que estas propiedades se proporcionan a partir de Microsoft Outlook 2003 Service Pack 1, agregarlas a un almacén en una versión anterior de Microsoft Outlook no tiene ningún efecto. Se omiten si no existen o si su valor es **false**. 
  
Propiedades:
  
- **[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**
    
- **[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**
    
- **[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**
    
- **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**
    
Interfaces:
  
- **[IFolderSupport](ifoldersupportiunknown.md)**
    
- **[IMSCapabilities](imscapabilitiesiunknown.md)**
    
- **[IProxyStoreObject](iproxystoreobject.md)**
    
## <a name="registering-stores-for-indexing"></a>Registro de almacenes para indización

El controlador de protocolo MAPI comprueba Windows registro de almacenes que debe indizar con fines de búsqueda. Los proveedores de almacenamiento que desean indizarse deben estar registrados en el Windows registro. Para obtener más información acerca del registro de proveedores de almacenes para la indización en Outlook 2013 o Outlook 2010, vea [About Registering Stores for Indexing](about-registering-stores-for-indexing.md).
  
## <a name="indexing-stores"></a>Almacenes de indización

Los proveedores de almacén MAPI pueden elegir permitir que el controlador de protocolo MAPI rastree e indexe mensajes en el almacén o envíe notificaciones al indizador solo cuando haya mensajes que se van a indizar. Para obtener más información acerca de la indización basada en notificaciones, [vea About Notification-Based Store Indexing](about-notification-based-store-indexing.md).
  

