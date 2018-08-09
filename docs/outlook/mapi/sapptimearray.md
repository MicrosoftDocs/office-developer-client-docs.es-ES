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
ms.openlocfilehash: 834a7141f0e7150140fa27c21d88db422d6f5561
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820548"
---
# <a name="sapptimearray"></a><span data-ttu-id="d7c40-103">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="d7c40-103">SAppTimeArray</span></span>

  
  
<span data-ttu-id="d7c40-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d7c40-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d7c40-105">Contiene una matriz de valores de hora.</span><span class="sxs-lookup"><span data-stu-id="d7c40-105">Contains an array of time values.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d7c40-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d7c40-106">Header file:</span></span>  <br/> |<span data-ttu-id="d7c40-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d7c40-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a><span data-ttu-id="d7c40-108">Members</span><span class="sxs-lookup"><span data-stu-id="d7c40-108">Members</span></span>

 <span data-ttu-id="d7c40-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="d7c40-109">**cValues**</span></span>
  
> <span data-ttu-id="d7c40-110">Recuento de valores de la matriz indicada por el miembro **lpat** .</span><span class="sxs-lookup"><span data-stu-id="d7c40-110">Count of values in the array pointed to by the **lpat** member.</span></span> 
    
 <span data-ttu-id="d7c40-111">**lpat**</span><span class="sxs-lookup"><span data-stu-id="d7c40-111">**lpat**</span></span>
  
> <span data-ttu-id="d7c40-112">Puntero a una matriz de valores de tiempo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="d7c40-112">Pointer to an array of application time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d7c40-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d7c40-113">Remarks</span></span>

<span data-ttu-id="d7c40-114">La estructura **SAppTimeArray** se usa para definir las propiedades de tipo PT_MV_APPTIME.</span><span class="sxs-lookup"><span data-stu-id="d7c40-114">The **SAppTimeArray** structure is used to define properties of type PT_MV_APPTIME.</span></span> <span data-ttu-id="d7c40-115">Para obtener más información sobre PT_MV_APPTIME, vea la [Lista de tipos de propiedad](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="d7c40-115">For more information about PT_MV_APPTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d7c40-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7c40-116">See also</span></span>



[<span data-ttu-id="d7c40-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="d7c40-117">MAPI Structures</span></span>](mapi-structures.md)

