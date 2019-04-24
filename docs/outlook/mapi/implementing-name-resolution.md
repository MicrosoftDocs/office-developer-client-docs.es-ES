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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310083"
---
# <a name="implementing-name-resolution"></a>Implementación de la resolución de nombres

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de la libreta de direcciones son responsables de admitir la resolución de nombres: el proceso de asociar un identificador de entrada con un nombre para mostrar. Los clientes inician la resolución de nombres cuando llaman a [IAddrBook:: ResolveName](iaddrbook-resolvename.md) para asegurarse de que cada miembro de la lista de destinatarios de un mensaje saliente se corresponde con una dirección válida. 
  
El proveedor puede admitir la resolución de nombres:
  
- Compatibilidad con la restricción de propiedad **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)), un requisito para todos los contenedores de la libreta de direcciones.
    
- Implementar el método [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) , una opción para todos los contenedores de la libreta de direcciones. 
    
Si decide admitir **IABContainer:: ResolveNames**, intente localizar una coincidencia exacta para cada nombre para mostrar sin resolver en la estructura [ADRLIST](adrlist.md) que se pasa con el parámetro _lpAdrList_ . Puede identificar un nombre para mostrar sin resolver porque falta la propiedad AEntries ([PidTagEntryId](pidtagentryid-canonical-property.md)) en la matriz de valores de propiedad en su **** miembro de la estructura **ADRLIST** . **** Ignore las entradas que tienen asociadas propiedades. 
  
Informe del resultado del intento de resolución en el parámetro _lpFlagList_ , una matriz de marcadores que corresponde a la matriz de nombres para mostrar en _lpAdrList_. Las marcas son posicionales para que el primer indicador se corresponda con el primer miembro **aEntries** de la estructura **ADRLIST** , el segundo indicador se corresponda con el segundo miembro **aEntries** , y así sucesivamente. 
  
Hay tres resultados posibles por cada entrada no resuelta:
  
- No se encontró ninguna coincidencia, lo que significa que ninguna de las entradas de las entradas de contenedor coincide con la entrada de la estructura **ADRLIST** . Establezca la entrada correspondiente en el parámetro _lpFlagList_ en MAPI_UNRESOLVED. 
    
- Se pueden encontrar varias coincidencias, lo que significa que hay varias entradas de contenedor que coinciden con la entrada en la estructura **ADRLIST** . Establezca la entrada correspondiente en el parámetro _lpFlagList_ en MAPI_AMBIGUOUS. No cambie el número de entradas en la estructura **ADRLIST** . 
    
- Se puede encontrar una coincidencia exacta, lo que significa que solo hay una entrada de contenedor que coincida con la entrada en la estructura **ADRLIST** . Establezca el miembro correspondiente en el parámetro _lpFlagList_ en MAPI_RESOLVED y agregue el identificador de entrada a la matriz de propiedades asociada a la entrada **ADRLIST** . 
    
Si decide no admitir **IABContainer:: ResolveNames**, devuelva MAPI_E_NO_SUPPORT de su implementación.
  
Todos los proveedores de la libreta de direcciones deben admitir la resolución de nombres ambiguos (la restricción de propiedad **PR_ANR** ) en las tablas de contenido de los contenedores. Para proporcionar esta compatibilidad, administre la restricción PR_ANR en su implementación de [IMAPITable:: Restrict](imapitable-restrict.md) realizando un tipo de búsqueda "mejor estimación", que coincide con una o más propiedades concretas que tienen sentido para su proveedor. Puede elegir usar la misma propiedad o propiedades cada vez, como **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) o **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)), o permitir que un administrador elija en una lista de propiedades aceptables. 
  
Aunque la mayoría de los proveedores proporcionan su propia implementación de la tabla de contenido, puede personalizar la implementación suministrada por MAPI a través de la función [createTable](createtable.md) . Sin embargo, como la implementación de MAPI no admite restricciones de ningún tipo, debe crear un objeto contenedor para incluir una versión personalizada de **Restrict** que intercepte la llamada. 
  

