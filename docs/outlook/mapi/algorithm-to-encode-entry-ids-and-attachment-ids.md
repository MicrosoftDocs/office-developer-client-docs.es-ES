---
title: Algoritmo para codificar identificadores de entrada y de datos adjuntos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b9ae6679-99b7-6509-74d4-12aa13d54928
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4d3ca89ea7d3d72f625d38e37494e253b05b1569
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577922"
---
# <a name="algorithm-to-encode-entry-ids-and-attachment-ids"></a><span data-ttu-id="b2384-103">Algoritmo para codificar identificadores de entrada y de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="b2384-103">Algorithm to Encode Entry IDs and Attachment IDs</span></span>

  
  
<span data-ttu-id="b2384-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2384-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2384-105">Un proveedor de almacén puede enviar como parte de un localizador de recursos uniforme (URL) de MAPI un identificador de entrada y un identificador de datos adjuntos para el controlador de protocolo MAPI para identificar un objeto que está listo para la indización.</span><span class="sxs-lookup"><span data-stu-id="b2384-105">A store provider can send as part of a MAPI Uniform Resource Locator (URL) an entry ID and an attachment ID to the MAPI Protocol Handler to identify an object that is ready for indexing.</span></span> <span data-ttu-id="b2384-106">El proveedor de almacenamiento codifica la entrada de identificador y el identificador de datos adjuntos como cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="b2384-106">The store provider encodes the entry ID and attachment ID as Unicode strings.</span></span> <span data-ttu-id="b2384-107">En este tema se muestra un algoritmo que genera una representación compacta del identificador de entrada o el identificador de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="b2384-107">This topic shows an algorithm that generates a compact representation of the entry ID or attachment ID.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="b2384-108">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="b2384-108">See also</span></span>



[<span data-ttu-id="b2384-109">Información sobre la indexación de almacenes basada en notificaciones</span><span class="sxs-lookup"><span data-stu-id="b2384-109">About Notification-Based Store Indexing</span></span>](about-notification-based-store-indexing.md)
  
[<span data-ttu-id="b2384-110">Información sobre las direcciones URL de MAPI para la indexación basada en notificaciones</span><span class="sxs-lookup"><span data-stu-id="b2384-110">About MAPI URLs for Notification-Based Indexing</span></span>](about-mapi-urls-for-notification-based-indexing.md)

