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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 32aa91d43e4674c0de20a0dbb670dcb9e2c782cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820734"
---
# <a name="spropproblem"></a><span data-ttu-id="1dd46-103">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="1dd46-103">SPropProblem</span></span>

  
  
<span data-ttu-id="1dd46-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1dd46-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1dd46-105">Describe un error que se relacionan con una operación que implica una propiedad.</span><span class="sxs-lookup"><span data-stu-id="1dd46-105">Describes an error that relate to an operation involving a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1dd46-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="1dd46-106">Header file:</span></span>  <br/> |<span data-ttu-id="1dd46-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1dd46-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropProblem
{
  ULONG ulIndex;
  ULONG ulPropTag;
  SCODE scode;
} SPropProblem, FAR *LPSPropProblem;

```

## <a name="members"></a><span data-ttu-id="1dd46-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="1dd46-108">Members</span></span>

 <span data-ttu-id="1dd46-109">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="1dd46-109">**ulIndex**</span></span>
  
> <span data-ttu-id="1dd46-110">Un índice en una matriz de etiquetas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="1dd46-110">An index in an array of property tags.</span></span>
    
 <span data-ttu-id="1dd46-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="1dd46-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="1dd46-112">Etiqueta de propiedad de la propiedad que tiene el error.</span><span class="sxs-lookup"><span data-stu-id="1dd46-112">Property tag for the property that has the error.</span></span>
    
 <span data-ttu-id="1dd46-113">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="1dd46-113">**scode**</span></span>
  
> <span data-ttu-id="1dd46-114">Valor de error que describe el problema con la propiedad.</span><span class="sxs-lookup"><span data-stu-id="1dd46-114">Error value describing the problem with the property.</span></span> <span data-ttu-id="1dd46-115">Este valor puede ser cualquier valor [SCODE](scode.md) de MAPI.</span><span class="sxs-lookup"><span data-stu-id="1dd46-115">This value can be any MAPI [SCODE](scode.md) value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1dd46-116">Notas</span><span class="sxs-lookup"><span data-stu-id="1dd46-116">Remarks</span></span>

<span data-ttu-id="1dd46-117">Se devuelve una matriz de estructuras **SPropProblem** entre los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="1dd46-117">An array of **SPropProblem** structures is returned from the following methods:</span></span> 
  
- [<span data-ttu-id="1dd46-118">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="1dd46-118">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
    
- [<span data-ttu-id="1dd46-119">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="1dd46-119">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
    
- [<span data-ttu-id="1dd46-120">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="1dd46-120">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
    
- [<span data-ttu-id="1dd46-121">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="1dd46-121">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="1dd46-122">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="1dd46-122">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
- [<span data-ttu-id="1dd46-123">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="1dd46-123">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="1dd46-124">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="1dd46-124">IPropData::HrAddObjProps</span></span>](ipropdata-hraddobjprops.md)
    
<span data-ttu-id="1dd46-125">Una estructura **SPropProblem** contiene un valor de error **SCODE** que dan como resultado de una operación intenta modificar o eliminar una propiedad MAPI.</span><span class="sxs-lookup"><span data-stu-id="1dd46-125">An **SPropProblem** structure contains an **SCODE** error value that results from an operation trying to modify or delete a MAPI property.</span></span> 
  
<span data-ttu-id="1dd46-126">Para obtener más información acerca de cómo funciona la estructura **SPropProblem** con errores relacionados con las propiedades, vea [Propiedades de nombre de MAPI](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="1dd46-126">For more information about how the **SPropProblem** structure works with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1dd46-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="1dd46-127">See also</span></span>



[<span data-ttu-id="1dd46-128">SCODE</span><span class="sxs-lookup"><span data-stu-id="1dd46-128">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="1dd46-129">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="1dd46-129">SPropProblemArray</span></span>](spropproblemarray.md)


[<span data-ttu-id="1dd46-130">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="1dd46-130">MAPI Structures</span></span>](mapi-structures.md)

