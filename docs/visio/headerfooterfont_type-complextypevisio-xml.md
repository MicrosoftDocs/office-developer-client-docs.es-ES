---
title: HeaderFooterFont_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: cc51924aa68e3248583be5f717b5813d4a32af2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335626"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a><span data-ttu-id="72f2d-102">HeaderFooterFont_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="72f2d-102">HeaderFooterFont_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="72f2d-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="72f2d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="72f2d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="72f2d-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="72f2d-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="72f2d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="72f2d-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="72f2d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="72f2d-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="72f2d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="72f2d-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="72f2d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="72f2d-109">Definición</span><span class="sxs-lookup"><span data-stu-id="72f2d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="72f2d-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="72f2d-110">Elements and attributes</span></span>

<span data-ttu-id="72f2d-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="72f2d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="72f2d-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="72f2d-112">Child elements</span></span>

<span data-ttu-id="72f2d-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="72f2d-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="72f2d-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="72f2d-114">Attributes</span></span>

|<span data-ttu-id="72f2d-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="72f2d-115">**Attribute**</span></span>|<span data-ttu-id="72f2d-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="72f2d-116">**Type**</span></span>|<span data-ttu-id="72f2d-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="72f2d-117">**Required**</span></span>|<span data-ttu-id="72f2d-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="72f2d-118">**Description**</span></span>|<span data-ttu-id="72f2d-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="72f2d-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="72f2d-120">CharSet</span><span class="sxs-lookup"><span data-stu-id="72f2d-120">CharSet</span></span>  <br/> |<span data-ttu-id="72f2d-121">xsd: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="72f2d-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="72f2d-122">opcional</span><span class="sxs-lookup"><span data-stu-id="72f2d-122">optional</span></span>  <br/> ||<span data-ttu-id="72f2d-123">Valores del tipo xsd: unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="72f2d-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="72f2d-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="72f2d-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="72f2d-125">xsd: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="72f2d-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="72f2d-126">opcional</span><span class="sxs-lookup"><span data-stu-id="72f2d-126">optional</span></span>  <br/> ||<span data-ttu-id="72f2d-127">Valores del tipo xsd: unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="72f2d-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="72f2d-128">Escape</span><span class="sxs-lookup"><span data-stu-id="72f2d-128">Escapement</span></span>  <br/> |<span data-ttu-id="72f2d-129">xsd: int</span><span class="sxs-lookup"><span data-stu-id="72f2d-129">xsd:int</span></span>  <br/> |<span data-ttu-id="72f2d-130">opcional</span><span class="sxs-lookup"><span data-stu-id="72f2d-130">optional</span></span>  <br/> ||<span data-ttu-id="72f2d-131">Valores del tipo xsd: int.</span><span class="sxs-lookup"><span data-stu-id="72f2d-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="72f2d-132">FaceName</span><span class="sxs-lookup"><span data-stu-id="72f2d-132">FaceName</span></span>  <br/> |<span data-ttu-id="72f2d-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="72f2d-133">xsd:string</span></span>  <br/> |<span data-ttu-id="72f2d-134">opcional</span><span class="sxs-lookup"><span data-stu-id="72f2d-134">optional</span></span>  <br/> ||<span data-ttu-id="72f2d-135">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="72f2d-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="72f2d-136">Height</span><span class="sxs-lookup"><span data-stu-id="72f2d-136">Height</span></span>  <br/> |<span data-ttu-id="72f2d-137">xsd: int</span><span class="sxs-lookup"><span data-stu-id="72f2d-137">xsd:int</span></span>  <br/> |<span data-ttu-id="72f2d-138">opcional</span><span class="sxs-lookup"><span data-stu-id="72f2d-138">optional</span></span>  <br/> ||<span data-ttu-id="72f2d-139">Valores del tipo xsd: int.</span><span class="sxs-lookup"><span data-stu-id="72f2d-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="72f2d-140">Italic</span><span class="sxs-lookup"><span data-stu-id="72f2d-140">Italic</span></span>  <br/> |<span data-ttu-id="72f2d-141">xsd: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="72f2d-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="72f2d-142">opcional</span><span class="sxs-lookup"><span data-stu-id="72f2d-142">optional</span></span>  <br/> ||<span data-ttu-id="72f2d-143">Valores del tipo xsd: unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="72f2d-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="72f2d-144">Orientation</span><span class="sxs-lookup"><span data-stu-id="72f2d-144">Orientation</span></span>  <br/> |<span data-ttu-id="72f2d-145">xsd: int</span><span class="sxs-lookup"><span data-stu-id="72f2d-145">xsd:int</span></span>  <br/> |<span data-ttu-id="72f2d-146">opcional</span><span class="sxs-lookup"><span data-stu-id="72f2d-146">optional</span></span>  <br/> ||<span data-ttu-id="72f2d-147">Valores del tipo xsd: int.</span><span class="sxs-lookup"><span data-stu-id="72f2d-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="72f2d-148">DePrecision</span><span class="sxs-lookup"><span data-stu-id="72f2d-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="72f2d-149">xsd: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="72f2d-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="72f2d-150">opcional</span><span class="sxs-lookup"><span data-stu-id="72f2d-150">optional</span></span>  <br/> ||<span data-ttu-id="72f2d-151">Valores del tipo xsd: unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="72f2d-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="72f2d-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="72f2d-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="72f2d-153">xsd: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="72f2d-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="72f2d-154">opcional</span><span class="sxs-lookup"><span data-stu-id="72f2d-154">optional</span></span>  <br/> ||<span data-ttu-id="72f2d-155">Valores del tipo xsd: unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="72f2d-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="72f2d-156">Quality</span><span class="sxs-lookup"><span data-stu-id="72f2d-156">Quality</span></span>  <br/> |<span data-ttu-id="72f2d-157">xsd: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="72f2d-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="72f2d-158">opcional</span><span class="sxs-lookup"><span data-stu-id="72f2d-158">optional</span></span>  <br/> ||<span data-ttu-id="72f2d-159">Valores del tipo xsd: unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="72f2d-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="72f2d-160">Tacha</span><span class="sxs-lookup"><span data-stu-id="72f2d-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="72f2d-161">xsd: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="72f2d-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="72f2d-162">opcional</span><span class="sxs-lookup"><span data-stu-id="72f2d-162">optional</span></span>  <br/> ||<span data-ttu-id="72f2d-163">Valores del tipo xsd: unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="72f2d-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="72f2d-164">Underline</span><span class="sxs-lookup"><span data-stu-id="72f2d-164">Underline</span></span>  <br/> |<span data-ttu-id="72f2d-165">xsd: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="72f2d-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="72f2d-166">opcional</span><span class="sxs-lookup"><span data-stu-id="72f2d-166">optional</span></span>  <br/> ||<span data-ttu-id="72f2d-167">Valores del tipo xsd: unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="72f2d-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="72f2d-168">Peso</span><span class="sxs-lookup"><span data-stu-id="72f2d-168">Weight</span></span>  <br/> |<span data-ttu-id="72f2d-169">xsd: int</span><span class="sxs-lookup"><span data-stu-id="72f2d-169">xsd:int</span></span>  <br/> |<span data-ttu-id="72f2d-170">opcional</span><span class="sxs-lookup"><span data-stu-id="72f2d-170">optional</span></span>  <br/> ||<span data-ttu-id="72f2d-171">Valores del tipo xsd: int.</span><span class="sxs-lookup"><span data-stu-id="72f2d-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="72f2d-172">Width</span><span class="sxs-lookup"><span data-stu-id="72f2d-172">Width</span></span>  <br/> |<span data-ttu-id="72f2d-173">xsd: int</span><span class="sxs-lookup"><span data-stu-id="72f2d-173">xsd:int</span></span>  <br/> |<span data-ttu-id="72f2d-174">opcional</span><span class="sxs-lookup"><span data-stu-id="72f2d-174">optional</span></span>  <br/> ||<span data-ttu-id="72f2d-175">Valores del tipo xsd: int.</span><span class="sxs-lookup"><span data-stu-id="72f2d-175">Values of the xsd:int type.</span></span>  <br/> |
   

