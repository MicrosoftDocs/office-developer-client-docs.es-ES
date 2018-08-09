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
ms.openlocfilehash: 9734adff9c9c7526fc8ff46d17ca913752e104b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820595"
---
# <a name="sdatetimearray"></a><span data-ttu-id="b5c23-103">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="b5c23-103">SDateTimeArray</span></span>

  
  
<span data-ttu-id="b5c23-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b5c23-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b5c23-105">Contiene una matriz de valores de hora que se utilizan para describir una propiedad de tipo PT_MV_SYSTIME.</span><span class="sxs-lookup"><span data-stu-id="b5c23-105">Contains an array of time values that are used to describe a property of type PT_MV_SYSTIME.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b5c23-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="b5c23-106">Header file:</span></span>  <br/> |<span data-ttu-id="b5c23-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b5c23-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDateTimeArray
{
  ULONG cValues;
  FILETIME FAR *lpft;
} SDateTimeArray;

```

## <a name="members"></a><span data-ttu-id="b5c23-108">Members</span><span class="sxs-lookup"><span data-stu-id="b5c23-108">Members</span></span>

 <span data-ttu-id="b5c23-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="b5c23-109">**cValues**</span></span>
  
> <span data-ttu-id="b5c23-110">Recuento de valores de la matriz indicada por el miembro **lpft** .</span><span class="sxs-lookup"><span data-stu-id="b5c23-110">Count of values in the array pointed to by the **lpft** member.</span></span> 
    
 <span data-ttu-id="b5c23-111">**lpft**</span><span class="sxs-lookup"><span data-stu-id="b5c23-111">**lpft**</span></span>
  
> <span data-ttu-id="b5c23-112">Puntero a una matriz de estructuras [FILETIME](filetime.md) que contienen los valores de tiempo.</span><span class="sxs-lookup"><span data-stu-id="b5c23-112">Pointer to an array of [FILETIME](filetime.md) structures that contain the time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b5c23-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b5c23-113">Remarks</span></span>

<span data-ttu-id="b5c23-114">Para obtener más información sobre PT_MV_SYSTIME, vea la [Lista de tipos de propiedad](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="b5c23-114">For more information about PT_MV_SYSTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b5c23-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5c23-115">See also</span></span>



[<span data-ttu-id="b5c23-116">FILETIME</span><span class="sxs-lookup"><span data-stu-id="b5c23-116">FILETIME</span></span>](filetime.md)
  
[<span data-ttu-id="b5c23-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b5c23-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="b5c23-118">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="b5c23-118">MAPI Structures</span></span>](mapi-structures.md)

