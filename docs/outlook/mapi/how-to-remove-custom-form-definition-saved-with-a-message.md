---
title: Quitar la definición de formulario personalizada que se guarda con un mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6a270f0c-104a-84a1-9adf-aea166f89071
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: ac162cb73cfdee83bf034de32064c5ed9df3bc02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345937"
---
# <a name="remove-custom-form-definition-saved-with-a-message"></a><span data-ttu-id="cddd0-103">Quitar la definición de formulario personalizada que se guarda con un mensaje</span><span class="sxs-lookup"><span data-stu-id="cddd0-103">Remove custom form definition saved with a message</span></span>
  
<span data-ttu-id="cddd0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cddd0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cddd0-105">En este tema se muestra un ejemplo de código en C++ que convierte un mensaje que se ha guardado con una definición de formulario personalizado en un mensaje normal sin la definición de formulario.</span><span class="sxs-lookup"><span data-stu-id="cddd0-105">This topic shows a code sample in C++ that converts a message that has been saved with a custom form definition to a regular message without the form definition.</span></span>
  
<span data-ttu-id="cddd0-106">En Microsoft Outlook 2010 o Microsoft Outlook 2013, puede compartir formularios que contienen páginas de formulario personalizadas publicándolo en una biblioteca de formularios o guardando la definición de formulario correspondiente con un mensaje.</span><span class="sxs-lookup"><span data-stu-id="cddd0-106">In Microsoft Outlook 2010 or Microsoft Outlook 2013, you can share forms containing custom form pages by either publishing them to a forms library or saving the corresponding form definition with a message.</span></span> <span data-ttu-id="cddd0-107">Un formulario personalizado guardado con un mensaje normalmente se conoce como un "formulario de uso único", ya que el formulario solo se comparte para ver ese mensaje específico como una instancia única.</span><span class="sxs-lookup"><span data-stu-id="cddd0-107">A custom form saved with a message is commonly referred as a "one-off form", since the form is shared only for viewing that specific message as a one-off instance.</span></span> <span data-ttu-id="cddd0-108">Esto suele hacerse cuando el formulario no se publica en una biblioteca de formularios, pero desea que el destinatario use el formulario personalizado al abrir el elemento.</span><span class="sxs-lookup"><span data-stu-id="cddd0-108">You typically do this when the form is not published in a forms library but you want the recipient to use the custom form when opening the item.</span></span> <span data-ttu-id="cddd0-109">Puede especificar que un formulario es de uso único en el diseñador de formularios, activando la casilla de verificación **enviar la definición del formulario con el elemento** de la página de **propiedades** del formulario.</span><span class="sxs-lookup"><span data-stu-id="cddd0-109">You can specify a form is a one-off in the Forms Designer, by selecting the **Send form definition with item** check box on the **Properties** page of the form.</span></span> 
  
<span data-ttu-id="cddd0-110">Los formularios que contienen páginas de formulario se pueden personalizar con código en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="cddd0-110">Forms containing form pages can be customized with code in Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="cddd0-111">Los mensajes que se guardan con definiciones de formulario suelen tener un tamaño mayor.</span><span class="sxs-lookup"><span data-stu-id="cddd0-111">Messages that are saved with form definitions are generally bigger in size.</span></span> <span data-ttu-id="cddd0-112">Por motivos de seguridad y almacenamiento, Outlook 2010 y Outlook 2013 ignoran las definiciones de formulario guardadas con cualquier elemento.</span><span class="sxs-lookup"><span data-stu-id="cddd0-112">For security and storage reasons, Outlook 2010 and Outlook 2013 ignore form definitions saved with any item.</span></span>
  
<span data-ttu-id="cddd0-113">Para convertir un mensaje que se ha guardado con una definición de formulario personalizado en uno sin, debe quitar cuatro propiedades con nombre:</span><span class="sxs-lookup"><span data-stu-id="cddd0-113">To convert a message that is saved with a custom form definition to one without, you must remove four named properties:</span></span>
  
- [<span data-ttu-id="cddd0-114">Propiedad can�nico de PidLidFormStorage</span><span class="sxs-lookup"><span data-stu-id="cddd0-114">PidLidFormStorage Canonical Property</span></span>](pidlidformstorage-canonical-property.md)
    
- [<span data-ttu-id="cddd0-115">Propiedad can�nico de PidLidPageDirStream</span><span class="sxs-lookup"><span data-stu-id="cddd0-115">PidLidPageDirStream Canonical Property</span></span>](pidlidpagedirstream-canonical-property.md)
    
- [<span data-ttu-id="cddd0-116">Propiedad can�nico de PidLidFormPropStream</span><span class="sxs-lookup"><span data-stu-id="cddd0-116">PidLidFormPropStream Canonical Property</span></span>](pidlidformpropstream-canonical-property.md)
    
- [<span data-ttu-id="cddd0-117">Propiedad can�nico de PidLidScriptStream</span><span class="sxs-lookup"><span data-stu-id="cddd0-117">PidLidScriptStream Canonical Property</span></span>](pidlidscriptstream-canonical-property.md)
    
<span data-ttu-id="cddd0-118">Además, también debe quitar la [propiedad canónica PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) que contiene las definiciones de propiedades personalizadas guardadas con ese mensaje.</span><span class="sxs-lookup"><span data-stu-id="cddd0-118">In addition, you should also remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md) that contains the definitions of custom properties saved with that message.</span></span> <span data-ttu-id="cddd0-119">Un efecto secundario de quitar esta propiedad es que los modelos de objetos de Outlook 2010 u Outlook 2013 y la interfaz de usuario de Outlook 2010 o Outlook 2013 ya no podrán tener acceso a las propiedades de usuario establecidas en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="cddd0-119">A side effect of removing this property is that the Outlook 2010 or Outlook 2013 object models and the Outlook 2010 or Outlook 2013 user interface will no longer be able to access user properties that have been set on the message.</span></span> <span data-ttu-id="cddd0-120">Todavía puede obtener acceso a estas propiedades y sus valores a través de MAPI.</span><span class="sxs-lookup"><span data-stu-id="cddd0-120">You are still able to access these properties and their values through MAPI.</span></span> <span data-ttu-id="cddd0-121">Tenga en cuenta que si no quita esta propiedad y el mensaje se guarda con otra definición de formulario, la [propiedad canónica PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) se sobrescribe parcialmente con nuevos datos y no se garantiza la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="cddd0-121">Note that if you do not remove this property and the message is saved with another form definition, the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md) is partially overwritten with new data and data integrity is not guaranteed.</span></span> 
  
<span data-ttu-id="cddd0-122">Si quita la [propiedad canónica PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md), también debe quitar la marca **INSP_PROPDEFINITION** de la [propiedad canónica PidLidCustomFlag](pidlidcustomflag-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="cddd0-122">If you remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md), then you should also remove the **INSP_PROPDEFINITION** flag from the [PidLidCustomFlag Canonical Property](pidlidcustomflag-canonical-property.md).</span></span>
  
<span data-ttu-id="cddd0-123">La siguiente función, `RemoveOneOff`, acepta como parámetros de entrada un puntero a un mensaje y un indicador de si se va a quitar la [propiedad canónica PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="cddd0-123">The following function,  `RemoveOneOff`, accepts as input parameters a pointer to a message and an indicator whether to remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md).</span></span> <span data-ttu-id="cddd0-124">Mediante el puntero de mensaje, llama a [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener los identificadores de propiedad apropiados y, a continuación, llama a [IMAPIProp::D eleteprops](imapiprop-deleteprops.md) para quitar las propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="cddd0-124">Using the message pointer, it calls [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the appropriate property identifiers, and then calls [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) to remove the named properties.</span></span> <span data-ttu-id="cddd0-125">También llama a [IMAPIProp:: GetProps](imapiprop-getprops.md) para obtener la [propiedad canónica PidLidCustomFlag](pidlidcustomflag-canonical-property.md) y borra la marca **ONEOFFFLAGS\_INSP** y **INSP_PROPDEFINITION** según corresponda de esa propiedad, para que Outlook 2010 y Outlook 2013 no buscará las propiedades con nombre que se han quitado.</span><span class="sxs-lookup"><span data-stu-id="cddd0-125">It also calls [IMAPIProp::GetProps](imapiprop-getprops.md) to get the [PidLidCustomFlag Canonical Property](pidlidcustomflag-canonical-property.md) and clears the **INSP\_ONEOFFFLAGS** flag and **INSP_PROPDEFINITION** flag as appropriate from that property, so that Outlook 2010 and Outlook 2013 will not look for those named properties that have been removed.</span></span> 
  
```cpp
ULONG aulOneOffIDs[] = {dispidFormStorage,  
    dispidPageDirStream, 
    dispidFormPropStream, 
    dispidScriptStream, 
    dispidPropDefStream, // dispidPropDefStream must remain next to last in list 
    dispidCustomFlag};   // dispidCustomFlag must remain last in list 
 
#define ulNumOneOffIDs (sizeof(aulOneOffIDs)/sizeof(aulOneOffIDs[0])) 
 
HRESULT RemoveOneOff(LPMESSAGE lpMessage, BOOL bRemovePropDef) 
{ 
    if (!lpMessage) return MAPI_E_INVALID_PARAMETER; 
     
    HRESULT hRes = S_OK; 
    MAPINAMEID  rgnmid[ulNumOneOffIDs]; 
    LPMAPINAMEID rgpnmid[ulNumOneOffIDs]; 
    LPSPropTagArray lpTags = NULL; 
 
    ULONG i = 0; 
    for (i = 0 ; i < ulNumOneOffIDs ; i++) 
    { 
        rgnmid[i].lpguid = (LPGUID)&PSETID_Common; 
        rgnmid[i].ulKind = MNID_ID; 
        rgnmid[i].Kind.lID = aulOneOffIDs[i]; 
        rgpnmid[i] = &rgnmid[i]; 
    } 
   
    hRes = lpMessage->GetIDsFromNames( 
        ulNumOneOffIDs, 
        rgpnmid, 
        0, 
        &lpTags); 
    if (lpTags) 
    { 
        // The last prop is the flag value  
        // to be updated, don't count it 
        lpTags->cValues = ulNumOneOffIDs-1; 
 
        // If the prop def stream is not to be removed, don't count it 
        if (!bRemovePropDef) 
        { 
          lpTags->cValues = lpTags->cValues-1; 
        } 
 
        hRes = lpMessage->DeleteProps( 
            lpTags, 
            0); 
        if (SUCCEEDED(hRes)) 
        { 
            SPropTagArray pTag = {0}; 
            ULONG cProp = 0; 
            LPSPropValue lpCustomFlag = NULL; 
 
            // Grab dispidCustomFlag, the last tag in the array 
            pTag.cValues = 1; 
            pTag.aulPropTag[0] = CHANGE_PROP_TYPE( 
                lpTags->aulPropTag[ulNumOneOffIDs-1], 
                PT_LONG); 
 
            hRes = lpMessage->GetProps( 
                &pTag, 
                fMapiUnicode, 
                &cProp, 
                &lpCustomFlag); 
            if (SUCCEEDED(hRes) &&  
                1 == cProp && lpCustomFlag &&  
                PT_LONG == PROP_TYPE(lpCustomFlag->ulPropTag)) 
            { 
                // Clear the INSP_ONEOFFFLAGS bits so Outlook  
                // doesn't look for the props that have been deleted 
                lpCustomFlag->Value.l =  
                    lpCustomFlag->Value.l & ~(INSP_ONEOFFFLAGS); 
                if (bRemovePropDef) 
                { 
                    lpCustomFlag->Value.l =  
                        lpCustomFlag->Value.l & ~(INSP_PROPDEFINITION); 
                } 
                hRes = lpMessage->SetProps( 
                    1, 
                    lpCustomFlag, 
                    NULL); 
             } 
 
             hRes = lpMessage->SaveChanges(KEEP_OPEN_READWRITE); 
         } 
    } 
    MAPIFreeBuffer(lpTags); 
 
    return hRes; 
}
```

## <a name="see-also"></a><span data-ttu-id="cddd0-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="cddd0-126">See also</span></span>

- [<span data-ttu-id="cddd0-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="cddd0-127">MAPI Constants</span></span>](mapi-constants.md)

