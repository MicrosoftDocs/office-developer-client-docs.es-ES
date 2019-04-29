---
title: SLPSTRArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLPSTRArray
api_type:
- COM
ms.assetid: 5f570d9b-eb3d-4fc7-bcbe-348a0b8fe9e9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 987020bd6fd49fcba9453075cd502bd5cea4c3a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435911"
---
# <a name="slpstrarray"></a><span data-ttu-id="3eeeb-103">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="3eeeb-103">SLPSTRArray</span></span>

  
  
<span data-ttu-id="3eeeb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3eeeb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3eeeb-105">Contiene una matriz de valores de cadena que se usan para describir una propiedad de tipo PT_MV_STRING8.</span><span class="sxs-lookup"><span data-stu-id="3eeeb-105">Contains an array of string values that are used to describe a property of type PT_MV_STRING8.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3eeeb-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="3eeeb-106">Header file:</span></span>  <br/> |<span data-ttu-id="3eeeb-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3eeeb-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a><span data-ttu-id="3eeeb-108">Members</span><span class="sxs-lookup"><span data-stu-id="3eeeb-108">Members</span></span>

 <span data-ttu-id="3eeeb-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="3eeeb-109">**cValues**</span></span>
  
> <span data-ttu-id="3eeeb-110">Número de valores de la matriz a los que señala el miembro **lppszA** .</span><span class="sxs-lookup"><span data-stu-id="3eeeb-110">Count of values in the array pointed to by the **lppszA** member.</span></span> 
    
 <span data-ttu-id="3eeeb-111">**lppszA**</span><span class="sxs-lookup"><span data-stu-id="3eeeb-111">**lppszA**</span></span>
  
> <span data-ttu-id="3eeeb-112">Puntero a una matriz de cadenas de caracteres de 8 bits terminadas en NULL.</span><span class="sxs-lookup"><span data-stu-id="3eeeb-112">Pointer to an array of null-ended 8-bit character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3eeeb-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3eeeb-113">Remarks</span></span>

<span data-ttu-id="3eeeb-114">Para obtener más información acerca de PT_MV_STRING8, vea [lista de tipos de propiedades](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="3eeeb-114">For more information about PT_MV_STRING8, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3eeeb-115">Ver también</span><span class="sxs-lookup"><span data-stu-id="3eeeb-115">See also</span></span>



[<span data-ttu-id="3eeeb-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3eeeb-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="3eeeb-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="3eeeb-117">MAPI Structures</span></span>](mapi-structures.md)

