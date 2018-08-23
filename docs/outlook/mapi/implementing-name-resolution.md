---
title: Implementar la resolución de nombres
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4c71b08-c47a-4421-8603-d5356d32dca9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 489a5888014fa9299b407ebf91759627427b69bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571391"
---
# <a name="implementing-name-resolution"></a>Implementar la resolución de nombres

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de la libreta de direcciones son responsables de admitir la resolución de nombres, el proceso de asociar un identificador de entrada con un nombre para mostrar. Los clientes iniciar la resolución de nombres cuando llama a [IAddrBook::ResolveName](iaddrbook-resolvename.md) para asegurarse de que cada miembro de la lista de destinatarios de un mensaje saliente corresponde a una dirección válida. 
  
Su proveedor puede admitir la resolución de nombres:
  
- Compatibilidad con la restricción de propiedad **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)), un requisito para todos los contenedores de la libreta de direcciones.
    
- Implementación del método [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) , una opción para todos los contenedores de la libreta de direcciones. 
    
Si decide admitir **IABContainer:: ResolveNames**, intenta localizar a una coincidencia exacta para cada nombre para mostrar sin resolver en la estructura [ADRLIST](adrlist.md) pasada con el parámetro _lpAdrList_ . Puede identifiy un nombre para mostrar sin resolver porque falta la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) en la matriz de valores de propiedad en su miembro **aEntries** de la estructura **ADRLIST** . Omitir las entradas que tienen cero propiedades asociadas a ellos. 
  
Notificar el resultado de su intento de resolución en el parámetro _lpFlagList_ , una matriz de marcadores que corresponde a la matriz de nombres para mostrar en _lpAdrList_. Los marcadores son posicionales tal que la primera marca corresponde al primer miembro de **aEntries** en la estructura **ADRLIST** , el segundo indicador se corresponde con el segundo miembro de **aEntries** y así sucesivamente. 
  
Existen tres resultados posibles para cada entrada sin resolver:
  
- Se encontró ninguna coincidencia, lo que significa que ninguna de las entradas en las entradas de contenedor coinciden con la entrada en la estructura **ADRLIST** . Establezca la entrada correspondiente en el parámetro _lpFlagList_ a MAPI_UNRESOLVED. 
    
- Se encontraron varias coincidencias, lo que significa que no hay varias entradas de contenedor que coinciden con la entrada en la estructura **ADRLIST** . Establezca la entrada correspondiente en el parámetro _lpFlagList_ a MAPI_AMBIGUOUS. No cambie el número de entradas en la estructura **ADRLIST** . 
    
- Puede encontrar una coincidencia exacta, lo que significa que no hay entrada sólo un contenedor que coincida con la entrada en la estructura **ADRLIST** . Establecer al miembro correspondiente en el parámetro _lpFlagList_ a MAPI_RESOLVED y agregue el identificador de entrada a la matriz de las propiedades asociadas con la entrada **ADRLIST** . 
    
Si decide no admitir **IABContainer:: ResolveNames**, devolver MAPI_E_NO_SUPPORT de su implementación.
  
Todos los proveedores de libreta de direcciones son necesarios para admitir la resolución de nombres ambiguos: la restricción de propiedad **PR_ANR** : en las tablas de contenido de sus contenedores. Para proporcionar este soporte técnico, controlar la restricción de PR_ANR en su implementación de [IMAPITable:: Restrict](imapitable-restrict.md) mediante la realización de un tipo "mejor adivinar" de búsqueda, comparación con una o más propiedades determinadas que tiene sentido para su proveedor. Puede usar la misma propiedad o las propiedades de cada vez, como **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) o **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)), o permitir que un administrador elegir de una lista de propiedades aceptables. 
  
Aunque la mayoría de los proveedores proporciona su propia implementación de la tabla de contenido, puede personalizar la implementación proporcionada por MAPI a través de la función [CreateTable](createtable.md) . Sin embargo, debido a que la implementación de MAPI no admite restricciones de ningún tipo, debe crear un objeto contenedor para incluir una versión personalizada de **Restrict** que intercepta la llamada. 
  

