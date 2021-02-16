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
ms.openlocfilehash: 91440d619c8ad8a64b2bac7463a26d9c196a3c0f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439271"
---
# <a name="sdoublearray"></a><span data-ttu-id="abb3a-103">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="abb3a-103">SDoubleArray</span></span>

  
  
<span data-ttu-id="abb3a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="abb3a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="abb3a-105">Contiene una matriz de dobles que se usa para describir una propiedad de tipo PT_MV_DOUBLE.</span><span class="sxs-lookup"><span data-stu-id="abb3a-105">Contains an array of doubles used to describe a property of type PT_MV_DOUBLE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="abb3a-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="abb3a-106">Header file:</span></span>  <br/> |<span data-ttu-id="abb3a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="abb3a-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDoubleArray
{
  ULONG cValues;
  double FAR *lpdbl;
} SDoubleArray;

```

## <a name="members"></a><span data-ttu-id="abb3a-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="abb3a-108">Members</span></span>

 <span data-ttu-id="abb3a-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="abb3a-109">**cValues**</span></span>
  
> <span data-ttu-id="abb3a-110">Recuento de valores de la matriz a la que apunta el **miembro lpdbl.**</span><span class="sxs-lookup"><span data-stu-id="abb3a-110">Count of values in the array pointed to by the **lpdbl** member.</span></span> 
    
 <span data-ttu-id="abb3a-111">**lpdbl**</span><span class="sxs-lookup"><span data-stu-id="abb3a-111">**lpdbl**</span></span>
  
> <span data-ttu-id="abb3a-112">Puntero a una matriz de valores dobles.</span><span class="sxs-lookup"><span data-stu-id="abb3a-112">Pointer to an array of double values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="abb3a-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="abb3a-113">Remarks</span></span>

<span data-ttu-id="abb3a-114">Para obtener más información acerca PT_MV_DOUBLE, vea [Lista de tipos de propiedad](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="abb3a-114">For more information about PT_MV_DOUBLE, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="abb3a-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="abb3a-115">See also</span></span>



[<span data-ttu-id="abb3a-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="abb3a-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="abb3a-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="abb3a-117">MAPI Structures</span></span>](mapi-structures.md)

