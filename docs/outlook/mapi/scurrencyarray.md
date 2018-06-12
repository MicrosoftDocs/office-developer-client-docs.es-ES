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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: c440bb7d8f3d2d3002a4d1a80ca3a671b49f4d2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820605"
---
# <a name="scurrencyarray"></a><span data-ttu-id="83e93-103">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="83e93-103">SCurrencyArray</span></span>

  
  
<span data-ttu-id="83e93-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="83e93-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="83e93-105">Contiene una matriz de valores de moneda que se utilizan para describir una propiedad de tipo PT_MV_CURRENCY.</span><span class="sxs-lookup"><span data-stu-id="83e93-105">Contains an array of currency values that are used to describe a property of type PT_MV_CURRENCY.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="83e93-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="83e93-106">Header file:</span></span>  <br/> |<span data-ttu-id="83e93-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="83e93-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a><span data-ttu-id="83e93-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="83e93-108">Members</span></span>

 <span data-ttu-id="83e93-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="83e93-109">**cValues**</span></span>
  
> <span data-ttu-id="83e93-110">Recuento de valores de la matriz indicada por el miembro **lpcur** .</span><span class="sxs-lookup"><span data-stu-id="83e93-110">Count of values in the array pointed to by the **lpcur** member.</span></span> 
    
 <span data-ttu-id="83e93-111">**lpcur**</span><span class="sxs-lookup"><span data-stu-id="83e93-111">**lpcur**</span></span>
  
> <span data-ttu-id="83e93-112">Puntero a una matriz de estructuras de [moneda](currency.md) que contienen los valores de moneda.</span><span class="sxs-lookup"><span data-stu-id="83e93-112">Pointer to an array of [CURRENCY](currency.md) structures that contain the currency values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="83e93-113">Notas</span><span class="sxs-lookup"><span data-stu-id="83e93-113">Remarks</span></span>

<span data-ttu-id="83e93-114">Para obtener información sobre PT_MV_CURRENCY, vea la [Lista de tipos de propiedad](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="83e93-114">For information about PT_MV_CURRENCY, see [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="83e93-115">Ver también</span><span class="sxs-lookup"><span data-stu-id="83e93-115">See also</span></span>



[<span data-ttu-id="83e93-116">MONEDA</span><span class="sxs-lookup"><span data-stu-id="83e93-116">CURRENCY</span></span>](currency.md)
  
[<span data-ttu-id="83e93-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="83e93-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="83e93-118">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="83e93-118">MAPI Structures</span></span>](mapi-structures.md)

