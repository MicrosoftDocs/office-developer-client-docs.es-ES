---
title: SLongArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLongArray
api_type:
- COM
ms.assetid: 57435634-202d-4998-9931-4562f1a66f5f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a44974accea30b5d1406c9cc74570012f61639e5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580652"
---
# <a name="slongarray"></a><span data-ttu-id="7ed36-103">SLongArray</span><span class="sxs-lookup"><span data-stu-id="7ed36-103">SLongArray</span></span>

  
  
<span data-ttu-id="7ed36-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ed36-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ed36-105">Contiene una matriz de tipos de valor de tipo LONG que se utilizan para describir una propiedad de tipo PT_MV_LONG.</span><span class="sxs-lookup"><span data-stu-id="7ed36-105">Contains an array of LONG value types that are used to describe a property of type PT_MV_LONG.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7ed36-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="7ed36-106">Header file:</span></span>  <br/> |<span data-ttu-id="7ed36-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7ed36-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a><span data-ttu-id="7ed36-108">Members</span><span class="sxs-lookup"><span data-stu-id="7ed36-108">Members</span></span>

 <span data-ttu-id="7ed36-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="7ed36-109">**cValues**</span></span>
  
> <span data-ttu-id="7ed36-110">Recuento de valores de la matriz indicada por el miembro **lpl** .</span><span class="sxs-lookup"><span data-stu-id="7ed36-110">Count of values in the array pointed to by the **lpl** member.</span></span> 
    
 <span data-ttu-id="7ed36-111">**lpl**</span><span class="sxs-lookup"><span data-stu-id="7ed36-111">**lpl**</span></span>
  
> <span data-ttu-id="7ed36-112">Puntero a una matriz de valores de tipo LONG.</span><span class="sxs-lookup"><span data-stu-id="7ed36-112">Pointer to an array of LONG values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7ed36-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7ed36-113">Remarks</span></span>

<span data-ttu-id="7ed36-114">Para obtener más información sobre PT_MV_LONG, vea la [Lista de tipos de propiedad](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="7ed36-114">For more information about PT_MV_LONG, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7ed36-115">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="7ed36-115">See also</span></span>



[<span data-ttu-id="7ed36-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7ed36-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="7ed36-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="7ed36-117">MAPI Structures</span></span>](mapi-structures.md)

