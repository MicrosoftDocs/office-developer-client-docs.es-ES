---
title: Validación e inicialización de un almacén de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 74f0a1fe-2a79-4b32-ab88-85a8839a2639
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 77b3f707fc36a868de5acd7c7ba4642a1da4e3c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433692"
---
# <a name="validating-and-initializing-a-message-store"></a>Validación e inicialización de un almacén de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Al abrir un almacén de mensajes mediante el método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) sin establecer la marca MDB_NO_MAIL, MAPI crea varias carpetas y les asigna nombres y roles predeterminados. MAPI es responsable de crear estas carpetas para evitar las incompatibilidades que se producirían inevitablemente si los clientes o los proveedores del almacén de mensajes fueran responsables de la creación. 
  
A veces es necesario comprobar que se han creado las carpetas adecuadas y que son válidas. La [función HrValidateIPMSubtree](hrvalidateipmsubtree.md) está disponible para este fin. Si va a validar el almacén de mensajes predeterminado, pase MAPI_FULL_IPM_TREE marca. Se crea un grupo más amplio de carpetas para el almacén de mensajes predeterminado. Cuando **HrValidateIPMSubtree** recibe la marca MAPI_FULL_IPM_TREE, busca las siguientes carpetas: 
  
- Carpeta raíz del subárbol IPM
    
- Carpeta Elementos eliminados en la carpeta raíz de IPM
    
- Carpeta bandeja de entrada en la carpeta raíz de IPM
    
- Carpeta bandeja de salida en la carpeta raíz de IPM
    
- Carpeta Elementos enviados en la carpeta raíz de IPM
    
- Vistas de carpeta en la carpeta raíz del almacén de mensajes
    
- Vistas comunes en la carpeta raíz del almacén de mensajes
    
- Carpeta de búsqueda en la carpeta raíz del almacén de mensajes
    
Si el almacén de mensajes no es el valor predeterminado, puede establecer o no establecer la marca MAPI_FULL_IPM_TREE mensaje. Cuando no se establece esta marca, **HrValidateIPMSubtree** comprueba solo la carpeta raíz del subárbol, la carpeta Elementos eliminados y la carpeta raíz de los resultados de búsqueda del almacén de mensajes. 
  
Para inicializar un almacén de mensajes, almacene las siguientes propiedades en la memoria para que estén disponibles fácilmente:
  
- **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))
    
- **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))
    
Estas propiedades son máscaras de bits que describen las características del almacén de mensajes. **PR_VALID_FOLDER_MASK** tiene un conjunto de bits para cada carpeta especial que existe en el almacén de mensajes y tiene un identificador de entrada asignado que es válido. Para obtener más información acerca del acceso a estas carpetas y a sus identificadores de entrada, consulte [Opening a Message Store Folder](opening-a-message-store-folder.md). 
  
 **PR_STORE_SUPPORT_MASK** tiene un conjunto de bits para cada característica admitida en el almacén de mensajes. Por ejemplo, si un almacén de mensajes  admite notificaciones y texto con formato, su PR_STORE_SUPPORT_MASK tendrá los STORE_NOTIFY_OK y STORE_RTF_OK bits establecidos. 
  
Otras propiedades que deben almacenarse localmente incluyen los identificadores de entrada de las carpetas que la **propiedad PR_VALID_FOLDER_MASK** describe como válidas. Cada una de estas carpetas especiales, excepto la carpeta Bandeja de entrada, tiene asociada una propiedad de identificador de entrada. Por ejemplo, el identificador de entrada de la carpeta Bandeja de salida **es PR_IPM_OUTBOX_ENTRYID** propiedad ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)). Dado que estas carpetas son las carpetas que se abrirán con frecuencia, es una buena idea tener sus identificadores de entrada disponibles fácilmente.
  

