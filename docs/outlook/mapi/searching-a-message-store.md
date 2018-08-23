---
title: Búsqueda de un almacén de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9e8d4639-7507-4d98-b56f-a65be369dc40
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 74b63719f6d72e3c92cbcef6fdb26ee106d4b9aa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571839"
---
# <a name="searching-a-message-store"></a>Búsqueda de un almacén de mensajes

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Pueden buscar las aplicaciones cliente a través de una o varias carpetas busca los mensajes que coinciden con los criterios de búsqueda. La técnica más sencilla de búsqueda implica la aplicación de una restricción para definir los criterios y colocar los resultados en una carpeta de resultados de búsqueda, crea explícitamente para esta búsqueda o para una búsqueda anterior. No todos los almacenes de mensajes admiten esta técnica. 

Para determinar si el almacén de mensajes que utiliza admite el uso de las carpetas de resultados de búsqueda, llame a su método [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar la **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) (propiedad). Si se establece la marca STORE_SEARCH_OK, se admite la búsqueda. Si no está establecido, necesitará un planteamiento alternativo como la inspección manualmente las carpetas de destino.
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a>Para buscar una o varias carpetas en un almacén de mensajes
  
1. Si tiene una carpeta de resultados de búsqueda de una búsqueda anterior, vaya al paso 2. En caso contrario, para crear una carpeta de resultados de búsqueda:
    
    1. Recuperar el identificador de entrada de la carpeta raíz de resultados de búsqueda, llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) del almacén de mensajes y solicite **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).
        
    2. Llame a [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir la carpeta representada por PR_FINDER_ENTRYID. 
        
    3. Llamar al método [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) de la carpeta para crear una carpeta de resultados de búsqueda con el conjunto de marca FOLDER_SEARCH. 
    
2. Crear una restricción para retener el criterio de búsqueda. 
    
3. Crear una matriz de identificadores de entrada que representan las carpetas de búsqueda. Este paso es necesario si la carpeta de resultados de búsqueda se ha utilizado antes y desea que las mismas carpetas de búsqueda.
    
4. Llamar al método [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) de la carpeta de resultados de búsqueda, apuntar _lpContainerList_ a la matriz de identificador de entrada y _lpRestriction_ a la restricción. 
    
5. Si se ha registrado para las notificaciones de búsqueda completa con el almacén de mensajes, espere a que la notificación llegar.
    
6. Ver los resultados de la búsqueda mediante una llamada a los resultados de búsqueda (método) [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) de la carpeta para tener acceso a su tabla de contenido. 
    
7. Llamar el contenido [IMAPITable:: QueryRows](imapitable-queryrows.md) al método de la tabla para recuperar los mensajes que cumplen los criterios de búsqueda. 
    

