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
ms.openlocfilehash: bd9bfe4d1411b84a7811235aa68728afaefe64ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439222"
---
# <a name="flatmtsidlist"></a><span data-ttu-id="c942e-103">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="c942e-103">FLATMTSIDLIST</span></span>

  
  
<span data-ttu-id="c942e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c942e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c942e-105">Contiene una matriz de estructuras [MTSID](mtsid.md) , cada una de las cuales contiene un identificador de entrada del sistema de transporte de mensajes (mts) X. 400.</span><span class="sxs-lookup"><span data-stu-id="c942e-105">Contains an array of [MTSID](mtsid.md) structures, each of which contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c942e-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c942e-106">Header file:</span></span>  <br/> |<span data-ttu-id="c942e-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c942e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c942e-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="c942e-108">Related macros:</span></span>  <br/> |<span data-ttu-id="c942e-109">[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)</span><span class="sxs-lookup"><span data-stu-id="c942e-109">[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cMTSIDs;
  ULONG cbMTSIDs;
  BYTE abMTSIDs[MAPI_DIM];
} FLATMTSIDLIST, FAR *LPFLATMTSIDLIST;

```

## <a name="members"></a><span data-ttu-id="c942e-110">Members</span><span class="sxs-lookup"><span data-stu-id="c942e-110">Members</span></span>

 <span data-ttu-id="c942e-111">**cMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="c942e-111">**cMTSIDs**</span></span>
  
> <span data-ttu-id="c942e-112">Número de estructuras **MTSID** en la matriz descrita por el miembro **abMTSIDs** .</span><span class="sxs-lookup"><span data-stu-id="c942e-112">Count of **MTSID** structures in the array described by the **abMTSIDs** member.</span></span> 
    
 <span data-ttu-id="c942e-113">**cbMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="c942e-113">**cbMTSIDs**</span></span>
  
> <span data-ttu-id="c942e-114">Número de bytes de la matriz descrita por **abMTSIDs**.</span><span class="sxs-lookup"><span data-stu-id="c942e-114">Count of bytes in the array described by **abMTSIDs**.</span></span>
    
 <span data-ttu-id="c942e-115">**abMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="c942e-115">**abMTSIDs**</span></span>
  
> <span data-ttu-id="c942e-116">Matriz de bytes que contiene una o varias estructuras **MTSID** .</span><span class="sxs-lookup"><span data-stu-id="c942e-116">Byte array that contains one or more **MTSID** structures.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c942e-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c942e-117">Remarks</span></span>

<span data-ttu-id="c942e-118">El uso de la estructura **FLATMTSIDLIST** en la mensajería X. 400 corresponde al uso de la estructura [FLATENTRYLIST](flatentrylist.md) en la mensajería MAPI.</span><span class="sxs-lookup"><span data-stu-id="c942e-118">The **FLATMTSIDLIST** structure's use in X.400 messaging corresponds to the [FLATENTRYLIST](flatentrylist.md) structure's use in MAPI messaging.</span></span> <span data-ttu-id="c942e-119">MAPI usa las estructuras **FLATMTSIDLIST** para mantener las propiedades X. 400 durante el tratamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c942e-119">MAPI uses **FLATMTSIDLIST** structures to maintain X.400 properties during message handling.</span></span> <span data-ttu-id="c942e-120">Los proveedores de servicios usan estructuras **FLATMTSIDLIST** al controlar mensajes X. 400 entrantes y salientes.</span><span class="sxs-lookup"><span data-stu-id="c942e-120">Service providers use **FLATMTSIDLIST** structures when handling incoming and outgoing X.400 messages.</span></span> 
  
<span data-ttu-id="c942e-121">En la matriz **abMTSIDs** , cada estructura **MTSID** está alineada en un límite naturalmente alineado.</span><span class="sxs-lookup"><span data-stu-id="c942e-121">In the **abMTSIDs** array, each **MTSID** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="c942e-122">Los bytes adicionales se incluyen como relleno para garantizar la alineación natural entre dos estructuras **MTSID** .</span><span class="sxs-lookup"><span data-stu-id="c942e-122">Extra bytes are included as padding to make sure natural alignment between any two **MTSID** structures.</span></span> <span data-ttu-id="c942e-123">La primera estructura **MTSID** de la matriz siempre está alineada correctamente porque el desplazamiento del miembro **abMTSIDs** es 8.</span><span class="sxs-lookup"><span data-stu-id="c942e-123">The first **MTSID** structure in the array is always aligned correctly because the offset of the **abMTSIDs** member is 8.</span></span> <span data-ttu-id="c942e-124">Para calcular el desplazamiento de la estructura siguiente, use el tamaño de la primera entrada redondeada hasta el siguiente múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="c942e-124">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="c942e-125">Use la macro [CbNewMTSID](cbnewmtsid.md) para calcular el tamaño de una estructura **MTSID** .</span><span class="sxs-lookup"><span data-stu-id="c942e-125">Use the [CbNewMTSID](cbnewmtsid.md) macro to compute the size of an **MTSID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c942e-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="c942e-126">See also</span></span>



[<span data-ttu-id="c942e-127">CbNewFLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="c942e-127">CbNewFLATMTSIDLIST</span></span>](cbnewflatmtsidlist.md)
  
[<span data-ttu-id="c942e-128">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="c942e-128">FLATENTRYLIST</span></span>](flatentrylist.md)
  
[<span data-ttu-id="c942e-129">MTSID</span><span class="sxs-lookup"><span data-stu-id="c942e-129">MTSID</span></span>](mtsid.md)


[<span data-ttu-id="c942e-130">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="c942e-130">MAPI Structures</span></span>](mapi-structures.md)

