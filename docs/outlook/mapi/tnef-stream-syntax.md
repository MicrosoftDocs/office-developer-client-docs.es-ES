---
title: Sintaxis de la secuencia TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1353d494-c266-4715-afe7-14543a1bbe1b
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: cbaf37415608dd1d79a06be65b34632f2b4afc89
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820887"
---
# <a name="tnef-stream-syntax"></a><span data-ttu-id="5165d-103">Sintaxis de la secuencia TNEF</span><span class="sxs-lookup"><span data-stu-id="5165d-103">TNEF Stream Syntax</span></span>

  
  
<span data-ttu-id="5165d-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5165d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5165d-105">En este tema se presenta un Nauer Bakus parecido a la descripción de la sintaxis de la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="5165d-105">This topic presents a Bakus-Nauer like description of the TNEF stream syntax.</span></span> <span data-ttu-id="5165d-106">En esta descripción, no terminal elementos que tienen una definición más están en cursiva.</span><span class="sxs-lookup"><span data-stu-id="5165d-106">In this description, nonterminal elements that have a further definition are in italics.</span></span> <span data-ttu-id="5165d-107">Constantes y elementos literales están en negrita.</span><span class="sxs-lookup"><span data-stu-id="5165d-107">Constants and literal items are in bold.</span></span> <span data-ttu-id="5165d-108">Las secuencias de elementos se enumeran en el orden de una sola línea.</span><span class="sxs-lookup"><span data-stu-id="5165d-108">Sequences of elements are listed in order on a single line.</span></span> <span data-ttu-id="5165d-109">Por ejemplo, el elemento de _secuencia_ consta de la constante **TNEF_SIGNATURE**, seguido de una _clave_, seguido de un _objeto_.</span><span class="sxs-lookup"><span data-stu-id="5165d-109">For example, the  _Stream_ item consists of the constant **TNEF_SIGNATURE**, followed by a  _Key_, followed by an  _Object_.</span></span> <span data-ttu-id="5165d-110">Cuando un elemento tiene más de una implementación posible, las alternativas se muestran en líneas consecutivas.</span><span class="sxs-lookup"><span data-stu-id="5165d-110">When an item has more than one possible implementation, the alternatives are listed on consecutive lines.</span></span> <span data-ttu-id="5165d-111">Por ejemplo, un _objeto_ puede constar de un _Message_Seq_, un _Message_Seq_ seguido de un _Attach_Seq_, o simplemente un _Attach_Seq_.</span><span class="sxs-lookup"><span data-stu-id="5165d-111">For example, an  _Object_ can consist of a  _Message_Seq_, a  _Message_Seq_ followed by an  _Attach_Seq_, or just an  _Attach_Seq_.</span></span>
  
 <span data-ttu-id="5165d-112">_TNEF_Stream:_</span><span class="sxs-lookup"><span data-stu-id="5165d-112">_TNEF_Stream:_</span></span>
  
> <span data-ttu-id="5165d-113">**TNEF_SIGNATURE** _Clave_ _Objeto_</span><span class="sxs-lookup"><span data-stu-id="5165d-113">**TNEF_SIGNATURE** _Key_ _Object_</span></span>
    
 <span data-ttu-id="5165d-114">_Clave:_</span><span class="sxs-lookup"><span data-stu-id="5165d-114">_Key:_</span></span>
  
> <span data-ttu-id="5165d-115">un entero sin signo de 16 bits distinto de cero</span><span class="sxs-lookup"><span data-stu-id="5165d-115">a nonzero 16-bit unsigned integer</span></span>
    
<span data-ttu-id="5165d-116">Los transportes TNEF habilitado para generan este valor antes de usar la implementación de TNEF para generar una secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="5165d-116">TNEF enabled transports generate this value before using the TNEF implementation to generate a TNEF stream.</span></span>
  
 <span data-ttu-id="5165d-117">_Objeto:_</span><span class="sxs-lookup"><span data-stu-id="5165d-117">_Object:_</span></span>
  
>  <span data-ttu-id="5165d-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span><span class="sxs-lookup"><span data-stu-id="5165d-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span></span>
    
 <span data-ttu-id="5165d-119">_Message_Seq:_</span><span class="sxs-lookup"><span data-stu-id="5165d-119">_Message_Seq:_</span></span>
  
>  <span data-ttu-id="5165d-120">_attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="5165d-120">_attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="5165d-121">_attTnefVersion:_</span><span class="sxs-lookup"><span data-stu-id="5165d-121">_attTnefVersion:_</span></span>
  
> <span data-ttu-id="5165d-122">**Sizeof (ulong) attTnefVersion LVL_MESSAGE** **0 x 00010000** suma de comprobación</span><span class="sxs-lookup"><span data-stu-id="5165d-122">**LVL_MESSAGE attTnefVersion sizeof(ULONG)** **0x00010000** checksum</span></span> 
    
 <span data-ttu-id="5165d-123">_attMessageClass:_</span><span class="sxs-lookup"><span data-stu-id="5165d-123">_attMessageClass:_</span></span>
  
> <span data-ttu-id="5165d-124">**LVL_MESSAGE attMessageClass** suma de comprobación de _msg_class_length msg_class_</span><span class="sxs-lookup"><span data-stu-id="5165d-124">**LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ checksum</span></span> 
    
 <span data-ttu-id="5165d-125">_Msg_Attribute_Seq:_</span><span class="sxs-lookup"><span data-stu-id="5165d-125">_Msg_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="5165d-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="5165d-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="5165d-127">_Msg_Attribute:_</span><span class="sxs-lookup"><span data-stu-id="5165d-127">_Msg_Attribute:_</span></span>
  
> <span data-ttu-id="5165d-128">Suma de comprobación de datos de atributos de longitud de atributo **LVL_MESSAGE** identificador de atributo</span><span class="sxs-lookup"><span data-stu-id="5165d-128">**LVL_MESSAGE** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="5165d-129">Identificador de atributo es uno de los identificadores de atributo TNEF, como **attSubject**.</span><span class="sxs-lookup"><span data-stu-id="5165d-129">Attribute-ID is one of the TNEF attribute identifiers, such as **attSubject**.</span></span> <span data-ttu-id="5165d-130">Atributo-length es la longitud en bytes de los datos del atributo.</span><span class="sxs-lookup"><span data-stu-id="5165d-130">Attribute-length is the length in bytes of the attribute data.</span></span> <span data-ttu-id="5165d-131">Datos de atributos son los datos asociados con el atributo.</span><span class="sxs-lookup"><span data-stu-id="5165d-131">Attribute-data is the data associated with the attribute.</span></span>
  
 <span data-ttu-id="5165d-132">_Attach_Seq:_</span><span class="sxs-lookup"><span data-stu-id="5165d-132">_Attach_Seq:_</span></span>
  
>  <span data-ttu-id="5165d-133">_attRenddata attRenddata Att_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="5165d-133">_attRenddata attRenddata Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="5165d-134">_attRenddata:_</span><span class="sxs-lookup"><span data-stu-id="5165d-134">_attRenddata:_</span></span>
  
> <span data-ttu-id="5165d-135">**LVL_ATTACHMENT attRenddata** suma de comprobación de **sizeof(RENDDATA)** renddata</span><span class="sxs-lookup"><span data-stu-id="5165d-135">**LVL_ATTACHMENT attRenddata** **sizeof(RENDDATA)** renddata checksum</span></span> 
    
<span data-ttu-id="5165d-136">Renddata es los datos asociados con la estructura **RENDDATA** que contiene la información de representación de los datos adjuntos correspondiente.</span><span class="sxs-lookup"><span data-stu-id="5165d-136">Renddata is the data associated with the **RENDDATA** structure that contains the rendering information for the corresponding attachment.</span></span> <span data-ttu-id="5165d-137">La estructura **RENDDATA** se define en el TNEF. Archivo de encabezado H.</span><span class="sxs-lookup"><span data-stu-id="5165d-137">The **RENDDATA** structure is defined in the TNEF.H header file.</span></span> 
  
 <span data-ttu-id="5165d-138">_Att_Attribute_Seq:_</span><span class="sxs-lookup"><span data-stu-id="5165d-138">_Att_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="5165d-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="5165d-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="5165d-140">_Att_Attribute:_</span><span class="sxs-lookup"><span data-stu-id="5165d-140">_Att_Attribute:_</span></span>
  
> <span data-ttu-id="5165d-141">Suma de comprobación de datos de atributos de longitud de atributo **LVL_ATTACHMENT** identificador de atributo</span><span class="sxs-lookup"><span data-stu-id="5165d-141">**LVL_ATTACHMENT** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="5165d-142">Identificador de atributo, la longitud de atributo y datos de atributos tienen el mismo significado que para el elemento Msg_Attribute.</span><span class="sxs-lookup"><span data-stu-id="5165d-142">Attribute-ID, attribute-length, and attribute-data have the same meanings as for the Msg_Attribute item.</span></span>
  

