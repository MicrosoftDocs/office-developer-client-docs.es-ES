---
title: SPropProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblem
api_type:
- COM
ms.assetid: 55943197-fd11-442d-bb4b-0bff565b846e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b3a0872c94459fc7c24d13e35adf335ef8012182
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407777"
---
# <a name="spropproblem"></a><span data-ttu-id="fcd55-103">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="fcd55-103">SPropProblem</span></span>

  
  
<span data-ttu-id="fcd55-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fcd55-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fcd55-105">Describe un error relacionado con una operación que implica una propiedad.</span><span class="sxs-lookup"><span data-stu-id="fcd55-105">Describes an error that relate to an operation involving a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fcd55-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="fcd55-106">Header file:</span></span>  <br/> |<span data-ttu-id="fcd55-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fcd55-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropProblem
{
  ULONG ulIndex;
  ULONG ulPropTag;
  SCODE scode;
} SPropProblem, FAR *LPSPropProblem;

```

## <a name="members"></a><span data-ttu-id="fcd55-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="fcd55-108">Members</span></span>

 <span data-ttu-id="fcd55-109">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="fcd55-109">**ulIndex**</span></span>
  
> <span data-ttu-id="fcd55-110">Índice de una matriz de etiquetas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="fcd55-110">An index in an array of property tags.</span></span>
    
 <span data-ttu-id="fcd55-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="fcd55-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="fcd55-112">Etiqueta de propiedad de la propiedad que tiene el error.</span><span class="sxs-lookup"><span data-stu-id="fcd55-112">Property tag for the property that has the error.</span></span>
    
 <span data-ttu-id="fcd55-113">**scode**</span><span class="sxs-lookup"><span data-stu-id="fcd55-113">**scode**</span></span>
  
> <span data-ttu-id="fcd55-114">Valor de error que describe el problema con la propiedad.</span><span class="sxs-lookup"><span data-stu-id="fcd55-114">Error value describing the problem with the property.</span></span> <span data-ttu-id="fcd55-115">Este valor puede ser cualquier valor [de MAPI SCODE.](scode.md)</span><span class="sxs-lookup"><span data-stu-id="fcd55-115">This value can be any MAPI [SCODE](scode.md) value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fcd55-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fcd55-116">Remarks</span></span>

<span data-ttu-id="fcd55-117">Se devuelve una **matriz de estructuras SPropProblem** de los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="fcd55-117">An array of **SPropProblem** structures is returned from the following methods:</span></span> 
  
- [<span data-ttu-id="fcd55-118">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="fcd55-118">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
    
- [<span data-ttu-id="fcd55-119">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="fcd55-119">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
    
- [<span data-ttu-id="fcd55-120">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="fcd55-120">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
    
- [<span data-ttu-id="fcd55-121">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="fcd55-121">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="fcd55-122">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="fcd55-122">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
- [<span data-ttu-id="fcd55-123">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="fcd55-123">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="fcd55-124">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="fcd55-124">IPropData::HrAddObjProps</span></span>](ipropdata-hraddobjprops.md)
    
<span data-ttu-id="fcd55-125">Una **estructura SPropProblem** contiene un valor de error **SCODE** que resulta de una operación que intenta modificar o eliminar una propiedad MAPI.</span><span class="sxs-lookup"><span data-stu-id="fcd55-125">An **SPropProblem** structure contains an **SCODE** error value that results from an operation trying to modify or delete a MAPI property.</span></span> 
  
<span data-ttu-id="fcd55-126">Para obtener más información acerca de cómo funciona la estructura **SPropProblem** con errores relacionados con las propiedades, vea [MAPI Named Properties](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="fcd55-126">For more information about how the **SPropProblem** structure works with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fcd55-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fcd55-127">See also</span></span>



[<span data-ttu-id="fcd55-128">SCODE</span><span class="sxs-lookup"><span data-stu-id="fcd55-128">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="fcd55-129">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="fcd55-129">SPropProblemArray</span></span>](spropproblemarray.md)


[<span data-ttu-id="fcd55-130">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="fcd55-130">MAPI Structures</span></span>](mapi-structures.md)

