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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439404"
---
# <a name="scurrencyarray"></a><span data-ttu-id="17781-103">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="17781-103">SCurrencyArray</span></span>

  
  
<span data-ttu-id="17781-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17781-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17781-105">Contiene una matriz de valores de moneda que se usan para describir una propiedad de tipo PT_MV_CURRENCY.</span><span class="sxs-lookup"><span data-stu-id="17781-105">Contains an array of currency values that are used to describe a property of type PT_MV_CURRENCY.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="17781-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="17781-106">Header file:</span></span>  <br/> |<span data-ttu-id="17781-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="17781-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a><span data-ttu-id="17781-108">Members</span><span class="sxs-lookup"><span data-stu-id="17781-108">Members</span></span>

 <span data-ttu-id="17781-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="17781-109">**cValues**</span></span>
  
> <span data-ttu-id="17781-110">Recuento de valores en la matriz apuntada por el **miembro lpcur.**</span><span class="sxs-lookup"><span data-stu-id="17781-110">Count of values in the array pointed to by the **lpcur** member.</span></span> 
    
 <span data-ttu-id="17781-111">**lpcur**</span><span class="sxs-lookup"><span data-stu-id="17781-111">**lpcur**</span></span>
  
> <span data-ttu-id="17781-112">Puntero a una matriz de [estructuras CURRENCY](currency.md) que contienen los valores de moneda.</span><span class="sxs-lookup"><span data-stu-id="17781-112">Pointer to an array of [CURRENCY](currency.md) structures that contain the currency values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="17781-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="17781-113">Remarks</span></span>

<span data-ttu-id="17781-114">Para obtener información sobre PT_MV_CURRENCY, [vea List of Property Types](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="17781-114">For information about PT_MV_CURRENCY, see [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="17781-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="17781-115">See also</span></span>



[<span data-ttu-id="17781-116">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="17781-116">CURRENCY</span></span>](currency.md)
  
[<span data-ttu-id="17781-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="17781-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="17781-118">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="17781-118">MAPI Structures</span></span>](mapi-structures.md)

