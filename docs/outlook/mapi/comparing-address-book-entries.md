---
title: Comparar entradas de la libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e375367b-d107-4768-95de-00b8b9dc3511
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e5c46aed7a15ae4f48c8e4f1fe308fcb20ab3fe7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575360"
---
# <a name="comparing-address-book-entries"></a>Comparar entradas de la libreta de direcciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
[IABLogon::CompareEntryIDs](iablogon-compareentryids.md) implementación de su proveedor compara los identificadores de entrada para dos de los objetos de su proveedor. MAPI llama a este método después de determinar que los identificadores de dos entrada contienen su proveedor había registrado [MAPIUID](mapiuid.md). Por lo tanto, el método **CompareEntryIDs** no necesita verificar que los identificadores de entrada que se pasó para los parámetros _lpEntryID1_ y _lpEntryID2_ pertenecen a su proveedor. 
  
Al llamar a **IABLogon::CompareEntryIDs** es equivalente a la recuperación de la propiedad **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) para cada uno de los dos objetos y su comparación directamente.
  
 **Para implementar CompareEntryIds**
  
1. Comprobar el tipo de los identificadores de entrada que se pasó si su proveedor almacena esa información. Por ejemplo, un identificador de entrada es posible que pertenecen a un usuario de mensajería mientras la otra es posible que pertenecen a una lista de distribución. Si los tipos no coinciden, establezca el contenido del parámetro _lpulResult_ en FALSE y devolución. 
    
2. Compare los tamaños de los identificadores de dos entrada. Si no son las mismas, establezca el contenido del parámetro _lpulResult_ en FALSE y devolver. 
    
3. Compruebe que el tamaño de los identificadores de entrada es el tamaño correcto para su tipo. Si no es así, Establece el contenido del parámetro _lpulResult_ en FALSE y devolver el valor de error MAPI_E_UNKNOWN_ENTRYID. 
    
4. Compruebe si los identificadores de entrada son los mismos. Si se comparan igualmente, establezca el contenido del parámetro _lpulResult_ en TRUE y devolución. De lo contrario, establézcalo en FALSE antes de devolverlo. 
    
5. Si su proveedor es comparar un identificador de entrada a corto plazo con un identificador a largo plazo, debe comparar igualmente.
    

