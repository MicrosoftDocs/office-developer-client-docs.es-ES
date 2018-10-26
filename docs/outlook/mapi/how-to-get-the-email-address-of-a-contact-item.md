---
title: Obtener la dirección de correo electrónico de un elemento de contacto
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 032f7242-5500-1e21-06d3-b2d947eb1043
description: 'Última modificación: 25 de junio de 2012'
ms.openlocfilehash: f9c6766c934632a83fa0388ac2bc4c2c397eead6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575556"
---
# <a name="get-the-email-address-of-a-contact-item"></a><span data-ttu-id="6e98f-103">Obtener la dirección de correo electrónico de un elemento de contacto</span><span class="sxs-lookup"><span data-stu-id="6e98f-103">Get the email address of a Contact item</span></span>

<span data-ttu-id="6e98f-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e98f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e98f-105">En este tema se muestra cómo obtener el valor de una propiedad con nombre que representa la dirección de correo electrónico de un elemento de Microsoft Outlook 2010 o Microsoft Outlook 2013 contacto.</span><span class="sxs-lookup"><span data-stu-id="6e98f-105">This topic shows how to obtain the value of a named property that represents the email address of an Microsoft Outlook 2010 or Microsoft Outlook 2013 Contact item.</span></span>
  
<span data-ttu-id="6e98f-106">Puede asociar hasta tres direcciones de correo electrónico con un elemento de contacto en Outlook 2010 y Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="6e98f-106">You can associate up to three email addresses with a Contact item in Outlook 2010 and Outlook 2013.</span></span> <span data-ttu-id="6e98f-107">Cada dirección de correo electrónico corresponde a una propiedad del objeto de Outlook 2010 o Outlook 2013 **ContactItem** en los modelos de objetos de Outlook 2010 y Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="6e98f-107">Each email address corresponds to a property of the Outlook 2010 or Outlook 2013 **ContactItem** object in the Outlook 2010 and Outlook 2013 object models.</span></span> <span data-ttu-id="6e98f-108">Interna para Outlook 2010 y Outlook 2013, la dirección de correo electrónico también corresponde a una propiedad con nombre de MAPI.</span><span class="sxs-lookup"><span data-stu-id="6e98f-108">Internal to Outlook 2010 and Outlook 2013, the email address also corresponds to a MAPI named property.</span></span> <span data-ttu-id="6e98f-109">Por ejemplo, la primera dirección de correo electrónico de un contacto corresponde a la propiedad **Email1Address** del **objeto ContactItem** en los modelos de objetos de Outlook 2010 y Outlook 2013 y el [de con nombre interno de Outlook 2010 y Outlook 2013 Propiedad canónico PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="6e98f-109">For example, the first email address of a contact corresponds to the **Email1Address** property of the **ContactItem** in the Outlook 2010 and Outlook 2013 object models, and the Outlook 2010 and Outlook 2013 internal named [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md).</span></span>
  
<span data-ttu-id="6e98f-110">Para obtener el valor de una dirección de correo electrónico de un elemento de contacto, puede usar el objeto **PropertyAccessor** del modelo de objetos de Outlook 2010 o 2013 de Outlook o, en primer lugar utilice [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener la etiqueta de propiedad de la propiedad con nombre y, a continuación, Especifique esta etiqueta de propiedad en [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener el valor.</span><span class="sxs-lookup"><span data-stu-id="6e98f-110">To obtain the value of an email address of a contact item, you can use the **PropertyAccessor** object of the Outlook 2010 or Outlook 2013 object model, or first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag of the named property, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="6e98f-111">Cuando se llama a **IMAPIProp::GetIDsFromNames**, especifique los valores apropiados para la estructura [MAPINAMEID](mapinameid.md) señalado por el parámetro de entrada _lppPropNames_.</span><span class="sxs-lookup"><span data-stu-id="6e98f-111">When calling **IMAPIProp::GetIDsFromNames**, specify the appropriate values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_.</span></span> <span data-ttu-id="6e98f-112">El ejemplo de código siguiente muestra cómo obtener la primera dirección de correo electrónico de un contacto determinado, `lpContact`, utilizando **a GetIDsFromNames** y **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="6e98f-112">The following code sample shows how to obtain the first email address of a specified contact,  `lpContact`, using **GetIDsFromNames** and **GetProps**.</span></span> 
  
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


