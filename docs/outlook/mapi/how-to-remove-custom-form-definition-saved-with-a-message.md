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
# <a name="remove-custom-form-definition-saved-with-a-message"></a>Quitar la definición de formulario personalizada que se guarda con un mensaje
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En este tema se muestra un ejemplo de código en C++ que convierte un mensaje que se ha guardado con una definición de formulario personalizado en un mensaje normal sin la definición de formulario.
  
En Microsoft Outlook 2010 o Microsoft Outlook 2013, puede compartir formularios que contienen páginas de formulario personalizadas publicándolo en una biblioteca de formularios o guardando la definición de formulario correspondiente con un mensaje. Un formulario personalizado guardado con un mensaje normalmente se conoce como un "formulario de uso único", ya que el formulario solo se comparte para ver ese mensaje específico como una instancia única. Esto suele hacerse cuando el formulario no se publica en una biblioteca de formularios, pero desea que el destinatario use el formulario personalizado al abrir el elemento. Puede especificar que un formulario es de uso único en el diseñador de formularios, activando la casilla de verificación **enviar la definición del formulario con el elemento** de la página de **propiedades** del formulario. 
  
Los formularios que contienen páginas de formulario se pueden personalizar con código en Visual Basic Scripting Edition (VBScript). Los mensajes que se guardan con definiciones de formulario suelen tener un tamaño mayor. Por motivos de seguridad y almacenamiento, Outlook 2010 y Outlook 2013 ignoran las definiciones de formulario guardadas con cualquier elemento.
  
Para convertir un mensaje que se ha guardado con una definición de formulario personalizado en uno sin, debe quitar cuatro propiedades con nombre:
  
- [Propiedad can�nico de PidLidFormStorage](pidlidformstorage-canonical-property.md)
    
- [Propiedad can�nico de PidLidPageDirStream](pidlidpagedirstream-canonical-property.md)
    
- [Propiedad can�nico de PidLidFormPropStream](pidlidformpropstream-canonical-property.md)
    
- [Propiedad can�nico de PidLidScriptStream](pidlidscriptstream-canonical-property.md)
    
Además, también debe quitar la [propiedad canónica PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) que contiene las definiciones de propiedades personalizadas guardadas con ese mensaje. Un efecto secundario de quitar esta propiedad es que los modelos de objetos de Outlook 2010 u Outlook 2013 y la interfaz de usuario de Outlook 2010 o Outlook 2013 ya no podrán tener acceso a las propiedades de usuario establecidas en el mensaje. Todavía puede obtener acceso a estas propiedades y sus valores a través de MAPI. Tenga en cuenta que si no quita esta propiedad y el mensaje se guarda con otra definición de formulario, la [propiedad canónica PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) se sobrescribe parcialmente con nuevos datos y no se garantiza la integridad de los datos. 
  
Si quita la [propiedad canónica PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md), también debe quitar la marca **INSP_PROPDEFINITION** de la [propiedad canónica PidLidCustomFlag](pidlidcustomflag-canonical-property.md).
  
La siguiente función, `RemoveOneOff`, acepta como parámetros de entrada un puntero a un mensaje y un indicador de si se va a quitar la [propiedad canónica PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md). Mediante el puntero de mensaje, llama a [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener los identificadores de propiedad apropiados y, a continuación, llama a [IMAPIProp::D eleteprops](imapiprop-deleteprops.md) para quitar las propiedades con nombre. También llama a [IMAPIProp:: GetProps](imapiprop-getprops.md) para obtener la [propiedad canónica PidLidCustomFlag](pidlidcustomflag-canonical-property.md) y borra la marca **ONEOFFFLAGS\_INSP** y **INSP_PROPDEFINITION** según corresponda de esa propiedad, para que Outlook 2010 y Outlook 2013 no buscará las propiedades con nombre que se han quitado. 
  
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

## <a name="see-also"></a>Vea también

- [Constantes MAPI](mapi-constants.md)

