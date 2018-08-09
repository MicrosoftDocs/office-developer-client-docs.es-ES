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
ms.openlocfilehash: 59911531b6d8f9c094ef8563510aaa176e3a63b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820764"
---
# <a name="sshortarray"></a><span data-ttu-id="f7596-103">SShortArray</span><span class="sxs-lookup"><span data-stu-id="f7596-103">SShortArray</span></span>

  
  
<span data-ttu-id="f7596-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f7596-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f7596-105">Contiene una matriz de valores de entero sin signo que se utilizan para describir una propiedad de tipo PT_MV_SHORT.</span><span class="sxs-lookup"><span data-stu-id="f7596-105">Contains an array of unsigned integer values that are used to describe a property of type PT_MV_SHORT.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f7596-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="f7596-106">Header file:</span></span>  <br/> |<span data-ttu-id="f7596-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f7596-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a><span data-ttu-id="f7596-108">Members</span><span class="sxs-lookup"><span data-stu-id="f7596-108">Members</span></span>

 <span data-ttu-id="f7596-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="f7596-109">**cValues**</span></span>
  
> <span data-ttu-id="f7596-110">Recuento de valores de la matriz indicada por el miembro **lpp** .</span><span class="sxs-lookup"><span data-stu-id="f7596-110">Count of values in the array pointed to by the **lpi** member.</span></span> 
    
 <span data-ttu-id="f7596-111">**lpp**</span><span class="sxs-lookup"><span data-stu-id="f7596-111">**lpi**</span></span>
  
> <span data-ttu-id="f7596-112">Puntero a una matriz de valores enteros sin signo.</span><span class="sxs-lookup"><span data-stu-id="f7596-112">Pointer to an array of unsigned integer values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f7596-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f7596-113">Remarks</span></span>

<span data-ttu-id="f7596-114">Para obtener más información acerca de PT_MV_SHORT y otros tipos de propiedades, vea [Tipos de propiedades](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="f7596-114">For more information about PT_MV_SHORT and other property types, see [Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f7596-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7596-115">See also</span></span>



[<span data-ttu-id="f7596-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f7596-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="f7596-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="f7596-117">MAPI Structures</span></span>](mapi-structures.md)

