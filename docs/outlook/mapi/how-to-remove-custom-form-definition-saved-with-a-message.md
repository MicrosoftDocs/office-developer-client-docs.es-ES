---
title: Quitar la definición de formulario personalizada que se guarda con un mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6a270f0c-104a-84a1-9adf-aea166f89071
description: 'Última modificación: 25 de junio de 2012'
ms.openlocfilehash: 4b12824542a1408a364452eb6587122ec66412d3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594456"
---
# <a name="remove-custom-form-definition-saved-with-a-message"></a>Quitar la definición de formulario personalizada que se guarda con un mensaje
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
En este tema se muestra un ejemplo de código en C++ que convierte un mensaje que se ha guardado con una definición de formulario personalizada para un mensaje normal sin la definición del formulario.
  
En Microsoft Outlook 2010 o Microsoft Outlook 2013, puede compartir formularios que contiene páginas de formulario personalizadas publicarlos en una biblioteca de formularios o guardar la definición de formulario correspondiente con un mensaje. Un formulario personalizado que se guarda con un mensaje con frecuencia se conoce como "constituye un formulario", dado que el formulario se comparte sólo para ver ese mensaje específico como una instancia de uso único. Normalmente, hacer esto cuando el formulario no se publica en una biblioteca de formularios, pero desea que el destinatario debe usar el formulario personalizado al abrir el elemento. Puede especificar que un formulario es de uso único en el Diseñador de formularios, mediante la selección de la casilla de verificación **enviar la definición del formulario con el elemento** en la página de **Propiedades** del formulario. 
  
Los formularios que contiene las páginas de formulario se pueden personalizar con código en Visual Basic Scripting Edition (VBScript). Los mensajes que se guardan con definiciones de formulario son generalmente mayores tamaño. Por motivos de almacenamiento y seguridad, Outlook 2010 y Outlook 2013 pasan por alto las definiciones de formularios guardadas con cualquier elemento.
  
Para convertir un mensaje en el que se guarda con una definición de formulario personalizada a uno sin, debe quitar cuatro propiedades con nombre:
  
- [Propiedad canónica PidLidFormStorage](pidlidformstorage-canonical-property.md)
    
- [Propiedad canónica PidLidPageDirStream](pidlidpagedirstream-canonical-property.md)
    
- [Propiedad canónica PidLidFormPropStream](pidlidformpropstream-canonical-property.md)
    
- [Propiedad canónica PidLidScriptStream](pidlidscriptstream-canonical-property.md)
    
Además, también debe quitar la [Propiedad canónico PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) que contiene las definiciones de las propiedades personalizadas que se guarda con ese mensaje. Un efecto secundario de la eliminación de esta propiedad es que los modelos de objetos de Outlook 2010 o Outlook 2013 y la interfaz de usuario de Outlook 2010 o 2013 de Outlook ya no podrán obtener acceso a las propiedades de usuario que se han establecido en el mensaje. Son todavía puede tener acceso a estas propiedades y sus valores a través de MAPI. Tenga en cuenta que si no quite esta propiedad y el mensaje se guarda con otra definición de formulario, la [Propiedad canónico PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) parcialmente se sobrescribe con los nuevos datos y no se garantiza la integridad de los datos. 
  
Si quita la [Propiedad canónico PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md), también debe quitar la marca **INSP_PROPDEFINITION** de la [Propiedad canónico PidLidCustomFlag](pidlidcustomflag-canonical-property.md).
  
La siguiente función, `RemoveOneOff`, acepta como parámetros de entrada de un puntero a un mensaje y un indicador de si desea quitar la [Propiedad canónico PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md). Con el puntero de mensaje, se llama a [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener los identificadores de propiedad correspondiente y, a continuación, llama a [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) para quitar las propiedades con nombre. También llama a [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener la [Propiedad canónico PidLidCustomFlag](pidlidcustomflag-canonical-property.md) y borra el **INSP\_ONEOFFFLAGS** marca y **INSP_PROPDEFINITION** indicador según corresponda de esa propiedad, por lo que Outlook 2010 y Outlook 2013 no buscará para las propiedades con nombre que se han quitado. 
  
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

