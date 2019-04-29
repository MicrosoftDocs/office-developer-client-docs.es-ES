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
  
Una aplicación cliente prepara a los destinatarios convirtiendo sus identificadores de entrada a corto plazo en identificadores de entrada a largo plazo y posiblemente agregando, cambiando o reordenando propiedades. Puede preparar a los destinatarios que forman parte de una lista de destinatarios para un mensaje o destinatarios que no están relacionados con un mensaje. Normalmente, los clientes llaman a [IAddrBook::P reparerecips](iaddrbook-preparerecips.md) directamente para convertir los identificadores de entrada a corto plazo en identificadores de entrada a largo plazo para los destinatarios que se incluyen en el cuadro de diálogo Dirección común. Para los destinatarios asociados a un mensaje saliente, la preparación del destinatario se controla mediante el proceso de resolución de nombres. 
  
Para preparar una lista de destinatarios, llame a **IAddrBook::P reparerecips**. **PrepareRecips** acepta una estructura [ADRLIST](adrlist.md) y una lista de etiquetas de propiedad. La estructura **ADRLIST** contiene los destinatarios que se van a preparar, mientras que la lista de etiquetas de propiedades representa las propiedades que debe admitir cada destinatario. **PrepareRecips** intenta situar las propiedades que se incluyen en la lista de etiquetas de propiedad al principio de la estructura **ADRLIST** . Si alguna de las propiedades de la lista falta en la estructura **ADRLIST** , MAPI llama al proveedor de la libreta de direcciones para proporcionarlas. Si solo necesita comprobar los identificadores de entrada a largo plazo, pase NULL para el parámetro _lpSPropTagArray_ . 
  
Por ejemplo, supongamos que está trabajando con cinco destinatarios. Los cinco destinatarios aparecen en la estructura **ADRLIST** con las propiedades siguientes en el orden siguiente: 
  
1. **** Es ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
2. **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
3. **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
4. **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
5. **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
Se incluyen otras tres propiedades en la estructura **ADRLIST** para los dos primeros destinatarios. 
  
1. **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))
    
2. **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))
    
3. **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))
    
Como es necesario que todos los destinatarios tengan las tres primeras propiedades **PR_ADDRTYPE**, **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), cree una matriz de etiquetas de propiedad con estas propiedades y pase **** y la estructura **ADRLIST** a **PrepareRecips**. **PrepareRecips** llama al método **IMAPIProp:: GetProps** de cada destinatario para recuperar **PR_HOME_TELEPHONE_NUMBER** porque no forma parte actualmente de la estructura **ADRLIST** . Cuando **PrepareRecips** devuelve, la lista de destinatarios representa una lista combinada de destinatarios con las propiedades incluidas en la estructura **ADRLIST** que aparecen primero para cada destinatario. 
  
La lista de destinatarios de los destinatarios 1 y 2 incluye propiedades en el orden siguiente:
  
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
    
La lista de destinatarios para los destinatarios 3, 4 y 5 incluye propiedades en el orden siguiente:
  
1. **PR_ADDRTYPE**
    
2. **PR_ENTRYID**
    
3. **PR_HOME_TELEPHONE_NUMBER**
    
4. **PR_DISPLAY_NAME**
    
5. **PR_SEARCH_KEY**
    
6. **PR_EMAIL_ADDRESS**
    
7. **PR_ADDRTYPE**
    
Como alternativa a llamar a **IAddrBook::P reparerecips** para trabajar con propiedades, llame al método [IMAPIProp:: GetProps](imapiprop-getprops.md) de cada uno de los destinatarios y, si es necesario, su método [IMAPIProp:: SetProps](imapiprop-setprops.md) . Cuando sólo interviene un destinatario, cualquier técnica es satisfactoria. Sin embargo, cuando hay varios destinatarios implicados, llamar a **PrepareRecips** en lugar de a los métodos **IMAPIProp** ahorra tiempo y, si está operando de forma remota, a muchas llamadas a procedimientos remotos. **PrepareRecips** procesa todos los destinatarios en una sola llamada mientras que **GetProps** y **SetProps** realizan una llamada para cada destinatario. 
  

