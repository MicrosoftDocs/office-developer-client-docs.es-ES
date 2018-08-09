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
ms.openlocfilehash: fe07ed7c7f9c76f82b54732c019b9b5f8beb5db2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820553"
---
# <a name="sbinary"></a><span data-ttu-id="d33a2-103">SBinary</span><span class="sxs-lookup"><span data-stu-id="d33a2-103">SBinary</span></span>

  
  
<span data-ttu-id="d33a2-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d33a2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d33a2-105">Describe una propiedad de tipo PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="d33a2-105">Describes a property of type PT_BINARY.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d33a2-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d33a2-106">Header file:</span></span>  <br/> |<span data-ttu-id="d33a2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d33a2-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinary
{
  ULONG      cb;
  LPBYTE     lpb;
} SBinary, FAR *LPSBinary;

```

## <a name="members"></a><span data-ttu-id="d33a2-108">Members</span><span class="sxs-lookup"><span data-stu-id="d33a2-108">Members</span></span>

 <span data-ttu-id="d33a2-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="d33a2-109">**cb**</span></span>
  
> <span data-ttu-id="d33a2-110">Recuento de bytes en el miembro **lpb** .</span><span class="sxs-lookup"><span data-stu-id="d33a2-110">Count of bytes in the **lpb** member.</span></span> 
    
 <span data-ttu-id="d33a2-111">**lpb**</span><span class="sxs-lookup"><span data-stu-id="d33a2-111">**lpb**</span></span>
  
> <span data-ttu-id="d33a2-112">Puntero para el valor de la propiedad PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="d33a2-112">Pointer to the PT_BINARY property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d33a2-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d33a2-113">Remarks</span></span>

<span data-ttu-id="d33a2-114">Para obtener información acerca de los tipos de propiedad, vea [Información general sobre el tipo de propiedad MAPI](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d33a2-114">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d33a2-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="d33a2-115">See also</span></span>



[<span data-ttu-id="d33a2-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d33a2-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="d33a2-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="d33a2-117">MAPI Structures</span></span>](mapi-structures.md)

