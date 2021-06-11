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
# <a name="get-the-email-address-of-a-contact-item"></a><span data-ttu-id="8610b-103">Obtener la dirección de correo electrónico de un elemento de contacto</span><span class="sxs-lookup"><span data-stu-id="8610b-103">Get the email address of a Contact item</span></span>

<span data-ttu-id="8610b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8610b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8610b-105">En este tema se muestra cómo obtener el valor de una propiedad con nombre que representa la dirección de correo electrónico de Microsoft Outlook 2010 o Microsoft Outlook 2013 Elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="8610b-105">This topic shows how to obtain the value of a named property that represents the email address of an Microsoft Outlook 2010 or Microsoft Outlook 2013 Contact item.</span></span>
  
<span data-ttu-id="8610b-106">Puede asociar hasta tres direcciones de correo electrónico con un elemento de contacto en Outlook 2010 y Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="8610b-106">You can associate up to three email addresses with a Contact item in Outlook 2010 and Outlook 2013.</span></span> <span data-ttu-id="8610b-107">Cada dirección de correo electrónico corresponde a una propiedad del objeto **ContactItem** de Outlook 2010 o Outlook 2013 en los modelos de objetos Outlook 2010 y Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="8610b-107">Each email address corresponds to a property of the Outlook 2010 or Outlook 2013 **ContactItem** object in the Outlook 2010 and Outlook 2013 object models.</span></span> <span data-ttu-id="8610b-108">Internal to Outlook 2010 and Outlook 2013, the email address also corresponds to a MAPI named property.</span><span class="sxs-lookup"><span data-stu-id="8610b-108">Internal to Outlook 2010 and Outlook 2013, the email address also corresponds to a MAPI named property.</span></span> <span data-ttu-id="8610b-109">Por ejemplo, la primera dirección de correo electrónico de un contacto corresponde a la propiedad **Email1Address** del **objeto ContactItem** en los modelos de objetos Outlook 2010 y Outlook 2013, y los modelos de objetos Outlook 2010 y Outlook 2013 denominados [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="8610b-109">For example, the first email address of a contact corresponds to the **Email1Address** property of the **ContactItem** in the Outlook 2010 and Outlook 2013 object models, and the Outlook 2010 and Outlook 2013 internal named [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md).</span></span>
  
<span data-ttu-id="8610b-110">Para obtener el valor de una dirección de correo electrónico de un elemento de contacto, puede usar el objeto **PropertyAccessor** del modelo de objetos de Outlook 2010 o Outlook 2013, o usar primero [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener la etiqueta de propiedad de la propiedad con nombre y, a continuación, especificar esta etiqueta de propiedad en [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener el valor.</span><span class="sxs-lookup"><span data-stu-id="8610b-110">To obtain the value of an email address of a contact item, you can use the **PropertyAccessor** object of the Outlook 2010 or Outlook 2013 object model, or first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag of the named property, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="8610b-111">Al llamar **a IMAPIProp::GetIDsFromNames**, especifique los valores adecuados para la estructura [MAPINAMEID](mapinameid.md) apuntada por el parámetro de entrada  _lppPropNames_.</span><span class="sxs-lookup"><span data-stu-id="8610b-111">When calling **IMAPIProp::GetIDsFromNames**, specify the appropriate values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_.</span></span> <span data-ttu-id="8610b-112">En el ejemplo de código siguiente se muestra cómo obtener la primera dirección de correo electrónico de un contacto especificado,  `lpContact` mediante **GetIDsFromNames** y **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="8610b-112">The following code sample shows how to obtain the first email address of a specified contact,  `lpContact`, using **GetIDsFromNames** and **GetProps**.</span></span> 
  
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


