---
title: Actualización de las propiedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: faafde3d-3989-4182-91f1-a0cf0f1b5388
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6c2c733b87b85971fad8060040e713b41b0f5616
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360518"
---
# <a name="updating-mapi-properties"></a><span data-ttu-id="1619c-103">Actualización de las propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1619c-103">Updating MAPI properties</span></span>

<span data-ttu-id="1619c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1619c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1619c-105">Los clientes y los proveedores de servicios pueden actualizar un valor de propiedad llamando a:</span><span class="sxs-lookup"><span data-stu-id="1619c-105">Clients and service providers can update a property value by calling:</span></span>
  
- <span data-ttu-id="1619c-106">El método [IMAPIProp:: SetProps](imapiprop-setprops.md) de un objeto para actualizar el valor de una o varias de las propiedades de un objeto.</span><span class="sxs-lookup"><span data-stu-id="1619c-106">An object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to update the value of one or more of an object's properties.</span></span> 
    
- <span data-ttu-id="1619c-107">La función [HrSetOneProp](hrsetoneprop.md) para actualizar sólo una propiedad a la vez.</span><span class="sxs-lookup"><span data-stu-id="1619c-107">The [HrSetOneProp](hrsetoneprop.md) function to update only one property at a time.</span></span> <span data-ttu-id="1619c-108">Use **HrSetOneProp** solo si el objeto de destino es local; Esta función puede provocar una degradación del rendimiento cuando se usa con objetos remotos.</span><span class="sxs-lookup"><span data-stu-id="1619c-108">Use **HrSetOneProp** only if the target object is local; this function can cause performance degradation when used with remote objects.</span></span> 
    
<span data-ttu-id="1619c-109">El siguiente procedimiento muestra cómo usar **SetProps** para actualizar la clase de mensaje o la propiedad PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="1619c-109">The following procedure illustrates how to use **SetProps** to update the message class, or PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property, of a message.</span></span> 
  
### <a name="to-update-the-message-class-of-a-message"></a><span data-ttu-id="1619c-110">Para actualizar la clase de mensaje de un mensaje</span><span class="sxs-lookup"><span data-stu-id="1619c-110">To update the message class of a message</span></span> 
  
1. <span data-ttu-id="1619c-111">Asigne una estructura [SPropValue](spropvalue.md) para la clase Message y establezca sus miembros según corresponda.</span><span class="sxs-lookup"><span data-stu-id="1619c-111">Allocate an [SPropValue](spropvalue.md) structure for the message class and set its members as appropriate.</span></span> 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. <span data-ttu-id="1619c-112">Llame al método **IMAPIProp:: SetProps** del mensaje para establecer la nueva clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="1619c-112">Call the message's **IMAPIProp::SetProps** method to set the new message class.</span></span> 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a><span data-ttu-id="1619c-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="1619c-113">See also</span></span>

- [<span data-ttu-id="1619c-114">Información general sobre MAPI (propiedad)</span><span class="sxs-lookup"><span data-stu-id="1619c-114">MAPI Property Overview</span></span>](mapi-property-overview.md)

