---
title: SMAPIFormPropArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormPropArray
api_type:
- COM
ms.assetid: bb243bc4-4974-4ad6-aa76-2426c1ebe84b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d907f2e8ecb9b6126898ff35b13427b088af9561
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820710"
---
# <a name="smapiformproparray"></a><span data-ttu-id="62be2-103">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="62be2-103">SMAPIFormPropArray</span></span>

  
  
<span data-ttu-id="62be2-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="62be2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="62be2-105">Contiene una matriz de estructuras [SMAPIFormProp](smapiformprop.md) .</span><span class="sxs-lookup"><span data-stu-id="62be2-105">Contains an array of [SMAPIFormProp](smapiformprop.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="62be2-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="62be2-106">Header file:</span></span>  <br/> |<span data-ttu-id="62be2-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="62be2-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="62be2-108">Macro relacionado:</span><span class="sxs-lookup"><span data-stu-id="62be2-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="62be2-109">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="62be2-109">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cProps;
  ULONG ulPad;
  SMAPIFormProp aFormProp[MAPI_DIM];
} SMAPIFormPropArray, FAR * LPMAPIFORMPROPARRAY;

```

## <a name="members"></a><span data-ttu-id="62be2-110">Members</span><span class="sxs-lookup"><span data-stu-id="62be2-110">Members</span></span>

 <span data-ttu-id="62be2-111">**cProps**</span><span class="sxs-lookup"><span data-stu-id="62be2-111">**cProps**</span></span>
  
> <span data-ttu-id="62be2-112">Recuento de propiedades con nombre en la matriz en el miembro **aFormProp** .</span><span class="sxs-lookup"><span data-stu-id="62be2-112">Count of named properties in the array in the **aFormProp** member.</span></span> 
    
 <span data-ttu-id="62be2-113">**ulPad**</span><span class="sxs-lookup"><span data-stu-id="62be2-113">**ulPad**</span></span>
  
>  <span data-ttu-id="62be2-114">Ocho bytes de relleno utilizado para garantizar la alineación correcta.</span><span class="sxs-lookup"><span data-stu-id="62be2-114">Eight bytes of padding used to guarantee correct alignment.</span></span> 
    
 <span data-ttu-id="62be2-115">**aFormProp**</span><span class="sxs-lookup"><span data-stu-id="62be2-115">**aFormProp**</span></span>
  
> <span data-ttu-id="62be2-116">Matriz de las propiedades del formulario.</span><span class="sxs-lookup"><span data-stu-id="62be2-116">Array of form properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="62be2-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="62be2-117">Remarks</span></span>

<span data-ttu-id="62be2-118">La estructura **SMAPIFormPropArray** se pasa como parámetro a los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="62be2-118">The **SMAPIFormPropArray** structure is passed as a parameter to the following methods:</span></span> 
  
- [<span data-ttu-id="62be2-119">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="62be2-119">IMAPIFormInfo::CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md)
    
- [<span data-ttu-id="62be2-120">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="62be2-120">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="62be2-121">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="62be2-121">IMAPIFormContainer::CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a><span data-ttu-id="62be2-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="62be2-122">See also</span></span>



[<span data-ttu-id="62be2-123">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="62be2-123">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md)
  
[<span data-ttu-id="62be2-124">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="62be2-124">SMAPIFormProp</span></span>](smapiformprop.md)


[<span data-ttu-id="62be2-125">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="62be2-125">MAPI Structures</span></span>](mapi-structures.md)

