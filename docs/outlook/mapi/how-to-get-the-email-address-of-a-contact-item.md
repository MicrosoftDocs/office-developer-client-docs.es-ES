---
title: Obtener la dirección de correo electrónico de un elemento de contacto
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 032f7242-5500-1e21-06d3-b2d947eb1043
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: fab09d0c594bac1374973f523abe6ff0b9c09dd0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429596"
---
# <a name="get-the-email-address-of-a-contact-item"></a>Obtener la dirección de correo electrónico de un elemento de contacto

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En este tema se muestra cómo obtener el valor de una propiedad con nombre que representa la dirección de correo electrónico de un elemento de contacto de Microsoft Outlook 2010 o Microsoft Outlook 2013.
  
Puede asociar hasta tres direcciones de correo electrónico con un elemento de contacto en Outlook 2010 y Outlook 2013. Cada dirección de correo electrónico corresponde a una propiedad del objeto de **ContactItem** de Outlook 2010 u Outlook 2013 en los modelos de objetos de Outlook 2010 y Outlook 2013. Interna en Outlook 2010 y Outlook 2013, la dirección de correo electrónico también corresponde a una propiedad con nombre MAPI. Por ejemplo, la primera dirección de correo electrónico de un contacto corresponde a la propiedad **Email1Address** del objeto **ContactItem** en los modelos de objetos outlook 2010 y Outlook 2013, y el nombre [interno de Outlook 2010 y Outlook 2013 Propiedad canónica PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md).
  
Para obtener el valor de una dirección de correo electrónico de un elemento de contacto, puede usar el objeto **PropertyAccessor** del modelo de objetos de Outlook 2010 u Outlook 2013 o, por último, usar [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener la etiqueta de propiedad de la propiedad con nombre y, a continuación, Especifique esta etiqueta de propiedad en [IMAPIProp:: GetProps](imapiprop-getprops.md) para obtener el valor. Al llamar a **IMAPIProp:: GetIDsFromNames**, especifique los valores apropiados para la estructura [MAPINAMEID](mapinameid.md) a la que apunta el parámetro de entrada _lppPropNames_. El siguiente ejemplo de código muestra cómo obtener la primera dirección de correo electrónico de un contacto `lpContact`especificado, mediante **GetIDsFromNames** y **GetProps**. 
  
```cpp
HRESULT HrGetEmail1(LPMESSAGE lpContact) 
{ 
    HRESULT hRes = S_OK; 
    LPSPropTagArray lpNamedPropTags = NULL; 
    MAPINAMEID NamedID = {0}; 
    LPMAPINAMEID lpNamedID = &NamedID; 
    NamedID.lpguid = (LPGUID)&PSETID_Address; 
    NamedID.ulKind = MNID_ID; 
    NamedID.Kind.lID = dispidEmailEmailAddress; 
 
    hRes = lpContact->GetIDsFromNames( 
           1,  
           &lpNamedID,  
           NULL,  
           &lpNamedPropTags); 
 
    if (SUCCEEDED(hRes) && lpNamedPropTags) 
    { 
        SPropTagArray sPropTagArray; 
 
        sPropTagArray.cValues = 1; 
        sPropTagArray.aulPropTag[0] = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[0],PT_STRING8); 
        LPSPropValue lpProps = NULL; 
        ULONG cProps = 0; 
 
        hRes = lpContact->GetProps( 
               &sPropTagArray, 
               NULL, 
               &cProps, 
               &lpProps); 
        if (SUCCEEDED(hRes) &&  
            1 == cProps &&  
            lpProps &&  
            PT_STRING8 == PROP_TYPE(lpProps[0].ulPropTag) && 
            lpProps[0].Value.lpszA) 
        { 
            printf("Email address 1 = \"%s\"\n",lpProps[0].Value.lpszA); 
        } 
        MAPIFreeBuffer(lpProps); 
        MAPIFreeBuffer(lpNamedPropTags); 
     } 
     return hRes; 
}
```


