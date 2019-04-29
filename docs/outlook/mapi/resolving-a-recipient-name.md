---
title: Resolución de un nombre de destinatario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a3faed3dda2461cab749c824fc97c2074e62375f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405870"
---
# <a name="resolving-a-recipient-name"></a>Resolución de un nombre de destinatario

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando se trata de un mensaje, se crea una lista de destinatarios con las propiedades relacionadas con cada destinatario. En el momento de enviar el mensaje, una de esas propiedades debe ser el identificador de entrada a largo plazo del destinatario. Para asegurarse de que cada uno de **** los destinatarios incluye la propiedad[PidTagEntryId](pidtagentryid-canonical-property.md)), pase la estructura [ADRLIST](adrlist.md) que describe la lista de destinatarios en el contenido del parámetro _lpAdrList_ en una llamada a [IAddrBook:: ResolveName](iaddrbook-resolvename.md).
  
 **ResolveName** comienza el procesamiento pasando por alto las entradas de la estructura **ADRLIST** que ya se han resuelto, tal como indica la presencia de un identificador de entrada en la estructura de [ADRENTRY](adrentry.md) correspondiente **SPropValue** array. A continuación, **ResolveName** asigna automáticamente identificadores de entrada de un solo uso a dos tipos de destinatarios: 
  
- Destinatarios con una dirección con formato de dirección de Internet
    
- Destinatarios con una dirección con el siguiente formato:
    
     `displayname[address type:email address]`
    
Para el resto de las entradas, **ResolveName** busca en la libreta de direcciones una coincidencia exacta en el nombre para mostrar. **ResolveName** usa la propiedad **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) para determinar el conjunto de contenedores para buscar y el orden de búsqueda. MAPI llama al método [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) de cada contenedor para intentar resolver todos los nombres. Debido a que algunos contenedores no admiten **ResolveNames**, si el contenedor devuelve MAPI_E_NO_SUPPORT, MAPI aplica una restricción de propiedad **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) en su tabla de contenido. Todos los contenedores de la libreta de direcciones son necesarios para admitir la resolución de nombres con esta restricción. Una vez que se han resuelto todos los nombres, no se realizan más llamadas de contenedor. Si se ha llamado a todos los contenedores, pero quedan nombres ambiguos o sin resolver, MAPI muestra un cuadro de diálogo, siempre que sea posible, para solicitar al usuario que resuelva los nombres restantes.
  
La restricción **PR_ANR** coincide con el valor de la propiedad **PR_ANR** con el nombre para mostrar de la estructura **ADRLIST** . Limitar la vista de la tabla Contents de un contenedor con la restricción de propiedad **PR_ANR** hace que el proveedor de la libreta de direcciones realice un tipo de búsqueda "mejor estimación", que coincida con la propiedad que tiene sentido para el proveedor. Por ejemplo, un proveedor de libreta de direcciones siempre podría hacer coincidir los nombres de la lista de destinatarios con **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), mientras que otros podrían permitir a un administrador seleccionar la propiedad.
  
 **Para establecer una restricción de propiedad PR_ANR en una tabla de contenido de un contenedor de libretas de direcciones**
  
1. Cree una estructura [SRestriction](srestriction.md) como se muestra en el código siguiente: 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. Llame al método [IMAPITable:: Restrict](imapitable-restrict.md) de la tabla de contenido, pasando la estructura **SRestriction** como el parámetro _lpRestriction_ . 
    

