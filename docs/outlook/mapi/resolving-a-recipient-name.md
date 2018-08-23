---
title: Resolver un nombre de destinatario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d9b52edf7f4633fdf9c925a8d8db4953590713b3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22562935"
---
# <a name="resolving-a-recipient-name"></a>Resolver un nombre de destinatario

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando se envía un mensaje, se genera una lista de destinatarios con las propiedades relativas a cada destinatario. En el momento en que se envía el mensaje, una de esas propiedades debe ser el identificador de entrada a largo plazo del destinatario. Para asegurarse de que cada destinatario incluye la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)), pase la estructura [ADRLIST](adrlist.md) que describe la lista de destinatarios en el contenido del parámetro en una llamada a [IAddrBook _lpAdrList_ :: ResolveName](iaddrbook-resolvename.md).
  
 **ResolveName** comienza el procesamiento omitiendo las entradas en la estructura **ADRLIST** que ya se han resuelto, tal como indica la presencia de un identificador de entrada en el correspondiente [ADRENTRY](adrentry.md) de la estructura **SPropValue** matriz. A continuación, **ResolveName** asigna automáticamente los identificadores de entrada único a dos tipos de destinatarios: 
  
- Formato de los destinatarios con una dirección como una dirección de Internet
    
- Los destinatarios con una dirección con el formato siguiente:
    
     `displayname[address type:email address]`
    
Para todas las entradas restantes **ResolveName** busca en la libreta de direcciones para una coincidencia exacta en el nombre para mostrar. **ResolveName** usa la propiedad **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) para determinar el conjunto de contenedores para la búsqueda y el orden de búsqueda. El método [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) de cada contenedor para intentar resolver todos los nombres de llamadas de MAPI. Debido a que algunos contenedores no admiten **ResolveNames**, si el contenedor devuelve MAPI_E_NO_SUPPORT, MAPI aplica una restricción de propiedad **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) frente a su tabla de contenido. Todos los contenedores de la libreta de direcciones son necesarios para admitir la resolución de nombres con esta restricción. Una vez que todos los nombres se resuelven, ninguna otra se realizan las llamadas de contenedor. Si se ha llamado a todos los contenedores, pero permanecen nombres ambiguos o sin resolver, MAPI muestra un cuadro de diálogo si es posible preguntar al usuario para resolver los nombres restantes.
  
La restricción de **PR_ANR** coincide con el valor de la propiedad **PR_ANR** con el nombre para mostrar en la estructura **ADRLIST** . Limitar la vista de tabla de contenido de un contenedor con la restricción de propiedad **PR_ANR** hace que el proveedor de libreta de direcciones para llevar a cabo un tipo "mejor adivinar" de búsqueda, comparación con la propiedad que tenga sentido para el proveedor. Por ejemplo, un proveedor de libreta de direcciones siempre es posible que coinciden con los nombres en la lista de destinatarios contra **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) mientras que otra podría permitir a un administrador seleccionar la propiedad.
  
 **Para establecer una restricción de propiedad PR_ANR en la tabla de contenido de un contenedor de la libreta de direcciones**
  
1. Crear una estructura de [SRestriction](srestriction.md) tal como se muestra en el siguiente código: 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. Llame al método [IMAPITable:: Restrict](imapitable-restrict.md) de la tabla, pasando la estructura **SRestriction** como el parámetro _lpRestriction_ del contenido. 
    

