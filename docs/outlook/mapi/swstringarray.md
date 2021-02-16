---
title: SWStringArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SWStringArray
api_type:
- COM
ms.assetid: c1ae24ad-1bbb-4dee-b414-b5226593b6fa
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ff69981e83d42e439936a3e4be47eabfd811b310
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413608"
---
# <a name="swstringarray"></a><span data-ttu-id="0d7aa-103">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="0d7aa-103">SWStringArray</span></span>

  
  
<span data-ttu-id="0d7aa-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d7aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d7aa-105">Contiene una matriz de cadenas de caracteres que se usan para describir una propiedad de tipo PT_MV_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="0d7aa-105">Contains an array of character strings that are used to describe a property of type PT_MV_UNICODE.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0d7aa-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="0d7aa-106">Header file:</span></span>  <br/> |<span data-ttu-id="0d7aa-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0d7aa-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a><span data-ttu-id="0d7aa-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0d7aa-108">Members</span></span>

 <span data-ttu-id="0d7aa-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="0d7aa-109">**cValues**</span></span>
  
> <span data-ttu-id="0d7aa-110">Número de cadenas de la matriz a las que apunta el **miembro lppszW.**</span><span class="sxs-lookup"><span data-stu-id="0d7aa-110">Count of strings in the array pointed to by the **lppszW** member.</span></span> 
    
 <span data-ttu-id="0d7aa-111">**lppszW**</span><span class="sxs-lookup"><span data-stu-id="0d7aa-111">**lppszW**</span></span>
  
> <span data-ttu-id="0d7aa-112">Puntero a una matriz de cadenas de caracteres Unicode terminadas en null.</span><span class="sxs-lookup"><span data-stu-id="0d7aa-112">Pointer to an array of null-ended Unicode character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0d7aa-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0d7aa-113">Remarks</span></span>

<span data-ttu-id="0d7aa-114">Para obtener más información acerca PT_MV_UNICODE, vea [Tipos de propiedad](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="0d7aa-114">For more information about PT_MV_UNICODE, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0d7aa-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0d7aa-115">See also</span></span>



[<span data-ttu-id="0d7aa-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="0d7aa-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="0d7aa-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="0d7aa-117">MAPI Structures</span></span>](mapi-structures.md)

