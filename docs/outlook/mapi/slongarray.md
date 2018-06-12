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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: c207b1db6a24cc60967735e2f4b1a4aa97007750
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820697"
---
# <a name="slongarray"></a><span data-ttu-id="ac952-103">SLongArray</span><span class="sxs-lookup"><span data-stu-id="ac952-103">SLongArray</span></span>

  
  
<span data-ttu-id="ac952-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ac952-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ac952-105">Contiene una matriz de tipos de valor de tipo LONG que se utilizan para describir una propiedad de tipo PT_MV_LONG.</span><span class="sxs-lookup"><span data-stu-id="ac952-105">Contains an array of LONG value types that are used to describe a property of type PT_MV_LONG.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ac952-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="ac952-106">Header file:</span></span>  <br/> |<span data-ttu-id="ac952-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ac952-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a><span data-ttu-id="ac952-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ac952-108">Members</span></span>

 <span data-ttu-id="ac952-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="ac952-109">**cValues**</span></span>
  
> <span data-ttu-id="ac952-110">Recuento de valores de la matriz indicada por el miembro **lpl** .</span><span class="sxs-lookup"><span data-stu-id="ac952-110">Count of values in the array pointed to by the **lpl** member.</span></span> 
    
 <span data-ttu-id="ac952-111">**lpl**</span><span class="sxs-lookup"><span data-stu-id="ac952-111">**lpl**</span></span>
  
> <span data-ttu-id="ac952-112">Puntero a una matriz de valores de tipo LONG.</span><span class="sxs-lookup"><span data-stu-id="ac952-112">Pointer to an array of LONG values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ac952-113">Notas</span><span class="sxs-lookup"><span data-stu-id="ac952-113">Remarks</span></span>

<span data-ttu-id="ac952-114">Para obtener más información sobre PT_MV_LONG, vea la [Lista de tipos de propiedad](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="ac952-114">For more information about PT_MV_LONG, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ac952-115">Ver también</span><span class="sxs-lookup"><span data-stu-id="ac952-115">See also</span></span>



[<span data-ttu-id="ac952-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="ac952-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="ac952-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="ac952-117">MAPI Structures</span></span>](mapi-structures.md)

