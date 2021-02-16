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
ms.openlocfilehash: 9a131c633b8dcf9b0e5070f01de8fcab90a18ade
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357620"
---
# <a name="pidlidcustomflag-canonical-property"></a><span data-ttu-id="75dea-103">Propiedad canónica PidLidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="75dea-103">PidLidCustomFlag Canonical Property</span></span>

  
  
<span data-ttu-id="75dea-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75dea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75dea-105">Máscara de bits que especifica cómo se personaliza un mensaje, por ejemplo, se guarda con propiedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="75dea-105">A bitmask that specifies how a message is customized, for example, saved with custom properties.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="75dea-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="75dea-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="75dea-107">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="75dea-107">dispidCustomFlag</span></span>  <br/> |
|<span data-ttu-id="75dea-108">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="75dea-108">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="75dea-109">0x00008251</span><span class="sxs-lookup"><span data-stu-id="75dea-109">0x00008251</span></span>  <br/> |
|<span data-ttu-id="75dea-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="75dea-110">Data type:</span></span>  <br/> |<span data-ttu-id="75dea-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="75dea-111">PT_LONG</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75dea-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="75dea-112">Remarks</span></span>

<span data-ttu-id="75dea-113">Para recuperar el valor de esta propiedad, use primero **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** para obtener la etiqueta de propiedad y, a continuación, especifique esta etiqueta de propiedad en **[IMAPIProp::GetProps](imapiprop-getprops.md)** para obtener el valor.</span><span class="sxs-lookup"><span data-stu-id="75dea-113">To retrieve the value of this property, first use **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** to obtain the property tag, and then specify this property tag in **[IMAPIProp::GetProps](imapiprop-getprops.md)** to get the value.</span></span> 
  
<span data-ttu-id="75dea-114">Las marcas posibles son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="75dea-114">Possible Flags are as follows:</span></span>
  
****

|<span data-ttu-id="75dea-115">**Constante**</span><span class="sxs-lookup"><span data-stu-id="75dea-115">**Constant**</span></span>|<span data-ttu-id="75dea-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="75dea-116">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="75dea-117">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="75dea-117">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="75dea-118">0x0D000000</span><span class="sxs-lookup"><span data-stu-id="75dea-118">0x0D000000</span></span>  <br/> |
|<span data-ttu-id="75dea-119">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="75dea-119">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="75dea-120">0x02000000</span><span class="sxs-lookup"><span data-stu-id="75dea-120">0x02000000</span></span>  <br/> |
   
<span data-ttu-id="75dea-121">Al llamar **a IMAPIProp::GetIDsFromNames**, especifique los siguientes valores para la estructura **[MAPINAMEID](mapinameid.md)** a la que apunta el parámetro de entrada  *lppPropNames*  .</span><span class="sxs-lookup"><span data-stu-id="75dea-121">When calling **IMAPIProp::GetIDsFromNames**, specify the following values for the **[MAPINAMEID](mapinameid.md)** structure pointed to by the input parameter  *lppPropNames*  .</span></span> 
  
****

|<span data-ttu-id="75dea-122">**Miembro**</span><span class="sxs-lookup"><span data-stu-id="75dea-122">**Member**</span></span>|<span data-ttu-id="75dea-123">**Valor**</span><span class="sxs-lookup"><span data-stu-id="75dea-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="75dea-124">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="75dea-124">lpGuid:</span></span>  <br/> |<span data-ttu-id="75dea-125">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="75dea-125">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="75dea-126">ulKind:</span><span class="sxs-lookup"><span data-stu-id="75dea-126">ulKind:</span></span>  <br/> |<span data-ttu-id="75dea-127">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="75dea-127">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="75dea-128">Kind.lID:</span><span class="sxs-lookup"><span data-stu-id="75dea-128">Kind.lID:</span></span>  <br/> |<span data-ttu-id="75dea-129">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="75dea-129">dispidCustomFlag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="75dea-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="75dea-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="75dea-131">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="75dea-131">Protocol specifications</span></span>

<span data-ttu-id="75dea-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75dea-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75dea-133">Proporciona definiciones de conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="75dea-133">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="75dea-134">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="75dea-134">Header files</span></span>

<span data-ttu-id="75dea-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="75dea-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="75dea-136">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="75dea-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="75dea-137">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="75dea-137">Mapitags.h</span></span>
  
> <span data-ttu-id="75dea-138">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="75dea-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="75dea-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="75dea-139">See also</span></span>



[<span data-ttu-id="75dea-140">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="75dea-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="75dea-141">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="75dea-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="75dea-142">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="75dea-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="75dea-143">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="75dea-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

