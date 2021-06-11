---
title: SShortArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SShortArray
api_type:
- COM
ms.assetid: 201ceb76-41bc-4d7b-835d-5196bf3dc234
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8ea7d51b15a6e6acd44a3c0b6158378661f311bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429617"
---
# <a name="sshortarray"></a><span data-ttu-id="0a230-103">SShortArray</span><span class="sxs-lookup"><span data-stu-id="0a230-103">SShortArray</span></span>

  
  
<span data-ttu-id="0a230-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a230-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a230-105">Contiene una matriz de valores enteros sin signo que se usan para describir una propiedad de tipo PT_MV_SHORT.</span><span class="sxs-lookup"><span data-stu-id="0a230-105">Contains an array of unsigned integer values that are used to describe a property of type PT_MV_SHORT.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0a230-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="0a230-106">Header file:</span></span>  <br/> |<span data-ttu-id="0a230-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0a230-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a><span data-ttu-id="0a230-108">Members</span><span class="sxs-lookup"><span data-stu-id="0a230-108">Members</span></span>

 <span data-ttu-id="0a230-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="0a230-109">**cValues**</span></span>
  
> <span data-ttu-id="0a230-110">Recuento de valores en la matriz apuntada por el **miembro lpi.**</span><span class="sxs-lookup"><span data-stu-id="0a230-110">Count of values in the array pointed to by the **lpi** member.</span></span> 
    
 <span data-ttu-id="0a230-111">**lpi**</span><span class="sxs-lookup"><span data-stu-id="0a230-111">**lpi**</span></span>
  
> <span data-ttu-id="0a230-112">Puntero a una matriz de valores enteros sin signo.</span><span class="sxs-lookup"><span data-stu-id="0a230-112">Pointer to an array of unsigned integer values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0a230-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0a230-113">Remarks</span></span>

<span data-ttu-id="0a230-114">Para obtener más información acerca de PT_MV_SHORT y otros tipos de propiedades, vea [Tipos de propiedad](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="0a230-114">For more information about PT_MV_SHORT and other property types, see [Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0a230-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a230-115">See also</span></span>



[<span data-ttu-id="0a230-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="0a230-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="0a230-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="0a230-117">MAPI Structures</span></span>](mapi-structures.md)

