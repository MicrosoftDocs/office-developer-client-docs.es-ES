---
title: Comparación de entradas de libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e375367b-d107-4768-95de-00b8b9dc3511
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6ccd7a55c195b45b1fa83db6180efeacd41b968d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415358"
---
# <a name="comparing-address-book-entries"></a>Comparación de entradas de libreta de direcciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La implementación [de IABLogon::CompareEntryIDs](iablogon-compareentryids.md) del proveedor compara los identificadores de entrada de dos de los objetos del proveedor. MAPI llama a este método después de determinar que los dos identificadores de entrada contienen [mapiuid](mapiuid.md)registrado del proveedor . Por lo tanto, el **método CompareEntryIDs** no necesita comprobar que los identificadores de entrada pasados para los parámetros  _lpEntryID1_ y  _lpEntryID2_ pertenecen al proveedor. 
  
Llamar **a IABLogon::CompareEntryIDs** equivale **a** recuperar la propiedad PR_RECORD_KEY ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) para cada uno de los dos objetos y compararlos directamente.
  
 **Para implementar CompareEntryIds**
  
1. Compruebe el tipo de los identificadores de entrada pasados si su proveedor almacena esa información. Por ejemplo, un identificador de entrada puede pertenecer a un usuario de mensajería mientras que el otro puede pertenecer a una lista de distribución. Si los tipos no coinciden, establece el contenido del parámetro  _lpulResult_ en FALSE y devuelve. 
    
2. Compare los tamaños de los dos identificadores de entrada. Si no son iguales, establece el contenido del parámetro  _lpulResult_ en FALSE y devuelve. 
    
3. Compruebe que el tamaño de los identificadores de entrada es el tamaño correcto para su tipo. Si no es así, establezca el contenido del parámetro  _lpulResult_ en FALSE y devuelva el valor de error MAPI_E_UNKNOWN_ENTRYID. 
    
4. Compruebe si los identificadores de entrada son los mismos. Si se comparan por igual, establezca el contenido del parámetro  _lpulResult_ en TRUE y return. De lo contrario, estadóla en FALSE antes de devolverla. 
    
5. Si su proveedor compara un identificador de entrada a corto plazo con un identificador a largo plazo, debe compararse por igual.
    

