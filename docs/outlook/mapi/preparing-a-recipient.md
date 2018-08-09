---
title: Preparar un destinatario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9573f10c-66e1-4e87-93f0-89687e906b8b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 51241009262471bf30f7d71e3108b896bbce8df7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820437"
---
# <a name="preparing-a-recipient"></a>Preparar un destinatario

  
  
**Hace referencia a**: Outlook 
  
Una aplicación cliente prepara a los destinatarios mediante la conversión de sus identificadores de entrada a corto plazo a los identificadores de entrada a largo plazo y, posiblemente, agregar, cambiar o reordenación de propiedades. Puede preparar los destinatarios que forman parte de una lista de destinatarios para un mensaje o los destinatarios que no están relacionados con un mensaje. Normalmente, los clientes llaman [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) directamente para convertir los identificadores de entrada a corto plazo en los identificadores de entrada a largo plazo para los destinatarios que se incluyen en el cuadro de diálogo dirección comunes. Para los destinatarios que están asociados con un mensaje saliente, la preparación del destinatario se administra mediante el proceso de resolución de nombres. 
  
Para preparar una lista de destinatarios, llame a **IAddrBook::PrepareRecips**. **PrepareRecips** acepta una estructura de [ADRLIST](adrlist.md) y una lista de etiquetas de propiedad. La estructura **ADRLIST** contiene los destinatarios para estar preparado mientras la lista de etiquetas de propiedad representa las propiedades que debe admitir cada destinatario. **PrepareRecips** intenta colocar las propiedades que se incluyen en la lista de etiquetas de propiedad al principio de la estructura **ADRLIST** . Si cualquiera de las propiedades en la lista faltan de la estructura **ADRLIST** , MAPI llama al proveedor de la libreta de direcciones para proporcionar ellos. Si sólo necesita comprobar si los identificadores de entrada a largo plazo, pase NULL para el parámetro _lpSPropTagArray_ . 
  
Por ejemplo, suponga que trabaja con cinco destinatarios. Todos los destinatarios de cinco aparecen en la estructura **ADRLIST** con las propiedades siguientes en el orden siguiente: 
  
1. **Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
2. **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
3. **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
4. **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
5. **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
Otras tres propiedades se incluyen en la estructura **ADRLIST** para los dos primeros destinatarios. 
  
1. **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))
    
2. **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))
    
3. **PR_SURNAME** ([Pidtagsurname MAPI](pidtagsurname-canonical-property.md))
    
Dado que todos los destinatarios necesitan tener como sus tres primeros propiedades **PR_ADDRTYPE**, **entrada del objeto**y **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), cree una matriz de etiqueta de propiedad con estas propiedades y pase se y la estructura **ADRLIST** a **PrepareRecips**. **PrepareRecips** llama al método **IMAPIProp::GetProps** de cada destinatario para recuperar **PR_HOME_TELEPHONE_NUMBER** debido a que actualmente no es parte de la estructura **ADRLIST** . Cuando se devuelve **PrepareRecips** , la lista de destinatarios representa una lista combinada de los destinatarios con las propiedades incluidas en la estructura **ADRLIST** que aparezcan en primer lugar para cada destinatario. 
  
La lista de destinatarios para los destinatarios 1 y 2 incluye propiedades en el orden siguiente:
  
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
    
Como alternativa a llamar al método **IAddrBook::PrepareRecips** para trabajar con las propiedades, llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) de cada destinatario y, si es necesario, su método [IMAPIProp::SetProps](imapiprop-setprops.md) . Cuando un solo destinatario está implicado, cualquiera de estas técnicas sea satisfactoria. Sin embargo, cuando son necesarios para varios destinatarios, al llamar a **PrepareRecips** en lugar de los métodos de **IMAPIProp** ahorra tiempo y, si está trabajando de forma remota, todas las llamadas a procedimiento remoto. **PrepareRecips** procesa a todos los destinatarios en una sola llamada mientras que **GetProps** y **SetProps** realizar una llamada para cada destinatario. 
  

