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
ms.openlocfilehash: dc90f15835de35354a271d87a736366a4caf8dd9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578783"
---
# <a name="sdatetimearray"></a><span data-ttu-id="08086-103">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="08086-103">SDateTimeArray</span></span>

  
  
<span data-ttu-id="08086-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08086-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08086-105">Contiene una matriz de valores de hora que se utilizan para describir una propiedad de tipo PT_MV_SYSTIME.</span><span class="sxs-lookup"><span data-stu-id="08086-105">Contains an array of time values that are used to describe a property of type PT_MV_SYSTIME.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="08086-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="08086-106">Header file:</span></span>  <br/> |<span data-ttu-id="08086-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="08086-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDateTimeArray
{
  ULONG cValues;
  FILETIME FAR *lpft;
} SDateTimeArray;

```

## <a name="members"></a><span data-ttu-id="08086-108">Members</span><span class="sxs-lookup"><span data-stu-id="08086-108">Members</span></span>

 <span data-ttu-id="08086-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="08086-109">**cValues**</span></span>
  
> <span data-ttu-id="08086-110">Recuento de valores de la matriz indicada por el miembro **lpft** .</span><span class="sxs-lookup"><span data-stu-id="08086-110">Count of values in the array pointed to by the **lpft** member.</span></span> 
    
 <span data-ttu-id="08086-111">**lpft**</span><span class="sxs-lookup"><span data-stu-id="08086-111">**lpft**</span></span>
  
> <span data-ttu-id="08086-112">Puntero a una matriz de estructuras [FILETIME](filetime.md) que contienen los valores de tiempo.</span><span class="sxs-lookup"><span data-stu-id="08086-112">Pointer to an array of [FILETIME](filetime.md) structures that contain the time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="08086-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="08086-113">Remarks</span></span>

<span data-ttu-id="08086-114">Para obtener más información sobre PT_MV_SYSTIME, vea la [Lista de tipos de propiedad](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="08086-114">For more information about PT_MV_SYSTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="08086-115">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="08086-115">See also</span></span>



[<span data-ttu-id="08086-116">FILETIME</span><span class="sxs-lookup"><span data-stu-id="08086-116">FILETIME</span></span>](filetime.md)
  
[<span data-ttu-id="08086-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="08086-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="08086-118">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="08086-118">MAPI Structures</span></span>](mapi-structures.md)

