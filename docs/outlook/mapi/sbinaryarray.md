---
title: SBinaryArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinaryArray
api_type:
- COM
ms.assetid: 2d5b7302-cad2-4522-beb1-7c6c711f42e6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e601a59a68a3a7d248165d4e573c5abc34d27e2a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586469"
---
# <a name="sbinaryarray"></a><span data-ttu-id="d9fe8-103">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="d9fe8-103">SBinaryArray</span></span>

  
  
<span data-ttu-id="d9fe8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9fe8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9fe8-105">Contiene una matriz de valores binarios.</span><span class="sxs-lookup"><span data-stu-id="d9fe8-105">Contains an array of binary values.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d9fe8-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d9fe8-106">Header file:</span></span>  <br/> |<span data-ttu-id="d9fe8-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d9fe8-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a><span data-ttu-id="d9fe8-108">Members</span><span class="sxs-lookup"><span data-stu-id="d9fe8-108">Members</span></span>

 <span data-ttu-id="d9fe8-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="d9fe8-109">**cValues**</span></span>
  
> <span data-ttu-id="d9fe8-110">Recuento de valores de la matriz indicada por el miembro **lpbin** .</span><span class="sxs-lookup"><span data-stu-id="d9fe8-110">Count of values in the array pointed to by the **lpbin** member.</span></span> 
    
 <span data-ttu-id="d9fe8-111">**lpbin**</span><span class="sxs-lookup"><span data-stu-id="d9fe8-111">**lpbin**</span></span>
  
> <span data-ttu-id="d9fe8-112">Puntero a una matriz de estructuras [SBinary](sbinary.md) que contiene los valores binarios.</span><span class="sxs-lookup"><span data-stu-id="d9fe8-112">Pointer to an array of [SBinary](sbinary.md) structures that holds the binary values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d9fe8-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d9fe8-113">Remarks</span></span>

<span data-ttu-id="d9fe8-114">La estructura **SBinaryArray** se usa para describir las propiedades de tipo PT_MV_BINARY.</span><span class="sxs-lookup"><span data-stu-id="d9fe8-114">The **SBinaryArray** structure is used to describe properties of type PT_MV_BINARY.</span></span> 
  
<span data-ttu-id="d9fe8-115">Para obtener más información sobre PT_MV_BINARY, vea la [Lista de tipos de propiedad](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="d9fe8-115">For more information about PT_MV_BINARY, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d9fe8-116">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="d9fe8-116">See also</span></span>



[<span data-ttu-id="d9fe8-117">SBinary</span><span class="sxs-lookup"><span data-stu-id="d9fe8-117">SBinary</span></span>](sbinary.md)
  
[<span data-ttu-id="d9fe8-118">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d9fe8-118">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="d9fe8-119">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="d9fe8-119">MAPI Structures</span></span>](mapi-structures.md)

