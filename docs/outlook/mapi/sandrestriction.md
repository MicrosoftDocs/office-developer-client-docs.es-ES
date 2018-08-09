---
title: SAndRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAndRestriction
api_type:
- COM
ms.assetid: 1b7dfe87-f87f-43e3-8332-a0d9c3f70d16
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1437130caecd57344fc171d234c5391ea92e1d4b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820566"
---
# <a name="sandrestriction"></a><span data-ttu-id="a3653-103">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="a3653-103">SAndRestriction</span></span>

  
  
<span data-ttu-id="a3653-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a3653-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a3653-105">Describe una restricción **y** , que se usa para unirse a un grupo de restricciones de uso de una operación de **AND** lógica.</span><span class="sxs-lookup"><span data-stu-id="a3653-105">Describes an **AND** restriction, which is used to join a group of restrictions using a logical **AND** operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a3653-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a3653-106">Header file:</span></span>  <br/> |<span data-ttu-id="a3653-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a3653-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a><span data-ttu-id="a3653-108">Members</span><span class="sxs-lookup"><span data-stu-id="a3653-108">Members</span></span>

 <span data-ttu-id="a3653-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="a3653-109">**cRes**</span></span>
  
> <span data-ttu-id="a3653-110">Recuento de las restricciones de búsqueda en la matriz indicada por el miembro **lpRes** .</span><span class="sxs-lookup"><span data-stu-id="a3653-110">Count of search restrictions in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="a3653-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="a3653-111">**lpRes**</span></span>
  
> <span data-ttu-id="a3653-112">Puntero a una matriz de estructuras [SRestriction](srestriction.md) que se van a combinar con una operación de **AND** lógica.</span><span class="sxs-lookup"><span data-stu-id="a3653-112">Pointer to an array of [SRestriction](srestriction.md) structures that will be combined with a logical **AND** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a3653-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a3653-113">Remarks</span></span>

<span data-ttu-id="a3653-114">El resultado de la **SAndRestriction** es TRUE si todas las restricciones de sus secundarios se evalúan como TRUE.</span><span class="sxs-lookup"><span data-stu-id="a3653-114">The result of the **SAndRestriction** is TRUE if all its child restrictions evaluate to TRUE.</span></span> <span data-ttu-id="a3653-115">Es FALSE si algún tipo de restricción secundarios se evalúa como FALSE.</span><span class="sxs-lookup"><span data-stu-id="a3653-115">It is FALSE if any child restriction evaluates to FALSE.</span></span> 
  
<span data-ttu-id="a3653-116">Para obtener una descripción de los tipos de restricciones, cómo crearlas y código de ejemplo, vea [Acerca de las restricciones](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="a3653-116">For a description of types of restrictions, how to build them, and sample code, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a3653-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3653-117">See also</span></span>



[<span data-ttu-id="a3653-118">SRestriction</span><span class="sxs-lookup"><span data-stu-id="a3653-118">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="a3653-119">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="a3653-119">MAPI Structures</span></span>](mapi-structures.md)

