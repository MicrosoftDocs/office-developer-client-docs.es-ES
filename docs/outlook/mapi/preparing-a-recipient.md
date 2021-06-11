---
title: Preparación de un destinatario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9573f10c-66e1-4e87-93f0-89687e906b8b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bb6bc8b8d0199ab07d5dad353dbc25da240593e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419880"
---
# <a name="preparing-a-recipient"></a>Preparación de un destinatario

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una aplicación cliente prepara a los destinatarios convirtiendo sus identificadores de entrada a corto plazo en identificadores de entrada a largo plazo y posiblemente agregando, cambiando o reordenando propiedades. Puede preparar destinatarios que forman parte de una lista de destinatarios para un mensaje o destinatarios que no están relacionados con un mensaje. Normalmente, los clientes llaman a [IAddrBook::P repareRecips](iaddrbook-preparerecips.md) directamente para traducir los identificadores de entrada a corto plazo en identificadores de entrada a largo plazo para los destinatarios que se incluyen en el cuadro de diálogo de direcciones comunes. Para los destinatarios asociados con un mensaje saliente, la preparación del destinatario se controla mediante el proceso de resolución de nombres. 
  
Para preparar una lista de destinatarios, llame a **IAddrBook::P repareRecips**. **PrepareRecips** acepta una estructura [ADRLIST](adrlist.md) y una lista de etiquetas de propiedades. La **estructura ADRLIST** contiene los destinatarios que se deben preparar mientras que la lista de etiquetas de propiedades representa las propiedades que cada destinatario debe admitir. **PrepareRecips intenta** colocar las propiedades que se incluyen en la lista de etiquetas de propiedades al principio de la **estructura ADRLIST.** Si falta alguna de las propiedades de la lista de la estructura **ADRLIST,** MAPI llama al proveedor de libreta de direcciones para suministrarlas. Si solo necesita comprobar si hay identificadores de entrada a largo plazo, pase NULL para el parámetro _lpSPropTagArray._ 
  
Por ejemplo, supongamos que está trabajando con cinco destinatarios. Los cinco destinatarios aparecen en la estructura **ADRLIST** con las siguientes propiedades en el orden siguiente: 
  
1. **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
2. **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
3. **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
4. **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
5. **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
Otras tres propiedades se incluyen en la estructura **ADRLIST** para los dos primeros destinatarios. 
  
1. **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))
    
2. **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))
    
3. **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))
    
Dado que todos los destinatarios deben tener como sus tres primeras propiedades **PR_ADDRTYPE**, **PR_ENTRYID** y **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), cree una matriz de etiquetas de propiedad con estas propiedades y pásala y la estructura **ADRLIST** a **PrepareRecips**. **PrepareRecips llama** al método **IMAPIProp::GetProps**  de cada destinatario para recuperar PR_HOME_TELEPHONE_NUMBER porque actualmente no forma parte de la **estructura ADRLIST.** Cuando **PrepareRecips** devuelve, la lista de destinatarios representa una lista combinada de destinatarios con las propiedades incluidas en la estructura **ADRLIST** que aparecen primero para cada destinatario. 
  
La lista de destinatarios de los destinatarios 1 y 2 incluye propiedades en el siguiente orden:
  
1. **PR_ADDRTYPE**
    
2. **PR_ENTRYID**
    
3. **PR_HOME_TELEPHONE_NUMBER**
    
4. **PR_DISPLAY_NAME**
    
5. **PR_SEARCH_KEY**
    
6. **PR_EMAIL_ADDRESS**
    
7. **PR_ADDRTYPE**
    
8. **PR_ACCOUNT**
    
9. **PR_GIVEN_NAME**
    
10. **PR_SURNAME**
    
La lista de destinatarios de los destinatarios 3, 4 y 5 incluye propiedades en el siguiente orden:
  
1. **PR_ADDRTYPE**
    
2. **PR_ENTRYID**
    
3. **PR_HOME_TELEPHONE_NUMBER**
    
4. **PR_DISPLAY_NAME**
    
5. **PR_SEARCH_KEY**
    
6. **PR_EMAIL_ADDRESS**
    
7. **PR_ADDRTYPE**
    
Como alternativa a llamar a **IAddrBook::P repareRecips** para trabajar con propiedades, llama al método [IMAPIProp::GetProps](imapiprop-getprops.md) de cada destinatario y, si es necesario, a [su método IMAPIProp::SetProps.](imapiprop-setprops.md) Cuando solo hay un destinatario implicado, cualquiera de las dos técnicas es satisfactoria. Sin embargo, cuando hay varios destinatarios implicados, llamar a **PrepareRecips** en lugar de los métodos **IMAPIProp** ahorra tiempo y, si está operando de forma remota, muchas llamadas a procedimientos remotos. **PrepareRecips procesa** todos los destinatarios en una sola llamada, mientras que **GetProps** y **SetProps** hacen una llamada para cada destinatario. 
  

