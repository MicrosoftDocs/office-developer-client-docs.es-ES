---
title: SCurrencyArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCurrencyArray
api_type:
- COM
ms.assetid: d28852ab-b542-40e1-b2ec-85d20a2eddfd
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e9468d0c7fc7e46475afe19f12f225e53196639e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360700"
---
# <a name="scurrencyarray"></a><span data-ttu-id="aeff1-103">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="aeff1-103">SCurrencyArray</span></span>

  
  
<span data-ttu-id="aeff1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aeff1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aeff1-105">Contiene una matriz de valores de moneda que se usan para describir una propiedad de tipo PT_MV_CURRENCY.</span><span class="sxs-lookup"><span data-stu-id="aeff1-105">Contains an array of currency values that are used to describe a property of type PT_MV_CURRENCY.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aeff1-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="aeff1-106">Header file:</span></span>  <br/> |<span data-ttu-id="aeff1-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="aeff1-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a><span data-ttu-id="aeff1-108">Members</span><span class="sxs-lookup"><span data-stu-id="aeff1-108">Members</span></span>

 <span data-ttu-id="aeff1-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="aeff1-109">**cValues**</span></span>
  
> <span data-ttu-id="aeff1-110">Número de valores de la matriz a los que señala el miembro **lpcur** .</span><span class="sxs-lookup"><span data-stu-id="aeff1-110">Count of values in the array pointed to by the **lpcur** member.</span></span> 
    
 <span data-ttu-id="aeff1-111">**lpcur**</span><span class="sxs-lookup"><span data-stu-id="aeff1-111">**lpcur**</span></span>
  
> <span data-ttu-id="aeff1-112">Puntero a una matriz de estructuras de [moneda](currency.md) que contienen los valores de moneda.</span><span class="sxs-lookup"><span data-stu-id="aeff1-112">Pointer to an array of [CURRENCY](currency.md) structures that contain the currency values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="aeff1-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aeff1-113">Remarks</span></span>

<span data-ttu-id="aeff1-114">Para obtener información sobre PT_MV_CURRENCY, vea [lista de tipos de propiedades](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="aeff1-114">For information about PT_MV_CURRENCY, see [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aeff1-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="aeff1-115">See also</span></span>



[<span data-ttu-id="aeff1-116">Visa</span><span class="sxs-lookup"><span data-stu-id="aeff1-116">CURRENCY</span></span>](currency.md)
  
[<span data-ttu-id="aeff1-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="aeff1-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="aeff1-118">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="aeff1-118">MAPI Structures</span></span>](mapi-structures.md)

