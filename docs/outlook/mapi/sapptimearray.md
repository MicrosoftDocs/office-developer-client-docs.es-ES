---
title: SAppTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAppTimeArray
api_type:
- COM
ms.assetid: 5a1ff95a-9862-4165-8a70-bd2eeb7fe683
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dee1de19ed61fa4f8edab69152315d77545b01b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430388"
---
# <a name="sapptimearray"></a><span data-ttu-id="2921f-103">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="2921f-103">SAppTimeArray</span></span>

  
  
<span data-ttu-id="2921f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2921f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2921f-105">Contiene una matriz de valores de tiempo.</span><span class="sxs-lookup"><span data-stu-id="2921f-105">Contains an array of time values.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2921f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="2921f-106">Header file:</span></span>  <br/> |<span data-ttu-id="2921f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2921f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a><span data-ttu-id="2921f-108">Members</span><span class="sxs-lookup"><span data-stu-id="2921f-108">Members</span></span>

 <span data-ttu-id="2921f-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="2921f-109">**cValues**</span></span>
  
> <span data-ttu-id="2921f-110">Recuento de valores en la matriz apuntada por el **miembro lpat.**</span><span class="sxs-lookup"><span data-stu-id="2921f-110">Count of values in the array pointed to by the **lpat** member.</span></span> 
    
 <span data-ttu-id="2921f-111">**lpat**</span><span class="sxs-lookup"><span data-stu-id="2921f-111">**lpat**</span></span>
  
> <span data-ttu-id="2921f-112">Puntero a una matriz de valores de tiempo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="2921f-112">Pointer to an array of application time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2921f-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2921f-113">Remarks</span></span>

<span data-ttu-id="2921f-114">La **estructura SAppTimeArray** se usa para definir propiedades de tipo PT_MV_APPTIME.</span><span class="sxs-lookup"><span data-stu-id="2921f-114">The **SAppTimeArray** structure is used to define properties of type PT_MV_APPTIME.</span></span> <span data-ttu-id="2921f-115">Para obtener más información PT_MV_APPTIME, [vea Lista de tipos de propiedad](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="2921f-115">For more information about PT_MV_APPTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2921f-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="2921f-116">See also</span></span>



[<span data-ttu-id="2921f-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="2921f-117">MAPI Structures</span></span>](mapi-structures.md)

