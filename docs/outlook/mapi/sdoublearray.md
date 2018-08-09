---
title: SDoubleArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDoubleArray
api_type:
- COM
ms.assetid: b63b26de-faf9-453c-ab8b-fb703ed09ae8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cde59b73381458533910dc8f0a728cc4e6ca0c01
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820607"
---
# <a name="sdoublearray"></a><span data-ttu-id="f0808-103">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="f0808-103">SDoubleArray</span></span>

  
  
<span data-ttu-id="f0808-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f0808-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f0808-105">Contiene una matriz de tipo Double que se usa para describir una propiedad de tipo PT_MV_DOUBLE.</span><span class="sxs-lookup"><span data-stu-id="f0808-105">Contains an array of doubles used to describe a property of type PT_MV_DOUBLE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f0808-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="f0808-106">Header file:</span></span>  <br/> |<span data-ttu-id="f0808-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f0808-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDoubleArray
{
  ULONG cValues;
  double FAR *lpdbl;
} SDoubleArray;

```

## <a name="members"></a><span data-ttu-id="f0808-108">Members</span><span class="sxs-lookup"><span data-stu-id="f0808-108">Members</span></span>

 <span data-ttu-id="f0808-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="f0808-109">**cValues**</span></span>
  
> <span data-ttu-id="f0808-110">Recuento de valores de la matriz indicada por el miembro **lpdbl** .</span><span class="sxs-lookup"><span data-stu-id="f0808-110">Count of values in the array pointed to by the **lpdbl** member.</span></span> 
    
 <span data-ttu-id="f0808-111">**lpdbl**</span><span class="sxs-lookup"><span data-stu-id="f0808-111">**lpdbl**</span></span>
  
> <span data-ttu-id="f0808-112">Puntero a una matriz de valores de tipo double.</span><span class="sxs-lookup"><span data-stu-id="f0808-112">Pointer to an array of double values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f0808-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f0808-113">Remarks</span></span>

<span data-ttu-id="f0808-114">Para obtener más información sobre PT_MV_DOUBLE, vea la [Lista de tipos de propiedad](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="f0808-114">For more information about PT_MV_DOUBLE, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f0808-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0808-115">See also</span></span>



[<span data-ttu-id="f0808-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f0808-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="f0808-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="f0808-117">MAPI Structures</span></span>](mapi-structures.md)

