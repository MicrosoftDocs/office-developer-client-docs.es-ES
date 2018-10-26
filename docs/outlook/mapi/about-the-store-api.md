---
title: Información sobre la API del almacén
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: 'Última modificación: 25 de junio de 2012'
ms.openlocfilehash: d72df30eab5fde4288b5feba1d7045da05117bde
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579378"
---
# <a name="about-the-store-api"></a>Información sobre la API del almacén

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
La API de almacenar proporciona funcionalidad de almacén de varios para los proveedores de almacén. Proporciona las siguientes definiciones, propiedades, tipos de datos y las interfaces.
  
Definiciones:
  
- [Constantes de la API del almacén](mapi-constants.md)
    
Tipos de datos:
  
- **[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**
    
- **[MSCAP_SELECTOR](mscap_selector.md)**
    
Propiedades con nombre:
  
- **[ArchiveSourceSupportMask](archivesourcesupportmask.md)**
    
- **[CrawlSourceSupportMask](crawlsourcesupportmask.md)**
    
- **[Mostrar el tamaño de la carpeta de servidor](display-server-folder-sizes-property.md)**
    
- **[Ocultar la opción de actualización de la reunión](hide-meeting-update-option-property.md)**
    
- **[Asegúrese de almacén tipo privado](make-store-type-private-property.md)**
    
- **[NoFolderScan](nofolderscan.md)**
    
> [!NOTE]
> Los proveedores de almacén que no requieren cualquiera de la funcionalidad proporcionada por estas propiedades con nombre pueden simplemente pasar por alto y no implementar la compatibilidad en la interfaz de **IMAPIProp** . Debido a que estas propiedades se proporcionan a partir de Microsoft Outlook 2003 Service Pack 1, agregarlos a un almacén en una versión anterior de Microsoft Outlook no tiene ningún efecto. Se omiten si no existen o si su valor es **false**. 
  
Propiedades:
  
- **[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**
    
- **[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**
    
- **[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**
    
- **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**
    
Interfaces:
  
- **[IFolderSupport](ifoldersupportiunknown.md)**
    
- **[IMSCapabilities](imscapabilitiesiunknown.md)**
    
- **[IProxyStoreObject](iproxystoreobject.md)**
    
## <a name="registering-stores-for-indexing"></a>Registrar almacenes para la indización

El controlador de protocolo MAPI comprueba el registro de Windows para los almacenes que deben indizar para fines de búsqueda. Los proveedores de almacén que desean indizar deben estar registrados en el registro de Windows. Para obtener más información acerca de cómo registrar los proveedores de almacén para la indización en Outlook 2013 o Outlook 2010, vea el [Registro de almacenes para la indización](about-registering-stores-for-indexing.md).
  
## <a name="indexing-stores"></a>Almacenes de indización

Pueden elegir los proveedores de almacén MAPI permitir que al controlador de protocolo MAPI a rastrear e indizar los mensajes en el almacén, o enviar notificaciones al indizador sólo cuando hay mensajes que se va a indizar. Para obtener más información acerca de la indización basada en notificaciones, vea [About Notification-Based almacén de indización](about-notification-based-store-indexing.md).
  

