---
title: SGuidArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SGuidArray
api_type:
- COM
ms.assetid: 2091e5fc-75c8-4ea4-87e9-a9bf508e9c58
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3d20a0932de0fb29ea73e56c37e262c0ccd062c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339217"
---
# <a name="sguidarray"></a><span data-ttu-id="e416c-103">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="e416c-103">SGuidArray</span></span>

  
  
<span data-ttu-id="e416c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e416c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e416c-105">Contiene una matriz de estructuras [GUID](guid.md) que se usan para describir una propiedad de tipo PT_MV_CLSID.</span><span class="sxs-lookup"><span data-stu-id="e416c-105">Contains an array of [GUID](guid.md) structures that are used to describe a property of type PT_MV_CLSID.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e416c-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e416c-106">Header file:</span></span>  <br/> |<span data-ttu-id="e416c-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e416c-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SGuidArray
{
  ULONG cValues;
  GUID FAR *lpguid;
} SGuidArray;

```

## <a name="members"></a><span data-ttu-id="e416c-108">Members</span><span class="sxs-lookup"><span data-stu-id="e416c-108">Members</span></span>

 <span data-ttu-id="e416c-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="e416c-109">**cValues**</span></span>
  
> <span data-ttu-id="e416c-110">Número de valores de la matriz a los que señala el miembro **lpguid** .</span><span class="sxs-lookup"><span data-stu-id="e416c-110">Count of values in the array pointed to by the **lpguid** member.</span></span> 
    
 <span data-ttu-id="e416c-111">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="e416c-111">**lpguid**</span></span>
  
> <span data-ttu-id="e416c-112">Puntero a una matriz de estructuras **GUID** que contiene los valores de identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="e416c-112">Pointer to an array of **GUID** structures that contains the class identifier values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e416c-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e416c-113">Remarks</span></span>

<span data-ttu-id="e416c-114">Para obtener más información acerca de PT_MV_CLSID, vea [lista de tipos de propiedades](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="e416c-114">For more information about PT_MV_CLSID, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e416c-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="e416c-115">See also</span></span>



[<span data-ttu-id="e416c-116">GUID</span><span class="sxs-lookup"><span data-stu-id="e416c-116">GUID</span></span>](guid.md)
  
[<span data-ttu-id="e416c-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="e416c-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="e416c-118">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="e416c-118">MAPI Structures</span></span>](mapi-structures.md)

