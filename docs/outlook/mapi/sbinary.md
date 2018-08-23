---
title: SBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinary
api_type:
- COM
ms.assetid: f21b5e6c-7a63-46bf-acbf-0e042e3519f7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f54ef96443e5c9fc5fb587f5a9c25388c1ff9cdb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577425"
---
# <a name="sbinary"></a><span data-ttu-id="bb0fd-103">SBinary</span><span class="sxs-lookup"><span data-stu-id="bb0fd-103">SBinary</span></span>

  
  
<span data-ttu-id="bb0fd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb0fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb0fd-105">Describe una propiedad de tipo PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="bb0fd-105">Describes a property of type PT_BINARY.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bb0fd-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="bb0fd-106">Header file:</span></span>  <br/> |<span data-ttu-id="bb0fd-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bb0fd-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinary
{
  ULONG      cb;
  LPBYTE     lpb;
} SBinary, FAR *LPSBinary;

```

## <a name="members"></a><span data-ttu-id="bb0fd-108">Members</span><span class="sxs-lookup"><span data-stu-id="bb0fd-108">Members</span></span>

 <span data-ttu-id="bb0fd-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="bb0fd-109">**cb**</span></span>
  
> <span data-ttu-id="bb0fd-110">Recuento de bytes en el miembro **lpb** .</span><span class="sxs-lookup"><span data-stu-id="bb0fd-110">Count of bytes in the **lpb** member.</span></span> 
    
 <span data-ttu-id="bb0fd-111">**lpb**</span><span class="sxs-lookup"><span data-stu-id="bb0fd-111">**lpb**</span></span>
  
> <span data-ttu-id="bb0fd-112">Puntero para el valor de la propiedad PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="bb0fd-112">Pointer to the PT_BINARY property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bb0fd-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bb0fd-113">Remarks</span></span>

<span data-ttu-id="bb0fd-114">Para obtener información acerca de los tipos de propiedad, vea [Información general sobre el tipo de propiedad MAPI](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bb0fd-114">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bb0fd-115">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="bb0fd-115">See also</span></span>



[<span data-ttu-id="bb0fd-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="bb0fd-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="bb0fd-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="bb0fd-117">MAPI Structures</span></span>](mapi-structures.md)

