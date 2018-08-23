---
title: SRealArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRealArray
api_type:
- COM
ms.assetid: 95be07bf-5732-4775-9e0f-fec47e99d9b7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8c7ce2805248bf91ce7da071c67ece28a5b8ca07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564286"
---
# <a name="srealarray"></a><span data-ttu-id="488ef-103">SRealArray</span><span class="sxs-lookup"><span data-stu-id="488ef-103">SRealArray</span></span>

  
  
<span data-ttu-id="488ef-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="488ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="488ef-105">Contiene una matriz de valores flotantes que se utilizan para describir una propiedad de tipo PT_MV_R4.</span><span class="sxs-lookup"><span data-stu-id="488ef-105">Contains an array of float values that are used to describe a property of type PT_MV_R4.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="488ef-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="488ef-106">Header file:</span></span>  <br/> |<span data-ttu-id="488ef-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="488ef-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a><span data-ttu-id="488ef-108">Members</span><span class="sxs-lookup"><span data-stu-id="488ef-108">Members</span></span>

 <span data-ttu-id="488ef-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="488ef-109">**cValues**</span></span>
  
> <span data-ttu-id="488ef-110">Recuento de valores de la matriz indicada por el miembro **lpflt** .</span><span class="sxs-lookup"><span data-stu-id="488ef-110">Count of values in the array pointed to by the **lpflt** member.</span></span> 
    
 <span data-ttu-id="488ef-111">**lpflt**</span><span class="sxs-lookup"><span data-stu-id="488ef-111">**lpflt**</span></span>
  
> <span data-ttu-id="488ef-112">Puntero a una matriz de valores float.</span><span class="sxs-lookup"><span data-stu-id="488ef-112">Pointer to an array of float values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="488ef-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="488ef-113">Remarks</span></span>

<span data-ttu-id="488ef-114">Para obtener más información sobre el tipo de propiedad PT_MV_R4, vea [Tipos de propiedades](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="488ef-114">For more information about the PT_MV_R4 property type, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="488ef-115">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="488ef-115">See also</span></span>



[<span data-ttu-id="488ef-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="488ef-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="488ef-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="488ef-117">MAPI Structures</span></span>](mapi-structures.md)

