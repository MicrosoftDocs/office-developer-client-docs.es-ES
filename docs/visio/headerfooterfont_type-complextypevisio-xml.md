---
title: HeaderFooterFont_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: 1d7c4d6850e4a8ea1933ae751c580d09e0dd67bd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822262"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a><span data-ttu-id="363c8-102">HeaderFooterFont_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="363c8-102">HeaderFooterFont_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="363c8-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="363c8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="363c8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="363c8-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="363c8-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="363c8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="363c8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="363c8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="363c8-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="363c8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="363c8-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="363c8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="363c8-109">Definición</span><span class="sxs-lookup"><span data-stu-id="363c8-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="363c8-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="363c8-110">Elements and attributes</span></span>

<span data-ttu-id="363c8-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="363c8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="363c8-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="363c8-112">Child elements</span></span>

<span data-ttu-id="363c8-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="363c8-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="363c8-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="363c8-114">Attributes</span></span>

|<span data-ttu-id="363c8-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="363c8-115">**Attribute**</span></span>|<span data-ttu-id="363c8-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="363c8-116">**Type**</span></span>|<span data-ttu-id="363c8-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="363c8-117">**Required**</span></span>|<span data-ttu-id="363c8-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="363c8-118">**Description**</span></span>|<span data-ttu-id="363c8-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="363c8-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="363c8-120">Juego de caracteres</span><span class="sxs-lookup"><span data-stu-id="363c8-120">CharSet</span></span>  <br/> |<span data-ttu-id="363c8-121">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="363c8-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="363c8-122">opcional</span><span class="sxs-lookup"><span data-stu-id="363c8-122">optional</span></span>  <br/> ||<span data-ttu-id="363c8-123">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="363c8-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="363c8-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="363c8-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="363c8-125">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="363c8-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="363c8-126">opcional</span><span class="sxs-lookup"><span data-stu-id="363c8-126">optional</span></span>  <br/> ||<span data-ttu-id="363c8-127">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="363c8-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="363c8-128">Escape</span><span class="sxs-lookup"><span data-stu-id="363c8-128">Escapement</span></span>  <br/> |<span data-ttu-id="363c8-129">xsd: int</span><span class="sxs-lookup"><span data-stu-id="363c8-129">xsd:int</span></span>  <br/> |<span data-ttu-id="363c8-130">opcional</span><span class="sxs-lookup"><span data-stu-id="363c8-130">optional</span></span>  <br/> ||<span data-ttu-id="363c8-131">Valores del tipo XSD: int.</span><span class="sxs-lookup"><span data-stu-id="363c8-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="363c8-132">Nombre de fuente</span><span class="sxs-lookup"><span data-stu-id="363c8-132">FaceName</span></span>  <br/> |<span data-ttu-id="363c8-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="363c8-133">xsd:string</span></span>  <br/> |<span data-ttu-id="363c8-134">opcional</span><span class="sxs-lookup"><span data-stu-id="363c8-134">optional</span></span>  <br/> ||<span data-ttu-id="363c8-135">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="363c8-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="363c8-136">Alto</span><span class="sxs-lookup"><span data-stu-id="363c8-136">Height</span></span>  <br/> |<span data-ttu-id="363c8-137">xsd: int</span><span class="sxs-lookup"><span data-stu-id="363c8-137">xsd:int</span></span>  <br/> |<span data-ttu-id="363c8-138">opcional</span><span class="sxs-lookup"><span data-stu-id="363c8-138">optional</span></span>  <br/> ||<span data-ttu-id="363c8-139">Valores del tipo XSD: int.</span><span class="sxs-lookup"><span data-stu-id="363c8-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="363c8-140">Cursiva</span><span class="sxs-lookup"><span data-stu-id="363c8-140">Italic</span></span>  <br/> |<span data-ttu-id="363c8-141">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="363c8-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="363c8-142">opcional</span><span class="sxs-lookup"><span data-stu-id="363c8-142">optional</span></span>  <br/> ||<span data-ttu-id="363c8-143">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="363c8-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="363c8-144">Orientation</span><span class="sxs-lookup"><span data-stu-id="363c8-144">Orientation</span></span>  <br/> |<span data-ttu-id="363c8-145">xsd: int</span><span class="sxs-lookup"><span data-stu-id="363c8-145">xsd:int</span></span>  <br/> |<span data-ttu-id="363c8-146">opcional</span><span class="sxs-lookup"><span data-stu-id="363c8-146">optional</span></span>  <br/> ||<span data-ttu-id="363c8-147">Valores del tipo XSD: int.</span><span class="sxs-lookup"><span data-stu-id="363c8-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="363c8-148">OutPrecision</span><span class="sxs-lookup"><span data-stu-id="363c8-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="363c8-149">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="363c8-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="363c8-150">opcional</span><span class="sxs-lookup"><span data-stu-id="363c8-150">optional</span></span>  <br/> ||<span data-ttu-id="363c8-151">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="363c8-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="363c8-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="363c8-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="363c8-153">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="363c8-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="363c8-154">opcional</span><span class="sxs-lookup"><span data-stu-id="363c8-154">optional</span></span>  <br/> ||<span data-ttu-id="363c8-155">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="363c8-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="363c8-156">Calidad</span><span class="sxs-lookup"><span data-stu-id="363c8-156">Quality</span></span>  <br/> |<span data-ttu-id="363c8-157">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="363c8-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="363c8-158">opcional</span><span class="sxs-lookup"><span data-stu-id="363c8-158">optional</span></span>  <br/> ||<span data-ttu-id="363c8-159">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="363c8-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="363c8-160">Tachado</span><span class="sxs-lookup"><span data-stu-id="363c8-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="363c8-161">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="363c8-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="363c8-162">opcional</span><span class="sxs-lookup"><span data-stu-id="363c8-162">optional</span></span>  <br/> ||<span data-ttu-id="363c8-163">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="363c8-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="363c8-164">Subrayado</span><span class="sxs-lookup"><span data-stu-id="363c8-164">Underline</span></span>  <br/> |<span data-ttu-id="363c8-165">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="363c8-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="363c8-166">opcional</span><span class="sxs-lookup"><span data-stu-id="363c8-166">optional</span></span>  <br/> ||<span data-ttu-id="363c8-167">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="363c8-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="363c8-168">Grosor</span><span class="sxs-lookup"><span data-stu-id="363c8-168">Weight</span></span>  <br/> |<span data-ttu-id="363c8-169">xsd: int</span><span class="sxs-lookup"><span data-stu-id="363c8-169">xsd:int</span></span>  <br/> |<span data-ttu-id="363c8-170">opcional</span><span class="sxs-lookup"><span data-stu-id="363c8-170">optional</span></span>  <br/> ||<span data-ttu-id="363c8-171">Valores del tipo XSD: int.</span><span class="sxs-lookup"><span data-stu-id="363c8-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="363c8-172">Ancho</span><span class="sxs-lookup"><span data-stu-id="363c8-172">Width</span></span>  <br/> |<span data-ttu-id="363c8-173">xsd: int</span><span class="sxs-lookup"><span data-stu-id="363c8-173">xsd:int</span></span>  <br/> |<span data-ttu-id="363c8-174">opcional</span><span class="sxs-lookup"><span data-stu-id="363c8-174">optional</span></span>  <br/> ||<span data-ttu-id="363c8-175">Valores del tipo XSD: int.</span><span class="sxs-lookup"><span data-stu-id="363c8-175">Values of the xsd:int type.</span></span>  <br/> |
   

