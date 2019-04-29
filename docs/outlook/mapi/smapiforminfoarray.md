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
ms.openlocfilehash: e274e24d9aff30bb39b1865306477164d413d9a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416975"
---
# <a name="smapiforminfoarray"></a><span data-ttu-id="9025b-103">SMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="9025b-103">SMAPIFormInfoArray</span></span>

  
  
<span data-ttu-id="9025b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9025b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9025b-105">Contiene una matriz de punteros a objetos de información de formulario.</span><span class="sxs-lookup"><span data-stu-id="9025b-105">Contains an array of pointers to form information objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9025b-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="9025b-106">Header file:</span></span>  <br/> |<span data-ttu-id="9025b-107">MAPIForm. h</span><span class="sxs-lookup"><span data-stu-id="9025b-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="9025b-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="9025b-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="9025b-109">CbMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="9025b-109">CbMAPIFormInfoArray</span></span>](cbmapiforminfoarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cForms;
  LPMAPIFORMINFO aFormInfo[MAPI_DIM];
} SMAPIFormInfoArray, FAR * LPSMAPIFORMINFOARRAY;

```

## <a name="members"></a><span data-ttu-id="9025b-110">Members</span><span class="sxs-lookup"><span data-stu-id="9025b-110">Members</span></span>

 <span data-ttu-id="9025b-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="9025b-111">**cForms**</span></span>
  
> <span data-ttu-id="9025b-112">Número de punteros en la matriz a la que señala el miembro **aFormInfo** .</span><span class="sxs-lookup"><span data-stu-id="9025b-112">Count of pointers in the array pointed to by the **aFormInfo** member.</span></span> 
    
 <span data-ttu-id="9025b-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="9025b-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="9025b-114">Puntero a una matriz de punteros a objetos de información de formulario.</span><span class="sxs-lookup"><span data-stu-id="9025b-114">Pointer to an array of pointers to form information objects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9025b-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9025b-115">Remarks</span></span>

<span data-ttu-id="9025b-116">La estructura **SMAPIFormInfoArray** se pasa como un parámetro en los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="9025b-116">The **SMAPIFormInfoArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="9025b-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="9025b-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="9025b-118">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="9025b-118">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="9025b-119">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="9025b-119">IMAPIFormMgr::SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md)
    
- [<span data-ttu-id="9025b-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="9025b-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="9025b-121">Ver también</span><span class="sxs-lookup"><span data-stu-id="9025b-121">See also</span></span>



[<span data-ttu-id="9025b-122">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="9025b-122">MAPI Structures</span></span>](mapi-structures.md)

