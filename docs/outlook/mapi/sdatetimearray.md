---
title: SDateTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDateTimeArray
api_type:
- COM
ms.assetid: 6a0dff65-1055-487c-9d15-4cfe336f2ad7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9d9fd04776742383f40c6989bcf588b24b33d84b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406783"
---
# <a name="sdatetimearray"></a><span data-ttu-id="36c99-103">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="36c99-103">SDateTimeArray</span></span>

  
  
<span data-ttu-id="36c99-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36c99-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36c99-105">Contiene una matriz de valores de tiempo que se usan para describir una propiedad de tipo PT_MV_SYSTIME.</span><span class="sxs-lookup"><span data-stu-id="36c99-105">Contains an array of time values that are used to describe a property of type PT_MV_SYSTIME.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="36c99-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="36c99-106">Header file:</span></span>  <br/> |<span data-ttu-id="36c99-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="36c99-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDateTimeArray
{
  ULONG cValues;
  FILETIME FAR *lpft;
} SDateTimeArray;

```

## <a name="members"></a><span data-ttu-id="36c99-108">Members</span><span class="sxs-lookup"><span data-stu-id="36c99-108">Members</span></span>

 <span data-ttu-id="36c99-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="36c99-109">**cValues**</span></span>
  
> <span data-ttu-id="36c99-110">Recuento de valores de la matriz a la que apunta el **miembro lpft.**</span><span class="sxs-lookup"><span data-stu-id="36c99-110">Count of values in the array pointed to by the **lpft** member.</span></span> 
    
 <span data-ttu-id="36c99-111">**lpft**</span><span class="sxs-lookup"><span data-stu-id="36c99-111">**lpft**</span></span>
  
> <span data-ttu-id="36c99-112">Puntero a una matriz de [estructuras FILETIME](filetime.md) que contienen los valores de hora.</span><span class="sxs-lookup"><span data-stu-id="36c99-112">Pointer to an array of [FILETIME](filetime.md) structures that contain the time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="36c99-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="36c99-113">Remarks</span></span>

<span data-ttu-id="36c99-114">Para obtener más información sobre PT_MV_SYSTIME, [vea Lista de tipos de propiedad](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="36c99-114">For more information about PT_MV_SYSTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="36c99-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="36c99-115">See also</span></span>



[<span data-ttu-id="36c99-116">FILETIME</span><span class="sxs-lookup"><span data-stu-id="36c99-116">FILETIME</span></span>](filetime.md)
  
[<span data-ttu-id="36c99-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="36c99-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="36c99-118">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="36c99-118">MAPI Structures</span></span>](mapi-structures.md)

