---
title: Sintaxis de secuencia TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1353d494-c266-4715-afe7-14543a1bbe1b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 12d2a92ff80897456707c7ab8af8f704605c85d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423030"
---
# <a name="tnef-stream-syntax"></a><span data-ttu-id="3b571-103">Sintaxis de secuencia TNEF</span><span class="sxs-lookup"><span data-stu-id="3b571-103">TNEF Stream Syntax</span></span>

  
  
<span data-ttu-id="3b571-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b571-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b571-105">En este tema se presenta una Bakus-Nauer como la descripción de la sintaxis de secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="3b571-105">This topic presents a Bakus-Nauer like description of the TNEF stream syntax.</span></span> <span data-ttu-id="3b571-106">En esta descripción, los elementos noterminales que tienen una definición adicional están en cursiva.</span><span class="sxs-lookup"><span data-stu-id="3b571-106">In this description, nonterminal elements that have a further definition are in italics.</span></span> <span data-ttu-id="3b571-107">Las constantes y los elementos literales están en negrita.</span><span class="sxs-lookup"><span data-stu-id="3b571-107">Constants and literal items are in bold.</span></span> <span data-ttu-id="3b571-108">Las secuencias de elementos se enumeran en orden en una sola línea.</span><span class="sxs-lookup"><span data-stu-id="3b571-108">Sequences of elements are listed in order on a single line.</span></span> <span data-ttu-id="3b571-109">Por ejemplo, el  _elemento Stream_ consta de la constante **TNEF_SIGNATURE**, seguida de  _una tecla_, seguida de un objeto  _Object_.</span><span class="sxs-lookup"><span data-stu-id="3b571-109">For example, the  _Stream_ item consists of the constant **TNEF_SIGNATURE**, followed by a  _Key_, followed by an  _Object_.</span></span> <span data-ttu-id="3b571-110">Cuando un elemento tiene más de una implementación posible, las alternativas se enumeran en líneas consecutivas.</span><span class="sxs-lookup"><span data-stu-id="3b571-110">When an item has more than one possible implementation, the alternatives are listed on consecutive lines.</span></span> <span data-ttu-id="3b571-111">Por ejemplo, un _objeto puede_ constar de  un Message_Seq _,_ un Message_Seq seguido de un _Attach_Seq_ o simplemente un _Attach_Seq_.</span><span class="sxs-lookup"><span data-stu-id="3b571-111">For example, an  _Object_ can consist of a  _Message_Seq_, a  _Message_Seq_ followed by an  _Attach_Seq_, or just an  _Attach_Seq_.</span></span>
  
 <span data-ttu-id="3b571-112">_TNEF_Stream:_</span><span class="sxs-lookup"><span data-stu-id="3b571-112">_TNEF_Stream:_</span></span>
  
> <span data-ttu-id="3b571-113">**TNEF_SIGNATURE** _key (objeto)_ </span><span class="sxs-lookup"><span data-stu-id="3b571-113">**TNEF_SIGNATURE** _Key_ _Object_</span></span>
    
 <span data-ttu-id="3b571-114">_Clave:_</span><span class="sxs-lookup"><span data-stu-id="3b571-114">_Key:_</span></span>
  
> <span data-ttu-id="3b571-115">un entero sin signo de 16 bits distinto de cero</span><span class="sxs-lookup"><span data-stu-id="3b571-115">a nonzero 16-bit unsigned integer</span></span>
    
<span data-ttu-id="3b571-116">Los transportes habilitados para TNEF generan este valor antes de usar la implementación de TNEF para generar una secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="3b571-116">TNEF enabled transports generate this value before using the TNEF implementation to generate a TNEF stream.</span></span>
  
 <span data-ttu-id="3b571-117">_Objeto:_</span><span class="sxs-lookup"><span data-stu-id="3b571-117">_Object:_</span></span>
  
>  <span data-ttu-id="3b571-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span><span class="sxs-lookup"><span data-stu-id="3b571-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span></span>
    
 <span data-ttu-id="3b571-119">_Message_Seq:_</span><span class="sxs-lookup"><span data-stu-id="3b571-119">_Message_Seq:_</span></span>
  
>  <span data-ttu-id="3b571-120">_attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="3b571-120">_attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="3b571-121">_attTnefVersion:_</span><span class="sxs-lookup"><span data-stu-id="3b571-121">_attTnefVersion:_</span></span>
  
> <span data-ttu-id="3b571-122">LVL_MESSAGE suma de comprobación de 0x00010000 **attTnefVersion sizeof(ULONG)** </span><span class="sxs-lookup"><span data-stu-id="3b571-122">**LVL_MESSAGE attTnefVersion sizeof(ULONG)** **0x00010000** checksum</span></span> 
    
 <span data-ttu-id="3b571-123">_attMessageClass:_</span><span class="sxs-lookup"><span data-stu-id="3b571-123">_attMessageClass:_</span></span>
  
> <span data-ttu-id="3b571-124">**LVL_MESSAGE suma de comprobación msg_class_length msg_class attMessageClass** </span><span class="sxs-lookup"><span data-stu-id="3b571-124">**LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ checksum</span></span> 
    
 <span data-ttu-id="3b571-125">_Msg_Attribute_Seq:_</span><span class="sxs-lookup"><span data-stu-id="3b571-125">_Msg_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="3b571-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="3b571-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="3b571-127">_Msg_Attribute:_</span><span class="sxs-lookup"><span data-stu-id="3b571-127">_Msg_Attribute:_</span></span>
  
> <span data-ttu-id="3b571-128">**LVL_MESSAGE** suma de comprobación de atributo-ID de atributo-longitud de atributo-datos</span><span class="sxs-lookup"><span data-stu-id="3b571-128">**LVL_MESSAGE** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="3b571-129">Attribute-ID es uno de los identificadores de atributo TNEF, como **attSubject**.</span><span class="sxs-lookup"><span data-stu-id="3b571-129">Attribute-ID is one of the TNEF attribute identifiers, such as **attSubject**.</span></span> <span data-ttu-id="3b571-130">La longitud del atributo es la longitud en bytes de los datos del atributo.</span><span class="sxs-lookup"><span data-stu-id="3b571-130">Attribute-length is the length in bytes of the attribute data.</span></span> <span data-ttu-id="3b571-131">Los datos de atributo son los datos asociados con el atributo.</span><span class="sxs-lookup"><span data-stu-id="3b571-131">Attribute-data is the data associated with the attribute.</span></span>
  
 <span data-ttu-id="3b571-132">_Attach_Seq:_</span><span class="sxs-lookup"><span data-stu-id="3b571-132">_Attach_Seq:_</span></span>
  
>  <span data-ttu-id="3b571-133">_attRenddata attRenddata Att_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="3b571-133">_attRenddata attRenddata Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="3b571-134">_attRenddata:_</span><span class="sxs-lookup"><span data-stu-id="3b571-134">_attRenddata:_</span></span>
  
> <span data-ttu-id="3b571-135">**LVL_ATTACHMENT suma de comprobación de renddata attRenddata** **sizeof(RENDDATA)**</span><span class="sxs-lookup"><span data-stu-id="3b571-135">**LVL_ATTACHMENT attRenddata** **sizeof(RENDDATA)** renddata checksum</span></span> 
    
<span data-ttu-id="3b571-136">Renddata es los datos asociados a la **estructura RENDDATA** que contiene la información de representación de los datos adjuntos correspondientes.</span><span class="sxs-lookup"><span data-stu-id="3b571-136">Renddata is the data associated with the **RENDDATA** structure that contains the rendering information for the corresponding attachment.</span></span> <span data-ttu-id="3b571-137">La **estructura RENDDATA** se define en el TNEF. Archivo de encabezado H.</span><span class="sxs-lookup"><span data-stu-id="3b571-137">The **RENDDATA** structure is defined in the TNEF.H header file.</span></span> 
  
 <span data-ttu-id="3b571-138">_Att_Attribute_Seq:_</span><span class="sxs-lookup"><span data-stu-id="3b571-138">_Att_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="3b571-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="3b571-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="3b571-140">_Att_Attribute:_</span><span class="sxs-lookup"><span data-stu-id="3b571-140">_Att_Attribute:_</span></span>
  
> <span data-ttu-id="3b571-141">**LVL_ATTACHMENT** suma de comprobación de atributo-ID de atributo-longitud de atributo-datos</span><span class="sxs-lookup"><span data-stu-id="3b571-141">**LVL_ATTACHMENT** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="3b571-142">Los datos de atributo-id, longitud de atributo y atributo tienen los mismos significados que para el Msg_Attribute atributo.</span><span class="sxs-lookup"><span data-stu-id="3b571-142">Attribute-ID, attribute-length, and attribute-data have the same meanings as for the Msg_Attribute item.</span></span>
  

