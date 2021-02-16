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
  
Cuando se trata un mensaje, se construye una lista de destinatarios con propiedades relacionadas con cada destinatario. Cuando se envía el mensaje, una de estas propiedades debe ser el identificador de entrada a largo plazo del destinatario. Para asegurarse de que cada destinatario incluye la propiedad **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), pase la estructura [ADRLIST](adrlist.md) que describe la lista de destinatarios en el contenido del parámetro  _lpAdrList_ en una llamada a [IAddrBook::ResolveName](iaddrbook-resolvename.md).
  
 **ResolveName** comienza el procesamiento ignorando las entradas de la estructura **ADRLIST** que ya se han resuelto, como se indica por la presencia de un identificador de entrada en la matriz **SPropValue** de la estructura [ADRENTRY](adrentry.md) correspondiente. A **continuación, ResolveName** asigna automáticamente identificadores de entrada de uso único a dos tipos de destinatarios: 
  
- Destinatarios con una dirección con formato de dirección de Internet
    
- Destinatarios con una dirección con el formato siguiente:
    
     `displayname[address type:email address]`
    
Para todas las entradas restantes, **ResolveName** busca en la libreta de direcciones una coincidencia exacta en el nombre para mostrar. **ResolveName** usa la **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) para determinar el conjunto de contenedores que se buscarán y el orden de búsqueda. MAPI llama al [método IABContainer::ResolveNames](iabcontainer-resolvenames.md) de cada contenedor para intentar resolver todos los nombres. Dado que algunos **contenedores no admiten ResolveNames**, si el contenedor devuelve MAPI_E_NO_SUPPORT, MAPI aplica una restricción de propiedad **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) a su tabla de contenido. Todos los contenedores de libreta de direcciones son necesarios para admitir la resolución de nombres con esta restricción. Una vez resueltos todos los nombres, no se realizan más llamadas de contenedor. Si se ha llamado a todos los contenedores, pero los nombres ambiguos o no resueltos permanecen, MAPI muestra un cuadro de diálogo si es posible para solicitar al usuario que resuelva los nombres restantes.
  
La **PR_ANR** coincide con el valor de **la propiedad PR_ANR** con el nombre para mostrar de la estructura **ADRLIST.** La limitación de la vista de la tabla de contenido de un contenedor con la restricción de propiedad **PR_ANR** hace que el proveedor de libreta de direcciones realice un tipo de búsqueda de "mejor suposición", que coincida con la propiedad que tiene sentido para el proveedor. Por ejemplo, un proveedor de libreta de direcciones siempre puede hacer coincidir los nombres de la lista de destinatarios con **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) mientras que otro puede permitir que un administrador seleccione la propiedad.
  
 **Para establecer una restricción PR_ANR propiedad en la tabla de contenido de un contenedor de libreta de direcciones**
  
1. Cree una [estructura SRestriction](srestriction.md) como se muestra en el siguiente código: 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. Llame al método [IMAPITable::Restrict](imapitable-restrict.md) de la tabla de contenido y pase la estructura **SRestriction** como parámetro _lpRestriction._ 
    

