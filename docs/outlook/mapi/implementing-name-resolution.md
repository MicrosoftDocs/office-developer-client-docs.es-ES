---
title: Implementación de la resolución de nombres
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4c71b08-c47a-4421-8603-d5356d32dca9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 15c1d502947865c02973f4950b6b6fa8109b8e78
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434707"
---
# <a name="implementing-name-resolution"></a>Implementación de la resolución de nombres

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de libretas de direcciones son responsables de admitir la resolución de nombres, el proceso de asociar un identificador de entrada con un nombre para mostrar. Los clientes inician la resolución de nombres cuando llaman a [IAddrBook::ResolveName](iaddrbook-resolvename.md) para asegurarse de que cada miembro de la lista de destinatarios de un mensaje saliente corresponde a una dirección válida. 
  
El proveedor puede admitir la resolución de nombres mediante:
  
- Compatibilidad con la **restricción PR_ANR** propiedad ([PidTagAnr](pidtaganr-canonical-property.md)), un requisito para todos los contenedores de libreta de direcciones.
    
- Implementar el método [IABContainer::ResolveNames,](iabcontainer-resolvenames.md) una opción para todos los contenedores de libreta de direcciones. 
    
Si decide admitir **IABContainer::ResolveNames,** intente buscar una coincidencia exacta para cada nombre para mostrar no resuelto en la estructura [ADRLIST](adrlist.md) pasada con el parámetro _lpAdrList._ Puede identificar un nombre para mostrar sin resolver porque falta la propiedad **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) en la matriz de valores de propiedad en su **miembro aEntries** de la estructura **ADRLIST.** Ignore cualquier entrada que tenga cero propiedades asociadas. 
  
Informe del resultado del intento de resolución en el parámetro  _lpFlagList,_ una matriz de marcas que corresponde a la matriz de nombres para mostrar  _en lpAdrList_. Las marcas son posicionales de modo que la primera marca corresponde al primer miembro **aEntries** de la estructura **ADRLIST,** la segunda marca corresponde al segundo miembro **aEntries,** y así sucesivamente. 
  
Hay tres resultados posibles para cada entrada sin resolver:
  
- No se encontró ninguna coincidencia, lo que significa que ninguna de las entradas de las entradas del contenedor coincide con la entrada de la estructura **ADRLIST.** Establezca la entrada correspondiente en el  _parámetro lpFlagList_ en MAPI_UNRESOLVED. 
    
- Se pueden encontrar varias coincidencias, lo que significa que hay varias entradas de contenedor que coinciden con la entrada en la estructura **ADRLIST.** Establezca la entrada correspondiente en el  _parámetro lpFlagList_ en MAPI_AMBIGUOUS. No cambie el número de entradas en la **estructura ADRLIST.** 
    
- Se puede encontrar una coincidencia exacta, lo que significa que solo hay una entrada de contenedor que coincide con la entrada en la **estructura ADRLIST.** Establezca el miembro correspondiente en el parámetro _lpFlagList_ en MAPI_RESOLVED y agregue el identificador de entrada a la matriz de propiedades asociadas con la **entrada ADRLIST.** 
    
Si decides no admitir **IABContainer::ResolveNames,** devuelve MAPI_E_NO_SUPPORT de la implementación.
  
Todos los proveedores de libretas de direcciones deben admitir la resolución de **nombres** ambiguos (la PR_ANR de propiedad) en las tablas de contenido de sus contenedores. Para proporcionar esta compatibilidad, controle la restricción PR_ANR en la implementación de [IMAPITable::Restrict](imapitable-restrict.md) realizando un tipo de búsqueda de "mejor suposición", que coincida con una o más propiedades concretas que tienen sentido para su proveedor. Puedes elegir usar la misma propiedad o propiedades cada vez, como **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) o **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)), o permitir que un administrador elija entre una lista de propiedades aceptables. 
  
Aunque la mayoría de los proveedores proporcionan su propia implementación de tabla de contenido, puede personalizar la implementación proporcionada por MAPI a través de la [función CreateTable.](createtable.md) Sin embargo, dado que la implementación MAPI no admite restricciones de ningún tipo, debe crear un objeto contenedor para incluir una versión personalizada de **Restrict** que intercepte la llamada. 
  

