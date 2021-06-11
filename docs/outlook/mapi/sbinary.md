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
ms.openlocfilehash: 38263f46ccb50e1836f31d457f54f52abca7ce9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407847"
---
# <a name="sbinary"></a><span data-ttu-id="a5190-103">SBinary</span><span class="sxs-lookup"><span data-stu-id="a5190-103">SBinary</span></span>

  
  
<span data-ttu-id="a5190-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5190-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5190-105">Describe una propiedad de tipo PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="a5190-105">Describes a property of type PT_BINARY.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a5190-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a5190-106">Header file:</span></span>  <br/> |<span data-ttu-id="a5190-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a5190-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinary
{
  ULONG      cb;
  LPBYTE     lpb;
} SBinary, FAR *LPSBinary;

```

## <a name="members"></a><span data-ttu-id="a5190-108">Members</span><span class="sxs-lookup"><span data-stu-id="a5190-108">Members</span></span>

 <span data-ttu-id="a5190-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="a5190-109">**cb**</span></span>
  
> <span data-ttu-id="a5190-110">Recuento de bytes en el **miembro lpb.**</span><span class="sxs-lookup"><span data-stu-id="a5190-110">Count of bytes in the **lpb** member.</span></span> 
    
 <span data-ttu-id="a5190-111">**lpb**</span><span class="sxs-lookup"><span data-stu-id="a5190-111">**lpb**</span></span>
  
> <span data-ttu-id="a5190-112">Puntero al valor PT_BINARY propiedad.</span><span class="sxs-lookup"><span data-stu-id="a5190-112">Pointer to the PT_BINARY property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a5190-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a5190-113">Remarks</span></span>

<span data-ttu-id="a5190-114">Para obtener información acerca de los tipos de propiedad, vea [Información general sobre el tipo de propiedad MAPI](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a5190-114">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a5190-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5190-115">See also</span></span>



[<span data-ttu-id="a5190-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="a5190-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="a5190-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="a5190-117">MAPI Structures</span></span>](mapi-structures.md)

