---
title: Algoritmo para codificar identificadores de entrada y de datos adJuntos
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
# <a name="algorithm-to-encode-entry-ids-and-attachment-ids"></a><span data-ttu-id="d8a21-103">Algoritmo para codificar identificadores de entrada y de datos adJuntos</span><span class="sxs-lookup"><span data-stu-id="d8a21-103">Algorithm to Encode Entry IDs and Attachment IDs</span></span>

  
  
<span data-ttu-id="d8a21-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8a21-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8a21-105">Un proveedor de almacenamiento puede enviar como parte de un localizador uniforme de recursos (URL) de MAPI, un identificador de entrada y un identificador de datos adjuntos al controlador del protocolo MAPI para identificar un objeto que está listo para la indización.</span><span class="sxs-lookup"><span data-stu-id="d8a21-105">A store provider can send as part of a MAPI Uniform Resource Locator (URL) an entry ID and an attachment ID to the MAPI Protocol Handler to identify an object that is ready for indexing.</span></span> <span data-ttu-id="d8a21-106">El proveedor de almacenamiento codifica el identificador de entrada y el identificador de datos adjuntos como cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="d8a21-106">The store provider encodes the entry ID and attachment ID as Unicode strings.</span></span> <span data-ttu-id="d8a21-107">En este tema se muestra un algoritmo que genera una representación compacta del identificador de entrada o el identificador de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="d8a21-107">This topic shows an algorithm that generates a compact representation of the entry ID or attachment ID.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="d8a21-108">Ver también</span><span class="sxs-lookup"><span data-stu-id="d8a21-108">See also</span></span>



[<span data-ttu-id="d8a21-109">Acerca de la indización de almacén basada en notificaciones</span><span class="sxs-lookup"><span data-stu-id="d8a21-109">About Notification-Based Store Indexing</span></span>](about-notification-based-store-indexing.md)
  
[<span data-ttu-id="d8a21-110">Acerca de las direcciones URL MAPI para la indización basada en notificaciones</span><span class="sxs-lookup"><span data-stu-id="d8a21-110">About MAPI URLs for Notification-Based Indexing</span></span>](about-mapi-urls-for-notification-based-indexing.md)

