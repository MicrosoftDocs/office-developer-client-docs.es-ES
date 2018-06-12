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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: c64e9a7497a70ea34dc09a5749dd281a24f9413d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820746"
---
# <a name="srealarray"></a><span data-ttu-id="2ba2b-103">SRealArray</span><span class="sxs-lookup"><span data-stu-id="2ba2b-103">SRealArray</span></span>

  
  
<span data-ttu-id="2ba2b-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2ba2b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2ba2b-105">Contiene una matriz de valores flotantes que se utilizan para describir una propiedad de tipo PT_MV_R4.</span><span class="sxs-lookup"><span data-stu-id="2ba2b-105">Contains an array of float values that are used to describe a property of type PT_MV_R4.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2ba2b-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="2ba2b-106">Header file:</span></span>  <br/> |<span data-ttu-id="2ba2b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2ba2b-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a><span data-ttu-id="2ba2b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="2ba2b-108">Members</span></span>

 <span data-ttu-id="2ba2b-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="2ba2b-109">**cValues**</span></span>
  
> <span data-ttu-id="2ba2b-110">Recuento de valores de la matriz indicada por el miembro **lpflt** .</span><span class="sxs-lookup"><span data-stu-id="2ba2b-110">Count of values in the array pointed to by the **lpflt** member.</span></span> 
    
 <span data-ttu-id="2ba2b-111">**lpflt**</span><span class="sxs-lookup"><span data-stu-id="2ba2b-111">**lpflt**</span></span>
  
> <span data-ttu-id="2ba2b-112">Puntero a una matriz de valores float.</span><span class="sxs-lookup"><span data-stu-id="2ba2b-112">Pointer to an array of float values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2ba2b-113">Notas</span><span class="sxs-lookup"><span data-stu-id="2ba2b-113">Remarks</span></span>

<span data-ttu-id="2ba2b-114">Para obtener más información sobre el tipo de propiedad PT_MV_R4, vea [Tipos de propiedades](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="2ba2b-114">For more information about the PT_MV_R4 property type, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2ba2b-115">Ver también</span><span class="sxs-lookup"><span data-stu-id="2ba2b-115">See also</span></span>



[<span data-ttu-id="2ba2b-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2ba2b-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="2ba2b-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="2ba2b-117">MAPI Structures</span></span>](mapi-structures.md)

