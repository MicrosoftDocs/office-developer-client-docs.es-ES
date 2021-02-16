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
ms.openlocfilehash: 9b1c5a09a60240efa9d4fa117f0d8fe8113169d5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414532"
---
# <a name="slongarray"></a><span data-ttu-id="1efa9-103">SLongArray</span><span class="sxs-lookup"><span data-stu-id="1efa9-103">SLongArray</span></span>

  
  
<span data-ttu-id="1efa9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1efa9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1efa9-105">Contiene una matriz de tipos de valor LONG que se usan para describir una propiedad de tipo PT_MV_LONG.</span><span class="sxs-lookup"><span data-stu-id="1efa9-105">Contains an array of LONG value types that are used to describe a property of type PT_MV_LONG.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1efa9-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="1efa9-106">Header file:</span></span>  <br/> |<span data-ttu-id="1efa9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1efa9-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a><span data-ttu-id="1efa9-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="1efa9-108">Members</span></span>

 <span data-ttu-id="1efa9-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="1efa9-109">**cValues**</span></span>
  
> <span data-ttu-id="1efa9-110">Recuento de valores en la matriz a la que apunta el **miembro lpl.**</span><span class="sxs-lookup"><span data-stu-id="1efa9-110">Count of values in the array pointed to by the **lpl** member.</span></span> 
    
 <span data-ttu-id="1efa9-111">**lpl**</span><span class="sxs-lookup"><span data-stu-id="1efa9-111">**lpl**</span></span>
  
> <span data-ttu-id="1efa9-112">Puntero a una matriz de valores LONG.</span><span class="sxs-lookup"><span data-stu-id="1efa9-112">Pointer to an array of LONG values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1efa9-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1efa9-113">Remarks</span></span>

<span data-ttu-id="1efa9-114">Para obtener más información acerca PT_MV_LONG, vea [Lista de tipos de propiedad](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="1efa9-114">For more information about PT_MV_LONG, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1efa9-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1efa9-115">See also</span></span>



[<span data-ttu-id="1efa9-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="1efa9-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="1efa9-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="1efa9-117">MAPI Structures</span></span>](mapi-structures.md)

