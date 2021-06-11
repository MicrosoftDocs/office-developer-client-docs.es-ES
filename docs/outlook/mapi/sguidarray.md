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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424927"
---
# <a name="sguidarray"></a><span data-ttu-id="acae0-103">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="acae0-103">SGuidArray</span></span>

  
  
<span data-ttu-id="acae0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="acae0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="acae0-105">Contiene una matriz de [estructuras GUID](guid.md) que se usan para describir una propiedad de tipo PT_MV_CLSID.</span><span class="sxs-lookup"><span data-stu-id="acae0-105">Contains an array of [GUID](guid.md) structures that are used to describe a property of type PT_MV_CLSID.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="acae0-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="acae0-106">Header file:</span></span>  <br/> |<span data-ttu-id="acae0-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="acae0-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SGuidArray
{
  ULONG cValues;
  GUID FAR *lpguid;
} SGuidArray;

```

## <a name="members"></a><span data-ttu-id="acae0-108">Members</span><span class="sxs-lookup"><span data-stu-id="acae0-108">Members</span></span>

 <span data-ttu-id="acae0-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="acae0-109">**cValues**</span></span>
  
> <span data-ttu-id="acae0-110">Recuento de valores en la matriz apuntada por el **miembro lpguid.**</span><span class="sxs-lookup"><span data-stu-id="acae0-110">Count of values in the array pointed to by the **lpguid** member.</span></span> 
    
 <span data-ttu-id="acae0-111">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="acae0-111">**lpguid**</span></span>
  
> <span data-ttu-id="acae0-112">Puntero a una matriz de **estructuras GUID** que contiene los valores de identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="acae0-112">Pointer to an array of **GUID** structures that contains the class identifier values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="acae0-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="acae0-113">Remarks</span></span>

<span data-ttu-id="acae0-114">Para obtener más información sobre PT_MV_CLSID, [vea List of Property Types](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="acae0-114">For more information about PT_MV_CLSID, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="acae0-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="acae0-115">See also</span></span>



[<span data-ttu-id="acae0-116">GUID</span><span class="sxs-lookup"><span data-stu-id="acae0-116">GUID</span></span>](guid.md)
  
[<span data-ttu-id="acae0-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="acae0-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="acae0-118">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="acae0-118">MAPI Structures</span></span>](mapi-structures.md)

