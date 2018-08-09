---
title: SMAPIFormInfoArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormInfoArray
api_type:
- COM
ms.assetid: f5eeb75d-debb-4ac1-b239-e8e852460ce0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6389bbf2094f51711d80896db0db9862059826cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820718"
---
# <a name="smapiforminfoarray"></a><span data-ttu-id="52e78-103">SMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="52e78-103">SMAPIFormInfoArray</span></span>

  
  
<span data-ttu-id="52e78-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="52e78-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="52e78-105">Contiene una matriz de punteros a objetos de información del formulario.</span><span class="sxs-lookup"><span data-stu-id="52e78-105">Contains an array of pointers to form information objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="52e78-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="52e78-106">Header file:</span></span>  <br/> |<span data-ttu-id="52e78-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="52e78-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="52e78-108">Macro relacionado:</span><span class="sxs-lookup"><span data-stu-id="52e78-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="52e78-109">CbMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="52e78-109">CbMAPIFormInfoArray</span></span>](cbmapiforminfoarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cForms;
  LPMAPIFORMINFO aFormInfo[MAPI_DIM];
} SMAPIFormInfoArray, FAR * LPSMAPIFORMINFOARRAY;

```

## <a name="members"></a><span data-ttu-id="52e78-110">Members</span><span class="sxs-lookup"><span data-stu-id="52e78-110">Members</span></span>

 <span data-ttu-id="52e78-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="52e78-111">**cForms**</span></span>
  
> <span data-ttu-id="52e78-112">Recuento de punteros de la matriz indicada por el miembro **aFormInfo** .</span><span class="sxs-lookup"><span data-stu-id="52e78-112">Count of pointers in the array pointed to by the **aFormInfo** member.</span></span> 
    
 <span data-ttu-id="52e78-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="52e78-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="52e78-114">Puntero a una matriz de punteros a objetos de información del formulario.</span><span class="sxs-lookup"><span data-stu-id="52e78-114">Pointer to an array of pointers to form information objects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="52e78-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="52e78-115">Remarks</span></span>

<span data-ttu-id="52e78-116">La estructura **SMAPIFormInfoArray** se pasa como un parámetro en los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="52e78-116">The **SMAPIFormInfoArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="52e78-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="52e78-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="52e78-118">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="52e78-118">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="52e78-119">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="52e78-119">IMAPIFormMgr::SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md)
    
- [<span data-ttu-id="52e78-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="52e78-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="52e78-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="52e78-121">See also</span></span>



[<span data-ttu-id="52e78-122">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="52e78-122">MAPI Structures</span></span>](mapi-structures.md)

