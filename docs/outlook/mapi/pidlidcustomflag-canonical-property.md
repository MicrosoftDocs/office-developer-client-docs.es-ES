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
ms.openlocfilehash: cba4989ec3b1afcadb0caddd4af444cc9c96ebda
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565959"
---
# <a name="pidlidcustomflag-canonical-property"></a><span data-ttu-id="2bdfc-103">Propiedad canónica PidLidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="2bdfc-103">PidLidCustomFlag Canonical Property</span></span>

  
  
<span data-ttu-id="2bdfc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2bdfc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2bdfc-105">Una máscara de bits que especifica cómo se personaliza un mensaje, por ejemplo, guarda con propiedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="2bdfc-105">A bitmask that specifies how a message is customized, for example, saved with custom properties.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="2bdfc-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2bdfc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2bdfc-107">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="2bdfc-107">dispidCustomFlag</span></span>  <br/> |
|<span data-ttu-id="2bdfc-108">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="2bdfc-108">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2bdfc-109">0x00008251</span><span class="sxs-lookup"><span data-stu-id="2bdfc-109">0x00008251</span></span>  <br/> |
|<span data-ttu-id="2bdfc-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2bdfc-110">Data type:</span></span>  <br/> |<span data-ttu-id="2bdfc-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2bdfc-111">PT_LONG</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2bdfc-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2bdfc-112">Remarks</span></span>

<span data-ttu-id="2bdfc-113">Para recuperar el valor de esta propiedad, en primer lugar utilice **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** para obtener la etiqueta de propiedad y, a continuación, especifique esta etiqueta de propiedad en **[IMAPIProp::GetProps](imapiprop-getprops.md)** para obtener el valor.</span><span class="sxs-lookup"><span data-stu-id="2bdfc-113">To retrieve the value of this property, first use **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** to obtain the property tag, and then specify this property tag in **[IMAPIProp::GetProps](imapiprop-getprops.md)** to get the value.</span></span> 
  
<span data-ttu-id="2bdfc-114">Indicadores de posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="2bdfc-114">Possible Flags are as follows:</span></span>
  
****

|<span data-ttu-id="2bdfc-115">**Constante**</span><span class="sxs-lookup"><span data-stu-id="2bdfc-115">**Constant**</span></span>|<span data-ttu-id="2bdfc-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="2bdfc-116">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2bdfc-117">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="2bdfc-117">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="2bdfc-118">0x0D000000</span><span class="sxs-lookup"><span data-stu-id="2bdfc-118">0x0D000000</span></span>  <br/> |
|<span data-ttu-id="2bdfc-119">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="2bdfc-119">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="2bdfc-120">0x02000000</span><span class="sxs-lookup"><span data-stu-id="2bdfc-120">0x02000000</span></span>  <br/> |
   
<span data-ttu-id="2bdfc-121">Cuando se llama a **IMAPIProp::GetIDsFromNames**, especifique los siguientes valores de la estructura **[MAPINAMEID](mapinameid.md)** indicada por el parámetro de entrada *lppPropNames* .</span><span class="sxs-lookup"><span data-stu-id="2bdfc-121">When calling **IMAPIProp::GetIDsFromNames**, specify the following values for the **[MAPINAMEID](mapinameid.md)** structure pointed to by the input parameter  *lppPropNames*  .</span></span> 
  
****

|<span data-ttu-id="2bdfc-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2bdfc-122">**Member**</span></span>|<span data-ttu-id="2bdfc-123">**Valor**</span><span class="sxs-lookup"><span data-stu-id="2bdfc-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2bdfc-124">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="2bdfc-124">lpGuid:</span></span>  <br/> |<span data-ttu-id="2bdfc-125">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="2bdfc-125">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="2bdfc-126">ulKind:</span><span class="sxs-lookup"><span data-stu-id="2bdfc-126">ulKind:</span></span>  <br/> |<span data-ttu-id="2bdfc-127">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="2bdfc-127">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="2bdfc-128">Kind.lID:</span><span class="sxs-lookup"><span data-stu-id="2bdfc-128">Kind.lID:</span></span>  <br/> |<span data-ttu-id="2bdfc-129">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="2bdfc-129">dispidCustomFlag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="2bdfc-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2bdfc-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2bdfc-131">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="2bdfc-131">Protocol specifications</span></span>

<span data-ttu-id="2bdfc-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2bdfc-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2bdfc-133">Proporciona definiciones de conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="2bdfc-133">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2bdfc-134">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2bdfc-134">Header files</span></span>

<span data-ttu-id="2bdfc-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2bdfc-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="2bdfc-136">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2bdfc-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="2bdfc-137">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2bdfc-137">Mapitags.h</span></span>
  
> <span data-ttu-id="2bdfc-138">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="2bdfc-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2bdfc-139">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="2bdfc-139">See also</span></span>



[<span data-ttu-id="2bdfc-140">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2bdfc-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2bdfc-141">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="2bdfc-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2bdfc-142">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2bdfc-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2bdfc-143">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="2bdfc-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

