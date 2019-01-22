---
title: TCHAR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- MAPI.TCHAR
api_type:
- COM
ms.assetid: 7a92060b-4c30-4eba-993f-36f5f9231a4b
description: 'Última modificación: 23 de julio de 2011'
localization_priority: Priority
ms.openlocfilehash: 2b04ebe6d05cd72a59fe6d44c9138468fd7ddec1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710450"
---
# <a name="tchar"></a><span data-ttu-id="5ca23-103">TCHAR</span><span class="sxs-lookup"><span data-stu-id="5ca23-103">TCHAR</span></span>

  
  
<span data-ttu-id="5ca23-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ca23-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ca23-105">Una cadena de caracteres Win32 que puede usarse para describir las cadenas DBCS, ANSI o Unicode.</span><span class="sxs-lookup"><span data-stu-id="5ca23-105">A Win32 character string that can be used to describe ANSI, DBCS, or Unicode strings.</span></span> <span data-ttu-id="5ca23-106">Para las plataformas ANSI y DBCS, TCHAR se define como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="5ca23-106">For ANSI and DBCS platforms, TCHAR is defined as follows:</span></span>
  
```cpp
typedef char TCHAR;

```

## <a name="remarks"></a><span data-ttu-id="5ca23-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ca23-107">Remarks</span></span>

<span data-ttu-id="5ca23-108">Para las plataformas Unicode, TCHAR se define como sinónimo de tipo WCHAR.</span><span class="sxs-lookup"><span data-stu-id="5ca23-108">For Unicode platforms, TCHAR is defined as synonymous with the WCHAR type.</span></span> 
  
<span data-ttu-id="5ca23-109">Los clientes MAPI pueden usar el tipo de datos TCHAR para representar una cadena de tipo WCHAR o char.</span><span class="sxs-lookup"><span data-stu-id="5ca23-109">MAPI clients can use the TCHAR data type to represent a string of either the WCHAR or char type.</span></span> <span data-ttu-id="5ca23-110">Asegúrese de definir la constante simbólica UNICODE y de limitar la plataforma cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="5ca23-110">Be sure to define the symbolic constant UNICODE and limit the platform when it is required.</span></span> <span data-ttu-id="5ca23-111">MAPI interpretará la información de la plataforma y traducirá TCHAR a la cadena apropiada de manera interna.</span><span class="sxs-lookup"><span data-stu-id="5ca23-111">MAPI will interpret the platform information and internally translate TCHAR to the appropriate string.</span></span> <span data-ttu-id="5ca23-112">El tipo de propiedad MAPI, PT_TSTRING, funciona igual que el tipo de datos TCHAR.</span><span class="sxs-lookup"><span data-stu-id="5ca23-112">The MAPI property type, PT_TSTRING, works just like the TCHAR data type.</span></span> <span data-ttu-id="5ca23-113">Cuando la plataforma admite Unicode, a las propiedades de tipo PT_TSTRING se les asigna el tipo PT_UNICODE a la hora de la compilación.</span><span class="sxs-lookup"><span data-stu-id="5ca23-113">When the platform supports Unicode, properties of type PT_TSTRING are assigned the type PT_UNICODE at compile time.</span></span> <span data-ttu-id="5ca23-114">Cuando la plataforma no admite Unicode, a estas propiedades se les asigna el tipo PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="5ca23-114">When the platform does not support Unicode, these properties are assigned the type PT_STRING8.</span></span>
  
<span data-ttu-id="5ca23-115">Para más información sobre esta funcionalidad, consulte [Juegos de caracteres](mapi-character-sets.md) y [Lista de tipos de propiedad](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="5ca23-115">For more information about this functionality, see [Character Sets](mapi-character-sets.md) and [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5ca23-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ca23-116">See also</span></span>



[<span data-ttu-id="5ca23-117">Tipos de datos MAPI</span><span class="sxs-lookup"><span data-stu-id="5ca23-117">MAPI Data Types</span></span>](mapi-data-types.md)

