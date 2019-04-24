---
title: Buscar un almacén de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9e8d4639-7507-4d98-b56f-a65be369dc40
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7240f49a15fdaea4d1f30dae578d25c3f2c1c0f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338804"
---
# <a name="searching-a-message-store"></a>Buscar un almacén de mensajes

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las aplicaciones cliente pueden buscar en una o varias carpetas en busca de mensajes que coinciden con los criterios de búsqueda. La técnica de búsqueda más sencilla implica aplicar una restricción para definir criterios y colocar los resultados en una carpeta de resultados de búsqueda, creada explícitamente para esta búsqueda o para una búsqueda anterior. No todos los almacenes de mensajes admiten esta técnica. 

Para determinar si el almacén de mensajes que está usando admite o no el uso de carpetas de resultados de búsqueda, llame a su método [IMAPIProp:: GetProps](imapiprop-getprops.md) para recuperar la propiedad **\_PR STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). Si se establece la marca STORE_SEARCH_OK, se admite la búsqueda. Si no lo está, necesitará un enfoque alternativo, como inspeccionar manualmente las carpetas de destino.
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a>Para buscar en una o más carpetas de un almacén de mensajes
  
1. Si tiene una carpeta de resultados de búsqueda de una búsqueda anterior, vaya al paso 2. De lo contrario, para crear una carpeta de resultados de búsqueda:
    
    1. Para recuperar el identificador de entrada de la carpeta raíz de resultados de búsqueda, llame al método [IMAPIProp:: GetProps](imapiprop-getprops.md) del almacén de mensajes y solicite **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).
        
    2. Llame a [IMsgStore:: OpenEntry](imsgstore-openentry.md) para abrir la carpeta representada por PR_FINDER_ENTRYID. 
        
    3. Llame al método [IMAPIFolder:: CreateFolder](imapifolder-createfolder.md) de la carpeta para crear una carpeta de resultados de búsqueda con la marca FOLDER_SEARCH establecida. 
    
2. Cree una restricción para mantener los criterios de búsqueda. 
    
3. Cree una matriz de identificadores de entrada que representan las carpetas que se van a buscar. Este paso no es necesario si la carpeta de resultados de búsqueda se ha usado antes y desea buscar en las mismas carpetas.
    
4. Llame al método [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) de la carpeta de resultados de búsqueda, señale _lpContainerList_ a la matriz de identificadores de entrada y _lpRestriction_ a la restricción. 
    
5. Si se ha registrado para recibir notificaciones de búsqueda completada con el almacén de mensajes, espere a que la notificación llegue.
    
6. Para ver los resultados de la búsqueda, llame al método [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md) de la carpeta de resultados de búsqueda para obtener acceso a su tabla de contenido. 
    
7. Llame al método [IMAPITable:: QueryRows](imapitable-queryrows.md) de la tabla de contenido para recuperar los mensajes que cumplen los criterios de búsqueda. 
    

