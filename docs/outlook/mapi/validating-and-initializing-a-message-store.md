---
title: Validar e inicializar un almacén de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 74f0a1fe-2a79-4b32-ab88-85a8839a2639
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7a5a5045594e87953d967fddbdeefd5ac18c8a3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581975"
---
# <a name="validating-and-initializing-a-message-store"></a>Validar e inicializar un almacén de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando se abre un almacén de mensajes a través del método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) sin establecer la marca MDB_NO_MAIL, MAPI crea varias carpetas y se les asigna roles y los nombres predeterminados. MAPI es responsable de la creación de estas carpetas para evitar las incompatibilidades que inevitablemente se produciría si los clientes o los proveedores de almacén de mensajes fueron los responsables de la creación. 
  
En ocasiones, es necesario comprobar que se han creado las carpetas correspondientes y que son válidos. La función [HrValidateIPMSubtree](hrvalidateipmsubtree.md) está disponible para este propósito. Si se está validando el almacén de mensajes de forma predeterminada, pase el indicador MAPI_FULL_IPM_TREE. Se crea un grupo más amplio de carpetas para el almacén de mensajes predeterminado. Cuando **HrValidateIPMSubtree** recibe el indicador MAPI_FULL_IPM_TREE, busca las siguientes carpetas: 
  
- Carpeta raíz para el subárbol IPM
    
- Carpeta Elementos eliminados en la carpeta raíz IPM
    
- Carpeta Bandeja de entrada en la carpeta raíz IPM
    
- Carpeta en la carpeta raíz IPM Bandeja de salida
    
- Carpeta Elementos enviados en la carpeta raíz IPM
    
- Vistas de la carpeta en la carpeta raíz del almacén de mensajes
    
- Vistas comunes en la carpeta raíz del almacén de mensajes
    
- Carpeta de búsqueda en la carpeta raíz del almacén de mensajes
    
Si el almacén de mensajes no es el valor predeterminado, puede establecer o no establecer la marca MAPI_FULL_IPM_TREE. Cuando esta marca no está establecida, **HrValidateIPMSubtree** comprueba sólo la carpeta raíz del subárbol, la carpeta Elementos eliminados y la carpeta raíz de mensaje almacenan los resultados de búsqueda. 
  
Para inicializar un almacén de mensajes, almacenar las siguientes propiedades en la memoria para que estén disponibles:
  
- **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))
    
- **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))
    
Estas propiedades son máscaras de bits que describen las características del almacén de mensajes. **PR_VALID_FOLDER_MASK** tiene un bit establecido para cada carpeta especial que existe en el almacén de mensajes y tiene un identificador de entrada asignados que es válido. Para obtener más información acerca del acceso a estas carpetas y sus identificadores de entrada, vea [Abrir una carpeta de almacén de mensajes](opening-a-message-store-folder.md). 
  
 **PR_STORE_SUPPORT_MASK** tiene un bit establecido para cada característica admitida en el almacén de mensajes. Por ejemplo, si es compatible con un almacén de mensajes de notificación y texto con formato, su **PR_STORE_SUPPORT_MASK** tendrá el conjunto de bits STORE_NOTIFY_OK y STORE_RTF_OK. 
  
Otras propiedades que se almacenen localmente incluyen los identificadores de entrada para las carpetas que se describe la propiedad **PR_VALID_FOLDER_MASK** como válido. Cada una de estas carpetas especiales, excepto la carpeta Bandeja de entrada, tiene una propiedad de identificador de entrada asociada con él. Por ejemplo, el identificador de entrada de la carpeta Bandeja de salida es su propiedad **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)). Dado que estas carpetas son las carpetas que se va a abrir con frecuencia, es una buena idea hacer que sus identificadores de entrada disponibles.
  

