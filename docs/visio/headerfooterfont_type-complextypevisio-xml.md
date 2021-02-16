---
title: HeaderFooterFont_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: dd99d87e0d80aad3bcde31e4834337ee59088da2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541074"
---
# <a name="headerfooterfont_type-complextype-visio-xml"></a><span data-ttu-id="a7d27-102">HeaderFooterFont_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a7d27-102">HeaderFooterFont_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="a7d27-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="a7d27-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a7d27-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a7d27-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a7d27-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a7d27-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a7d27-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a7d27-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a7d27-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="a7d27-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a7d27-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="a7d27-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a7d27-109">Definición</span><span class="sxs-lookup"><span data-stu-id="a7d27-109">Definition</span></span>

```XML
      <xs:complexType name="HeaderFooterFont_Type">
    <xs:attribute name="Height"
  type="xsd:int"
    />
    <xs:attribute name="Width"
  type="xsd:int"
    />
    <xs:attribute name="Escapement"
  type="xsd:int"
    />
    <xs:attribute name="Orientation"
  type="xsd:int"
    />
    <xs:attribute name="Weight"
  type="xsd:int"
    />
    <xs:attribute name="Italic"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="Underline"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="StrikeOut"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="CharSet"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="OutPrecision"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="ClipPrecision"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="Quality"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="PitchAndFamily"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="FaceName"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a7d27-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="a7d27-110">Elements and attributes</span></span>

<span data-ttu-id="a7d27-111">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="a7d27-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a7d27-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a7d27-112">Child elements</span></span>

<span data-ttu-id="a7d27-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a7d27-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a7d27-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="a7d27-114">Attributes</span></span>

|<span data-ttu-id="a7d27-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="a7d27-115">**Attribute**</span></span>|<span data-ttu-id="a7d27-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a7d27-116">**Type**</span></span>|<span data-ttu-id="a7d27-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="a7d27-117">**Required**</span></span>|<span data-ttu-id="a7d27-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a7d27-118">**Description**</span></span>|<span data-ttu-id="a7d27-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="a7d27-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a7d27-120">CharSet</span><span class="sxs-lookup"><span data-stu-id="a7d27-120">CharSet</span></span>  <br/> |<span data-ttu-id="a7d27-121">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="a7d27-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="a7d27-122">opcional</span><span class="sxs-lookup"><span data-stu-id="a7d27-122">optional</span></span>  <br/> ||<span data-ttu-id="a7d27-123">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="a7d27-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="a7d27-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="a7d27-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="a7d27-125">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="a7d27-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="a7d27-126">opcional</span><span class="sxs-lookup"><span data-stu-id="a7d27-126">optional</span></span>  <br/> ||<span data-ttu-id="a7d27-127">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="a7d27-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="a7d27-128">Escapement</span><span class="sxs-lookup"><span data-stu-id="a7d27-128">Escapement</span></span>  <br/> |<span data-ttu-id="a7d27-129">xsd:int</span><span class="sxs-lookup"><span data-stu-id="a7d27-129">xsd:int</span></span>  <br/> |<span data-ttu-id="a7d27-130">opcional</span><span class="sxs-lookup"><span data-stu-id="a7d27-130">optional</span></span>  <br/> ||<span data-ttu-id="a7d27-131">Valores del tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="a7d27-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="a7d27-132">FaceName</span><span class="sxs-lookup"><span data-stu-id="a7d27-132">FaceName</span></span>  <br/> |<span data-ttu-id="a7d27-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a7d27-133">xsd:string</span></span>  <br/> |<span data-ttu-id="a7d27-134">opcional</span><span class="sxs-lookup"><span data-stu-id="a7d27-134">optional</span></span>  <br/> ||<span data-ttu-id="a7d27-135">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a7d27-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a7d27-136">Height</span><span class="sxs-lookup"><span data-stu-id="a7d27-136">Height</span></span>  <br/> |<span data-ttu-id="a7d27-137">xsd:int</span><span class="sxs-lookup"><span data-stu-id="a7d27-137">xsd:int</span></span>  <br/> |<span data-ttu-id="a7d27-138">opcional</span><span class="sxs-lookup"><span data-stu-id="a7d27-138">optional</span></span>  <br/> ||<span data-ttu-id="a7d27-139">Valores del tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="a7d27-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="a7d27-140">Italic</span><span class="sxs-lookup"><span data-stu-id="a7d27-140">Italic</span></span>  <br/> |<span data-ttu-id="a7d27-141">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="a7d27-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="a7d27-142">opcional</span><span class="sxs-lookup"><span data-stu-id="a7d27-142">optional</span></span>  <br/> ||<span data-ttu-id="a7d27-143">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="a7d27-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="a7d27-144">Orientation</span><span class="sxs-lookup"><span data-stu-id="a7d27-144">Orientation</span></span>  <br/> |<span data-ttu-id="a7d27-145">xsd:int</span><span class="sxs-lookup"><span data-stu-id="a7d27-145">xsd:int</span></span>  <br/> |<span data-ttu-id="a7d27-146">opcional</span><span class="sxs-lookup"><span data-stu-id="a7d27-146">optional</span></span>  <br/> ||<span data-ttu-id="a7d27-147">Valores del tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="a7d27-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="a7d27-148">OutPrecision</span><span class="sxs-lookup"><span data-stu-id="a7d27-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="a7d27-149">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="a7d27-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="a7d27-150">opcional</span><span class="sxs-lookup"><span data-stu-id="a7d27-150">optional</span></span>  <br/> ||<span data-ttu-id="a7d27-151">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="a7d27-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="a7d27-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="a7d27-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="a7d27-153">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="a7d27-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="a7d27-154">opcional</span><span class="sxs-lookup"><span data-stu-id="a7d27-154">optional</span></span>  <br/> ||<span data-ttu-id="a7d27-155">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="a7d27-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="a7d27-156">Calidad</span><span class="sxs-lookup"><span data-stu-id="a7d27-156">Quality</span></span>  <br/> |<span data-ttu-id="a7d27-157">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="a7d27-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="a7d27-158">opcional</span><span class="sxs-lookup"><span data-stu-id="a7d27-158">optional</span></span>  <br/> ||<span data-ttu-id="a7d27-159">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="a7d27-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="a7d27-160">StrikeOut</span><span class="sxs-lookup"><span data-stu-id="a7d27-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="a7d27-161">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="a7d27-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="a7d27-162">opcional</span><span class="sxs-lookup"><span data-stu-id="a7d27-162">optional</span></span>  <br/> ||<span data-ttu-id="a7d27-163">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="a7d27-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="a7d27-164">Subrayado</span><span class="sxs-lookup"><span data-stu-id="a7d27-164">Underline</span></span>  <br/> |<span data-ttu-id="a7d27-165">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="a7d27-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="a7d27-166">opcional</span><span class="sxs-lookup"><span data-stu-id="a7d27-166">optional</span></span>  <br/> ||<span data-ttu-id="a7d27-167">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="a7d27-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="a7d27-168">Peso</span><span class="sxs-lookup"><span data-stu-id="a7d27-168">Weight</span></span>  <br/> |<span data-ttu-id="a7d27-169">xsd:int</span><span class="sxs-lookup"><span data-stu-id="a7d27-169">xsd:int</span></span>  <br/> |<span data-ttu-id="a7d27-170">opcional</span><span class="sxs-lookup"><span data-stu-id="a7d27-170">optional</span></span>  <br/> ||<span data-ttu-id="a7d27-171">Valores del tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="a7d27-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="a7d27-172">Width</span><span class="sxs-lookup"><span data-stu-id="a7d27-172">Width</span></span>  <br/> |<span data-ttu-id="a7d27-173">xsd:int</span><span class="sxs-lookup"><span data-stu-id="a7d27-173">xsd:int</span></span>  <br/> |<span data-ttu-id="a7d27-174">opcional</span><span class="sxs-lookup"><span data-stu-id="a7d27-174">optional</span></span>  <br/> ||<span data-ttu-id="a7d27-175">Valores del tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="a7d27-175">Values of the xsd:int type.</span></span>  <br/> |
   

