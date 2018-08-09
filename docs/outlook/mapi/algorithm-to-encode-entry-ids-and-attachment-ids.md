---
title: Algoritmo para codificar identificadores de entrada y de datos adjuntos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b9ae6679-99b7-6509-74d4-12aa13d54928
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 710ba5173dcce6e948e1f49c7d82e46bc83b8200
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816431"
---
# <a name="algorithm-to-encode-entry-ids-and-attachment-ids"></a>Algoritmo para codificar identificadores de entrada y de datos adjuntos

  
  
**Hace referencia a**: Outlook 
  
Un proveedor de almacén puede enviar como parte de un localizador de recursos uniforme (URL) de MAPI un identificador de entrada y un identificador de datos adjuntos para el controlador de protocolo MAPI para identificar un objeto que está listo para la indización. El proveedor de almacenamiento codifica la entrada de identificador y el identificador de datos adjuntos como cadenas Unicode. En este tema se muestra un algoritmo que genera una representación compacta del identificador de entrada o el identificador de datos adjuntos
  
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

## <a name="see-also"></a>Vea también



[Información sobre la indexación de almacenes basada en notificaciones](about-notification-based-store-indexing.md)
  
[Información sobre las direcciones URL de MAPI para la indexación basada en notificaciones](about-mapi-urls-for-notification-based-indexing.md)

