---
title: ComplexType HeaderFooterFont_Type (XML de Visio)
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
# <a name="headerfooterfonttype-complextype-visio-xml"></a><span data-ttu-id="3b120-102">ComplexType HeaderFooterFont_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="3b120-102">HeaderFooterFont_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="3b120-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="3b120-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3b120-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3b120-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3b120-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="3b120-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3b120-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="3b120-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3b120-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="3b120-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3b120-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="3b120-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3b120-109">Definición</span><span class="sxs-lookup"><span data-stu-id="3b120-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="3b120-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="3b120-110">Elements and attributes</span></span>

<span data-ttu-id="3b120-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="3b120-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3b120-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3b120-112">Child elements</span></span>

<span data-ttu-id="3b120-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3b120-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3b120-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="3b120-114">Attributes</span></span>

|<span data-ttu-id="3b120-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="3b120-115">**Attribute**</span></span>|<span data-ttu-id="3b120-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3b120-116">**Type**</span></span>|<span data-ttu-id="3b120-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="3b120-117">**Required**</span></span>|<span data-ttu-id="3b120-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3b120-118">**Description**</span></span>|<span data-ttu-id="3b120-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="3b120-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3b120-120">CharSet</span><span class="sxs-lookup"><span data-stu-id="3b120-120">CharSet</span></span>  <br/> |<span data-ttu-id="3b120-121">xsd: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="3b120-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="3b120-122">opcional</span><span class="sxs-lookup"><span data-stu-id="3b120-122">optional</span></span>  <br/> ||<span data-ttu-id="3b120-123">Valores del tipo xsd: unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="3b120-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="3b120-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="3b120-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="3b120-125">xsd: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="3b120-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="3b120-126">opcional</span><span class="sxs-lookup"><span data-stu-id="3b120-126">optional</span></span>  <br/> ||<span data-ttu-id="3b120-127">Valores del tipo xsd: unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="3b120-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="3b120-128">Escape</span><span class="sxs-lookup"><span data-stu-id="3b120-128">Escapement</span></span>  <br/> |<span data-ttu-id="3b120-129">xsd: int</span><span class="sxs-lookup"><span data-stu-id="3b120-129">xsd:int</span></span>  <br/> |<span data-ttu-id="3b120-130">opcional</span><span class="sxs-lookup"><span data-stu-id="3b120-130">optional</span></span>  <br/> ||<span data-ttu-id="3b120-131">Valores del tipo xsd: int.</span><span class="sxs-lookup"><span data-stu-id="3b120-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="3b120-132">FaceName</span><span class="sxs-lookup"><span data-stu-id="3b120-132">FaceName</span></span>  <br/> |<span data-ttu-id="3b120-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="3b120-133">xsd:string</span></span>  <br/> |<span data-ttu-id="3b120-134">opcional</span><span class="sxs-lookup"><span data-stu-id="3b120-134">optional</span></span>  <br/> ||<span data-ttu-id="3b120-135">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="3b120-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3b120-136">Height</span><span class="sxs-lookup"><span data-stu-id="3b120-136">Height</span></span>  <br/> |<span data-ttu-id="3b120-137">xsd: int</span><span class="sxs-lookup"><span data-stu-id="3b120-137">xsd:int</span></span>  <br/> |<span data-ttu-id="3b120-138">opcional</span><span class="sxs-lookup"><span data-stu-id="3b120-138">optional</span></span>  <br/> ||<span data-ttu-id="3b120-139">Valores del tipo xsd: int.</span><span class="sxs-lookup"><span data-stu-id="3b120-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="3b120-140">Italic</span><span class="sxs-lookup"><span data-stu-id="3b120-140">Italic</span></span>  <br/> |<span data-ttu-id="3b120-141">xsd: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="3b120-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="3b120-142">opcional</span><span class="sxs-lookup"><span data-stu-id="3b120-142">optional</span></span>  <br/> ||<span data-ttu-id="3b120-143">Valores del tipo xsd: unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="3b120-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="3b120-144">Orientation</span><span class="sxs-lookup"><span data-stu-id="3b120-144">Orientation</span></span>  <br/> |<span data-ttu-id="3b120-145">xsd: int</span><span class="sxs-lookup"><span data-stu-id="3b120-145">xsd:int</span></span>  <br/> |<span data-ttu-id="3b120-146">opcional</span><span class="sxs-lookup"><span data-stu-id="3b120-146">optional</span></span>  <br/> ||<span data-ttu-id="3b120-147">Valores del tipo xsd: int.</span><span class="sxs-lookup"><span data-stu-id="3b120-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="3b120-148">Deprecision</span><span class="sxs-lookup"><span data-stu-id="3b120-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="3b120-149">xsd: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="3b120-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="3b120-150">opcional</span><span class="sxs-lookup"><span data-stu-id="3b120-150">optional</span></span>  <br/> ||<span data-ttu-id="3b120-151">Valores del tipo xsd: unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="3b120-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="3b120-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="3b120-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="3b120-153">xsd: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="3b120-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="3b120-154">opcional</span><span class="sxs-lookup"><span data-stu-id="3b120-154">optional</span></span>  <br/> ||<span data-ttu-id="3b120-155">Valores del tipo xsd: unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="3b120-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="3b120-156">Quality</span><span class="sxs-lookup"><span data-stu-id="3b120-156">Quality</span></span>  <br/> |<span data-ttu-id="3b120-157">xsd: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="3b120-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="3b120-158">opcional</span><span class="sxs-lookup"><span data-stu-id="3b120-158">optional</span></span>  <br/> ||<span data-ttu-id="3b120-159">Valores del tipo xsd: unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="3b120-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="3b120-160">Tacha</span><span class="sxs-lookup"><span data-stu-id="3b120-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="3b120-161">xsd: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="3b120-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="3b120-162">opcional</span><span class="sxs-lookup"><span data-stu-id="3b120-162">optional</span></span>  <br/> ||<span data-ttu-id="3b120-163">Valores del tipo xsd: unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="3b120-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="3b120-164">Underline</span><span class="sxs-lookup"><span data-stu-id="3b120-164">Underline</span></span>  <br/> |<span data-ttu-id="3b120-165">xsd: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="3b120-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="3b120-166">opcional</span><span class="sxs-lookup"><span data-stu-id="3b120-166">optional</span></span>  <br/> ||<span data-ttu-id="3b120-167">Valores del tipo xsd: unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="3b120-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="3b120-168">Peso</span><span class="sxs-lookup"><span data-stu-id="3b120-168">Weight</span></span>  <br/> |<span data-ttu-id="3b120-169">xsd: int</span><span class="sxs-lookup"><span data-stu-id="3b120-169">xsd:int</span></span>  <br/> |<span data-ttu-id="3b120-170">opcional</span><span class="sxs-lookup"><span data-stu-id="3b120-170">optional</span></span>  <br/> ||<span data-ttu-id="3b120-171">Valores del tipo xsd: int.</span><span class="sxs-lookup"><span data-stu-id="3b120-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="3b120-172">Width</span><span class="sxs-lookup"><span data-stu-id="3b120-172">Width</span></span>  <br/> |<span data-ttu-id="3b120-173">xsd: int</span><span class="sxs-lookup"><span data-stu-id="3b120-173">xsd:int</span></span>  <br/> |<span data-ttu-id="3b120-174">opcional</span><span class="sxs-lookup"><span data-stu-id="3b120-174">optional</span></span>  <br/> ||<span data-ttu-id="3b120-175">Valores del tipo xsd: int.</span><span class="sxs-lookup"><span data-stu-id="3b120-175">Values of the xsd:int type.</span></span>  <br/> |
   

