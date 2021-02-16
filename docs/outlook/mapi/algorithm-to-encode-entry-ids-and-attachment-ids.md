---
title: Algoritmo para codificar identificadores de entrada e identificadores de datos adjuntos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b9ae6679-99b7-6509-74d4-12aa13d54928
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6c39fe513be122f265fdc316629a3e64a156fdc1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420139"
---
# <a name="algorithm-to-encode-entry-ids-and-attachment-ids"></a>Algoritmo para codificar identificadores de entrada e identificadores de datos adjuntos

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un proveedor de almacén puede enviar como parte de un localizador uniforme de recursos (URL) mapi un identificador de entrada y un identificador de datos adjuntos al controlador de protocolo MAPI para identificar un objeto que está listo para la indización. El proveedor del almacén codifica el identificador de entrada y el identificador de datos adjuntos como cadenas Unicode. En este tema se muestra un algoritmo que genera una representación compacta del identificador de entrada o el identificador de datos adjuntos.
  
```cpp
const WORD kwBaseOffset = 0xAC00;  // Hangul char range (AC00-D7AF) 
LPWSTR EncodeID(ULONG cbEID, LPENTRYID rgbID) 
{ 
    ULONG   i = 0; 
    LPWSTR  pwzDst = NULL; 
    LPBYTE  pbSrc = NULL; 
    LPWSTR  pwzIDEncoded = NULL; 
 
    // rgbID is the item Entry ID or the attachment ID 
    // cbID is the size in bytes of rgbID 
 
    // Allocate memory for pwzIDEncoded 
    pwzIDEncoded = new WCHAR[cbEID]; 
    if (!pwzIDEncoded) return NULL; 
 
    for (i = 0, pbSrc = (LPBYTE)rgbID, pwzDst = pwzIDEncoded; 
        i < cbEID; 
        i++, pbSrc++, pwzDst++) 
    { 
        *pwzDst = (WCHAR) (*pbSrc + kwBaseOffset); 
    } 
 
    // Ensure NULL terminated 
    *pwzDst = L'\0'; 
 
    // pwzIDEncoded now contains the entry ID encoded. 
    return pwzIDEncoded; 
}
```

## <a name="see-also"></a>Consulte también



[Acerca Notification-Based indexación de la Tienda](about-notification-based-store-indexing.md)
  
[Acerca de las direcciones URL MAPI Notification-Based indexación](about-mapi-urls-for-notification-based-indexing.md)

