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
ms.openlocfilehash: 6ccd7a55c195b45b1fa83db6180efeacd41b968d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335535"
---
# <a name="comparing-address-book-entries"></a>Comparar entradas de la libreta de direcciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La implementación de [IABLogon:: CompareEntryIDs](iablogon-compareentryids.md) del proveedor compara los identificadores de entrada para dos de los objetos de su proveedor. MAPI llama a este método después de determinar que los dos identificadores de entrada contienen la [MAPIUID](mapiuid.md)registrada del proveedor. Por lo tanto, el método **CompareEntryIDs** no tiene que comprobar si los identificadores de entrada pasados para los parámetros _lpEntryID1_ y _lpEntryID2_ pertenecen a su proveedor. 
  
Llamar a **IABLogon:: CompareEntryIDs** equivale a recuperar la propiedad **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) para cada uno de los dos objetos y compararlas directamente.
  
 **Para implementar CompareEntryIds**
  
1. Compruebe el tipo de los identificadores de entrada pasados si su proveedor almacena esa información. Por ejemplo, un identificador de entrada puede pertenecer a un usuario de mensajería mientras que el otro puede pertenecer a una lista de distribución. Si los tipos no coinciden, establezca el contenido del parámetro _lpulResult_ en false y vuelva. 
    
2. Compare los tamaños de los dos identificadores de entrada. Si no son iguales, establezca el contenido del parámetro _lpulResult_ en false y vuelva. 
    
3. Compruebe que el tamaño de los identificadores de entrada es el tamaño correcto para su tipo. Si no es así, establezca el contenido del parámetro _lpulResult_ en false y devuelva el valor de error MAPI_E_UNKNOWN_ENTRYID. 
    
4. Compruebe si los identificadores de entrada son iguales. Si se comparan de forma equitativa, establezca el contenido del parámetro _lpulResult_ en true y vuelva. De lo contrario, establézcalo en FALSE antes de volver. 
    
5. Si el proveedor compara un identificador de entrada a corto plazo con un identificador a largo plazo, debe compararse de forma equitativa.
    

