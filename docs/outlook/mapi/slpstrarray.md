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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 6d2bb6bdb934e0b02831b813b1246a3df4193e0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820703"
---
# <a name="slpstrarray"></a><span data-ttu-id="97fd5-103">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="97fd5-103">SLPSTRArray</span></span>

  
  
<span data-ttu-id="97fd5-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="97fd5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="97fd5-105">Contiene una matriz de valores de cadena que se utilizan para describir una propiedad de tipo PT_MV_STRING8.</span><span class="sxs-lookup"><span data-stu-id="97fd5-105">Contains an array of string values that are used to describe a property of type PT_MV_STRING8.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="97fd5-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="97fd5-106">Header file:</span></span>  <br/> |<span data-ttu-id="97fd5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="97fd5-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a><span data-ttu-id="97fd5-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="97fd5-108">Members</span></span>

 <span data-ttu-id="97fd5-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="97fd5-109">**cValues**</span></span>
  
> <span data-ttu-id="97fd5-110">Recuento de valores de la matriz indicada por el miembro **lppszA** .</span><span class="sxs-lookup"><span data-stu-id="97fd5-110">Count of values in the array pointed to by the **lppszA** member.</span></span> 
    
 <span data-ttu-id="97fd5-111">**lppszA**</span><span class="sxs-lookup"><span data-stu-id="97fd5-111">**lppszA**</span></span>
  
> <span data-ttu-id="97fd5-112">Puntero a una matriz de cadenas de caracteres de 8 bits terminado en null.</span><span class="sxs-lookup"><span data-stu-id="97fd5-112">Pointer to an array of null-ended 8-bit character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="97fd5-113">Notas</span><span class="sxs-lookup"><span data-stu-id="97fd5-113">Remarks</span></span>

<span data-ttu-id="97fd5-114">Para obtener más información sobre PT_MV_STRING8, vea la [Lista de tipos de propiedad](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="97fd5-114">For more information about PT_MV_STRING8, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="97fd5-115">Ver también</span><span class="sxs-lookup"><span data-stu-id="97fd5-115">See also</span></span>



[<span data-ttu-id="97fd5-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="97fd5-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="97fd5-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="97fd5-117">MAPI Structures</span></span>](mapi-structures.md)

