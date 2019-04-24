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
ms.openlocfilehash: 50b6581dec8211968a49b204c6d9b1ba1c65bb62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309516"
---
# <a name="smapiformproparray"></a><span data-ttu-id="b2f78-103">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="b2f78-103">SMAPIFormPropArray</span></span>

  
  
<span data-ttu-id="b2f78-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2f78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2f78-105">Contiene una matriz de estructuras [SMAPIFormProp](smapiformprop.md) .</span><span class="sxs-lookup"><span data-stu-id="b2f78-105">Contains an array of [SMAPIFormProp](smapiformprop.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b2f78-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="b2f78-106">Header file:</span></span>  <br/> |<span data-ttu-id="b2f78-107">MAPIForm. h</span><span class="sxs-lookup"><span data-stu-id="b2f78-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="b2f78-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="b2f78-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="b2f78-109">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="b2f78-109">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cProps;
  ULONG ulPad;
  SMAPIFormProp aFormProp[MAPI_DIM];
} SMAPIFormPropArray, FAR * LPMAPIFORMPROPARRAY;

```

## <a name="members"></a><span data-ttu-id="b2f78-110">Members</span><span class="sxs-lookup"><span data-stu-id="b2f78-110">Members</span></span>

 <span data-ttu-id="b2f78-111">**cProps**</span><span class="sxs-lookup"><span data-stu-id="b2f78-111">**cProps**</span></span>
  
> <span data-ttu-id="b2f78-112">Número de propiedades con nombre de la matriz en el miembro **aFormProp** .</span><span class="sxs-lookup"><span data-stu-id="b2f78-112">Count of named properties in the array in the **aFormProp** member.</span></span> 
    
 <span data-ttu-id="b2f78-113">**ulPad**</span><span class="sxs-lookup"><span data-stu-id="b2f78-113">**ulPad**</span></span>
  
>  <span data-ttu-id="b2f78-114">Ocho bytes de espacio usado para garantizar la alineación correcta.</span><span class="sxs-lookup"><span data-stu-id="b2f78-114">Eight bytes of padding used to guarantee correct alignment.</span></span> 
    
 <span data-ttu-id="b2f78-115">**aFormProp**</span><span class="sxs-lookup"><span data-stu-id="b2f78-115">**aFormProp**</span></span>
  
> <span data-ttu-id="b2f78-116">Matriz de propiedades de formulario.</span><span class="sxs-lookup"><span data-stu-id="b2f78-116">Array of form properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b2f78-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b2f78-117">Remarks</span></span>

<span data-ttu-id="b2f78-118">La estructura **SMAPIFormPropArray** se pasa como parámetro a los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b2f78-118">The **SMAPIFormPropArray** structure is passed as a parameter to the following methods:</span></span> 
  
- [<span data-ttu-id="b2f78-119">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="b2f78-119">IMAPIFormInfo::CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md)
    
- [<span data-ttu-id="b2f78-120">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="b2f78-120">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="b2f78-121">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="b2f78-121">IMAPIFormContainer::CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a><span data-ttu-id="b2f78-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2f78-122">See also</span></span>



[<span data-ttu-id="b2f78-123">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="b2f78-123">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md)
  
[<span data-ttu-id="b2f78-124">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="b2f78-124">SMAPIFormProp</span></span>](smapiformprop.md)


[<span data-ttu-id="b2f78-125">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="b2f78-125">MAPI Structures</span></span>](mapi-structures.md)

