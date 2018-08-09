---
title: Propiedad canónica PidLidCustomFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCustomFlag
api_type:
- COM
ms.assetid: bfb7fd1e-774f-9a2f-fbbe-ba7f68ed8663
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5d97f56946512266bb7a08aa6b4a4ff78dded56a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818622"
---
# <a name="pidlidcustomflag-canonical-property"></a><span data-ttu-id="6e616-103">Propiedad canónica PidLidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="6e616-103">PidLidCustomFlag Canonical Property</span></span>

  
  
<span data-ttu-id="6e616-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6e616-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6e616-105">Una máscara de bits que especifica cómo se personaliza un mensaje, por ejemplo, guarda con propiedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="6e616-105">A bitmask that specifies how a message is customized, for example, saved with custom properties.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="6e616-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="6e616-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6e616-107">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="6e616-107">dispidCustomFlag</span></span>  <br/> |
|<span data-ttu-id="6e616-108">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="6e616-108">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6e616-109">0x00008251</span><span class="sxs-lookup"><span data-stu-id="6e616-109">0x00008251</span></span>  <br/> |
|<span data-ttu-id="6e616-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="6e616-110">Data type:</span></span>  <br/> |<span data-ttu-id="6e616-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6e616-111">PT_LONG</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e616-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6e616-112">Remarks</span></span>

<span data-ttu-id="6e616-113">Para recuperar el valor de esta propiedad, en primer lugar utilice **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** para obtener la etiqueta de propiedad y, a continuación, especifique esta etiqueta de propiedad en **[IMAPIProp::GetProps](imapiprop-getprops.md)** para obtener el valor.</span><span class="sxs-lookup"><span data-stu-id="6e616-113">To retrieve the value of this property, first use **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** to obtain the property tag, and then specify this property tag in **[IMAPIProp::GetProps](imapiprop-getprops.md)** to get the value.</span></span> 
  
<span data-ttu-id="6e616-114">Indicadores de posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="6e616-114">Possible Flags are as follows:</span></span>
  
****

|<span data-ttu-id="6e616-115">**Constante**</span><span class="sxs-lookup"><span data-stu-id="6e616-115">**Constant**</span></span>|<span data-ttu-id="6e616-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6e616-116">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6e616-117">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="6e616-117">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="6e616-118">0x0D000000</span><span class="sxs-lookup"><span data-stu-id="6e616-118">0x0D000000</span></span>  <br/> |
|<span data-ttu-id="6e616-119">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="6e616-119">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="6e616-120">0x02000000</span><span class="sxs-lookup"><span data-stu-id="6e616-120">0x02000000</span></span>  <br/> |
   
<span data-ttu-id="6e616-121">Cuando se llama a **IMAPIProp::GetIDsFromNames**, especifique los siguientes valores de la estructura **[MAPINAMEID](mapinameid.md)** indicada por el parámetro de entrada *lppPropNames* .</span><span class="sxs-lookup"><span data-stu-id="6e616-121">When calling **IMAPIProp::GetIDsFromNames**, specify the following values for the **[MAPINAMEID](mapinameid.md)** structure pointed to by the input parameter  *lppPropNames*  .</span></span> 
  
****

|<span data-ttu-id="6e616-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6e616-122">**Member**</span></span>|<span data-ttu-id="6e616-123">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6e616-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6e616-124">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="6e616-124">lpGuid:</span></span>  <br/> |<span data-ttu-id="6e616-125">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="6e616-125">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="6e616-126">ulKind:</span><span class="sxs-lookup"><span data-stu-id="6e616-126">ulKind:</span></span>  <br/> |<span data-ttu-id="6e616-127">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="6e616-127">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="6e616-128">Kind.lID:</span><span class="sxs-lookup"><span data-stu-id="6e616-128">Kind.lID:</span></span>  <br/> |<span data-ttu-id="6e616-129">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="6e616-129">dispidCustomFlag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="6e616-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6e616-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6e616-131">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="6e616-131">Protocol specifications</span></span>

<span data-ttu-id="6e616-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e616-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e616-133">Proporciona definiciones de conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="6e616-133">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6e616-134">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="6e616-134">Header files</span></span>

<span data-ttu-id="6e616-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6e616-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="6e616-136">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="6e616-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="6e616-137">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6e616-137">Mapitags.h</span></span>
  
> <span data-ttu-id="6e616-138">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="6e616-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6e616-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e616-139">See also</span></span>



[<span data-ttu-id="6e616-140">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6e616-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6e616-141">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="6e616-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6e616-142">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="6e616-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6e616-143">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="6e616-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

