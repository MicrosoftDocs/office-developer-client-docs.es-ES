---
title: FLATMTSIDLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATMTSIDLIST
api_type:
- COM
ms.assetid: b66c2815-72bc-4535-b34c-899bb830f29e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0f1495549df751c59ab84e2b16fffbaf2f4f9fa5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574723"
---
# <a name="flatmtsidlist"></a><span data-ttu-id="a0068-103">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="a0068-103">FLATMTSIDLIST</span></span>

  
  
<span data-ttu-id="a0068-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0068-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0068-105">Contiene una matriz de estructuras [MTSID](mtsid.md) , cada uno de los cuales contiene un identificador de entrada del sistema (MTS) de transporte de mensaje X.400.</span><span class="sxs-lookup"><span data-stu-id="a0068-105">Contains an array of [MTSID](mtsid.md) structures, each of which contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0068-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a0068-106">Header file:</span></span>  <br/> |<span data-ttu-id="a0068-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a0068-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a0068-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="a0068-108">Related macros:</span></span>  <br/> |<span data-ttu-id="a0068-109">[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)</span><span class="sxs-lookup"><span data-stu-id="a0068-109">[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cMTSIDs;
  ULONG cbMTSIDs;
  BYTE abMTSIDs[MAPI_DIM];
} FLATMTSIDLIST, FAR *LPFLATMTSIDLIST;

```

## <a name="members"></a><span data-ttu-id="a0068-110">Members</span><span class="sxs-lookup"><span data-stu-id="a0068-110">Members</span></span>

 <span data-ttu-id="a0068-111">**cMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="a0068-111">**cMTSIDs**</span></span>
  
> <span data-ttu-id="a0068-112">Recuento de estructuras **MTSID** en la matriz descritos por el miembro **abMTSIDs** .</span><span class="sxs-lookup"><span data-stu-id="a0068-112">Count of **MTSID** structures in the array described by the **abMTSIDs** member.</span></span> 
    
 <span data-ttu-id="a0068-113">**cbMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="a0068-113">**cbMTSIDs**</span></span>
  
> <span data-ttu-id="a0068-114">Número de bytes de la matriz descritos por **abMTSIDs**.</span><span class="sxs-lookup"><span data-stu-id="a0068-114">Count of bytes in the array described by **abMTSIDs**.</span></span>
    
 <span data-ttu-id="a0068-115">**abMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="a0068-115">**abMTSIDs**</span></span>
  
> <span data-ttu-id="a0068-116">Matriz de bytes que contiene una o más estructuras **MTSID** .</span><span class="sxs-lookup"><span data-stu-id="a0068-116">Byte array that contains one or more **MTSID** structures.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a0068-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a0068-117">Remarks</span></span>

<span data-ttu-id="a0068-118">Uso de la estructura **FLATMTSIDLIST** en mensajería X.400 corresponde al uso de la estructura [FLATENTRYLIST](flatentrylist.md) de mensajería MAPI.</span><span class="sxs-lookup"><span data-stu-id="a0068-118">The **FLATMTSIDLIST** structure's use in X.400 messaging corresponds to the [FLATENTRYLIST](flatentrylist.md) structure's use in MAPI messaging.</span></span> <span data-ttu-id="a0068-119">MAPI utiliza estructuras **FLATMTSIDLIST** para mantener las propiedades de X.400 durante el control de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a0068-119">MAPI uses **FLATMTSIDLIST** structures to maintain X.400 properties during message handling.</span></span> <span data-ttu-id="a0068-120">Proveedores de servicios utilizan estructuras **FLATMTSIDLIST** al tratamiento de mensajes X.400 entrantes y salientes.</span><span class="sxs-lookup"><span data-stu-id="a0068-120">Service providers use **FLATMTSIDLIST** structures when handling incoming and outgoing X.400 messages.</span></span> 
  
<span data-ttu-id="a0068-121">En la matriz **abMTSIDs** , cada estructura **MTSID** se alinea en un límite alineado con naturalidad.</span><span class="sxs-lookup"><span data-stu-id="a0068-121">In the **abMTSIDs** array, each **MTSID** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="a0068-122">Bytes adicionales se incluyen como relleno para realizar la alineación natural seguro entre los dos estructuras **MTSID** .</span><span class="sxs-lookup"><span data-stu-id="a0068-122">Extra bytes are included as padding to make sure natural alignment between any two **MTSID** structures.</span></span> <span data-ttu-id="a0068-123">La primera estructura **MTSID** en la matriz siempre se alinea correctamente debido a que el desplazamiento del miembro **abMTSIDs** es 8.</span><span class="sxs-lookup"><span data-stu-id="a0068-123">The first **MTSID** structure in the array is always aligned correctly because the offset of the **abMTSIDs** member is 8.</span></span> <span data-ttu-id="a0068-124">Para calcular el desplazamiento de la estructura siguiente, utilice el tamaño de la primera entrada que se redondea hacia arriba hasta el próximo múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="a0068-124">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="a0068-125">Utilice la macro [CbNewMTSID](cbnewmtsid.md) para calcular el tamaño de una estructura **MTSID** .</span><span class="sxs-lookup"><span data-stu-id="a0068-125">Use the [CbNewMTSID](cbnewmtsid.md) macro to compute the size of an **MTSID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a0068-126">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="a0068-126">See also</span></span>



[<span data-ttu-id="a0068-127">CbNewFLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="a0068-127">CbNewFLATMTSIDLIST</span></span>](cbnewflatmtsidlist.md)
  
[<span data-ttu-id="a0068-128">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="a0068-128">FLATENTRYLIST</span></span>](flatentrylist.md)
  
[<span data-ttu-id="a0068-129">MTSID</span><span class="sxs-lookup"><span data-stu-id="a0068-129">MTSID</span></span>](mtsid.md)


[<span data-ttu-id="a0068-130">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="a0068-130">MAPI Structures</span></span>](mapi-structures.md)

