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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 553ec17e9caf9bf93278ff139eb94e02e6b48554
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19820659"
---
# <a name="sguidarray"></a><span data-ttu-id="03ff3-103">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="03ff3-103">SGuidArray</span></span>

  
  
<span data-ttu-id="03ff3-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="03ff3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="03ff3-105">Contiene una matriz de estructuras [GUID](guid.md) que se utilizan para describir una propiedad de tipo PT_MV_CLSID.</span><span class="sxs-lookup"><span data-stu-id="03ff3-105">Contains an array of [GUID](guid.md) structures that are used to describe a property of type PT_MV_CLSID.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="03ff3-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="03ff3-106">Header file:</span></span>  <br/> |<span data-ttu-id="03ff3-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="03ff3-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SGuidArray
{
  ULONG cValues;
  GUID FAR *lpguid;
} SGuidArray;

```

## <a name="members"></a><span data-ttu-id="03ff3-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="03ff3-108">Members</span></span>

 <span data-ttu-id="03ff3-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="03ff3-109">**cValues**</span></span>
  
> <span data-ttu-id="03ff3-110">Recuento de valores de la matriz indicada por el miembro **lpguid** .</span><span class="sxs-lookup"><span data-stu-id="03ff3-110">Count of values in the array pointed to by the **lpguid** member.</span></span> 
    
 <span data-ttu-id="03ff3-111">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="03ff3-111">**lpguid**</span></span>
  
> <span data-ttu-id="03ff3-112">Puntero a una matriz de estructuras **GUID** que contiene los valores de identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="03ff3-112">Pointer to an array of **GUID** structures that contains the class identifier values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="03ff3-113">Notas</span><span class="sxs-lookup"><span data-stu-id="03ff3-113">Remarks</span></span>

<span data-ttu-id="03ff3-114">Para obtener más información sobre PT_MV_CLSID, vea la [Lista de tipos de propiedad](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="03ff3-114">For more information about PT_MV_CLSID, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="03ff3-115">Ver también</span><span class="sxs-lookup"><span data-stu-id="03ff3-115">See also</span></span>



[<span data-ttu-id="03ff3-116">GUID</span><span class="sxs-lookup"><span data-stu-id="03ff3-116">GUID</span></span>](guid.md)
  
[<span data-ttu-id="03ff3-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="03ff3-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="03ff3-118">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="03ff3-118">MAPI Structures</span></span>](mapi-structures.md)

