---
title: SPropAttrArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropAttrArray
api_type:
- COM
ms.assetid: 30dd19d9-0840-49e9-aec6-ec8d19b1f91d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a8f4e62a8eb1b5e61cb0223c66b921e15ab9423b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577684"
---
# <a name="spropattrarray"></a><span data-ttu-id="7f596-103">SPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="7f596-103">SPropAttrArray</span></span>

  
  
<span data-ttu-id="7f596-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f596-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f596-105">Contiene una lista de atributos para las propiedades de un objeto.</span><span class="sxs-lookup"><span data-stu-id="7f596-105">Contains a list of attributes for properties of an object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7f596-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="7f596-106">Header file:</span></span>  <br/> |<span data-ttu-id="7f596-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="7f596-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="7f596-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="7f596-108">Related macros:</span></span>  <br/> |<span data-ttu-id="7f596-109">[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md)</span><span class="sxs-lookup"><span data-stu-id="7f596-109">[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cValues;
  ULONG aPropAttr[MAPI_DIM];
} SPropAttrArray, FAR *LPSPropAttrArray;

```

## <a name="members"></a><span data-ttu-id="7f596-110">Members</span><span class="sxs-lookup"><span data-stu-id="7f596-110">Members</span></span>

 <span data-ttu-id="7f596-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="7f596-111">**cValues**</span></span>
  
> <span data-ttu-id="7f596-112">Recuento de atributos de la propiedad en el miembro **aPropAttr** .</span><span class="sxs-lookup"><span data-stu-id="7f596-112">Count of property attributes in the **aPropAttr** member.</span></span> 
    
 <span data-ttu-id="7f596-113">**aPropAttr**</span><span class="sxs-lookup"><span data-stu-id="7f596-113">**aPropAttr**</span></span>
  
> <span data-ttu-id="7f596-114">Una matriz de atributos de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="7f596-114">An array of property attributes.</span></span> <span data-ttu-id="7f596-115">Los valores válidos para los atributos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="7f596-115">Valid values for attributes are as follows:</span></span>
    
    - <span data-ttu-id="7f596-116">PROPATTR_MANDATORY</span><span class="sxs-lookup"><span data-stu-id="7f596-116">PROPATTR_MANDATORY</span></span>
    
    - <span data-ttu-id="7f596-117">PROPATTR_READABLE</span><span class="sxs-lookup"><span data-stu-id="7f596-117">PROPATTR_READABLE</span></span>
    
    - <span data-ttu-id="7f596-118">PROPATTR_WRITEABLE</span><span class="sxs-lookup"><span data-stu-id="7f596-118">PROPATTR_WRITEABLE</span></span>
    
    - <span data-ttu-id="7f596-119">PROPATTR_NOT_PRESENT</span><span class="sxs-lookup"><span data-stu-id="7f596-119">PROPATTR_NOT_PRESENT</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7f596-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7f596-120">Remarks</span></span>

<span data-ttu-id="7f596-121">La estructura **SPropAttrArray** se usa en los objetos de datos de propiedad que implementan el [IPropData: IMAPIProp](ipropdataimapiprop.md) interfaz.</span><span class="sxs-lookup"><span data-stu-id="7f596-121">The **SPropAttrArray** structure is used by property data objects that implement the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> <span data-ttu-id="7f596-122">También se usa la implementación de MAPI de [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) es decir, en función de almacenamiento estructurado.</span><span class="sxs-lookup"><span data-stu-id="7f596-122">It is also used by MAPI's implementation of [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) that is based on structured storage.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7f596-123">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="7f596-123">See also</span></span>



[<span data-ttu-id="7f596-124">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7f596-124">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="7f596-125">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7f596-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="7f596-126">CbNewSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="7f596-126">CbNewSPropAttrArray</span></span>](cbnewspropattrarray.md)
  
[<span data-ttu-id="7f596-127">CbSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="7f596-127">CbSPropAttrArray</span></span>](cbspropattrarray.md)


[<span data-ttu-id="7f596-128">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="7f596-128">MAPI Structures</span></span>](mapi-structures.md)

