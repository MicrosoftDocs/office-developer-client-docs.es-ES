---
title: HeaderFooterFont_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: cc51924aa68e3248583be5f717b5813d4a32af2b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397250"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a><span data-ttu-id="618b5-102">HeaderFooterFont_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="618b5-102">HeaderFooterFont_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="618b5-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="618b5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="618b5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="618b5-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="618b5-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="618b5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="618b5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="618b5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="618b5-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="618b5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="618b5-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="618b5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="618b5-109">Definición</span><span class="sxs-lookup"><span data-stu-id="618b5-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="618b5-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="618b5-110">Elements and attributes</span></span>

<span data-ttu-id="618b5-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="618b5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="618b5-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="618b5-112">Child elements</span></span>

<span data-ttu-id="618b5-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="618b5-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="618b5-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="618b5-114">Attributes</span></span>

|<span data-ttu-id="618b5-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="618b5-115">**Attribute**</span></span>|<span data-ttu-id="618b5-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="618b5-116">**Type**</span></span>|<span data-ttu-id="618b5-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="618b5-117">**Required**</span></span>|<span data-ttu-id="618b5-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="618b5-118">**Description**</span></span>|<span data-ttu-id="618b5-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="618b5-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="618b5-120">Juego de caracteres</span><span class="sxs-lookup"><span data-stu-id="618b5-120">CharSet</span></span>  <br/> |<span data-ttu-id="618b5-121">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="618b5-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="618b5-122">opcional</span><span class="sxs-lookup"><span data-stu-id="618b5-122">optional</span></span>  <br/> ||<span data-ttu-id="618b5-123">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="618b5-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="618b5-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="618b5-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="618b5-125">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="618b5-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="618b5-126">opcional</span><span class="sxs-lookup"><span data-stu-id="618b5-126">optional</span></span>  <br/> ||<span data-ttu-id="618b5-127">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="618b5-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="618b5-128">Escape</span><span class="sxs-lookup"><span data-stu-id="618b5-128">Escapement</span></span>  <br/> |<span data-ttu-id="618b5-129">xsd: int</span><span class="sxs-lookup"><span data-stu-id="618b5-129">xsd:int</span></span>  <br/> |<span data-ttu-id="618b5-130">opcional</span><span class="sxs-lookup"><span data-stu-id="618b5-130">optional</span></span>  <br/> ||<span data-ttu-id="618b5-131">Valores del tipo XSD: int.</span><span class="sxs-lookup"><span data-stu-id="618b5-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="618b5-132">Nombre de fuente</span><span class="sxs-lookup"><span data-stu-id="618b5-132">FaceName</span></span>  <br/> |<span data-ttu-id="618b5-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="618b5-133">xsd:string</span></span>  <br/> |<span data-ttu-id="618b5-134">opcional</span><span class="sxs-lookup"><span data-stu-id="618b5-134">optional</span></span>  <br/> ||<span data-ttu-id="618b5-135">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="618b5-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="618b5-136">Alto</span><span class="sxs-lookup"><span data-stu-id="618b5-136">Height</span></span>  <br/> |<span data-ttu-id="618b5-137">xsd: int</span><span class="sxs-lookup"><span data-stu-id="618b5-137">xsd:int</span></span>  <br/> |<span data-ttu-id="618b5-138">opcional</span><span class="sxs-lookup"><span data-stu-id="618b5-138">optional</span></span>  <br/> ||<span data-ttu-id="618b5-139">Valores del tipo XSD: int.</span><span class="sxs-lookup"><span data-stu-id="618b5-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="618b5-140">Cursiva</span><span class="sxs-lookup"><span data-stu-id="618b5-140">Italic</span></span>  <br/> |<span data-ttu-id="618b5-141">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="618b5-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="618b5-142">opcional</span><span class="sxs-lookup"><span data-stu-id="618b5-142">optional</span></span>  <br/> ||<span data-ttu-id="618b5-143">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="618b5-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="618b5-144">Orientation</span><span class="sxs-lookup"><span data-stu-id="618b5-144">Orientation</span></span>  <br/> |<span data-ttu-id="618b5-145">xsd: int</span><span class="sxs-lookup"><span data-stu-id="618b5-145">xsd:int</span></span>  <br/> |<span data-ttu-id="618b5-146">opcional</span><span class="sxs-lookup"><span data-stu-id="618b5-146">optional</span></span>  <br/> ||<span data-ttu-id="618b5-147">Valores del tipo XSD: int.</span><span class="sxs-lookup"><span data-stu-id="618b5-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="618b5-148">OutPrecision</span><span class="sxs-lookup"><span data-stu-id="618b5-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="618b5-149">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="618b5-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="618b5-150">opcional</span><span class="sxs-lookup"><span data-stu-id="618b5-150">optional</span></span>  <br/> ||<span data-ttu-id="618b5-151">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="618b5-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="618b5-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="618b5-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="618b5-153">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="618b5-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="618b5-154">opcional</span><span class="sxs-lookup"><span data-stu-id="618b5-154">optional</span></span>  <br/> ||<span data-ttu-id="618b5-155">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="618b5-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="618b5-156">Calidad</span><span class="sxs-lookup"><span data-stu-id="618b5-156">Quality</span></span>  <br/> |<span data-ttu-id="618b5-157">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="618b5-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="618b5-158">opcional</span><span class="sxs-lookup"><span data-stu-id="618b5-158">optional</span></span>  <br/> ||<span data-ttu-id="618b5-159">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="618b5-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="618b5-160">Tachado</span><span class="sxs-lookup"><span data-stu-id="618b5-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="618b5-161">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="618b5-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="618b5-162">opcional</span><span class="sxs-lookup"><span data-stu-id="618b5-162">optional</span></span>  <br/> ||<span data-ttu-id="618b5-163">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="618b5-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="618b5-164">Subrayado</span><span class="sxs-lookup"><span data-stu-id="618b5-164">Underline</span></span>  <br/> |<span data-ttu-id="618b5-165">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="618b5-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="618b5-166">opcional</span><span class="sxs-lookup"><span data-stu-id="618b5-166">optional</span></span>  <br/> ||<span data-ttu-id="618b5-167">Valores del tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="618b5-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="618b5-168">Grosor</span><span class="sxs-lookup"><span data-stu-id="618b5-168">Weight</span></span>  <br/> |<span data-ttu-id="618b5-169">xsd: int</span><span class="sxs-lookup"><span data-stu-id="618b5-169">xsd:int</span></span>  <br/> |<span data-ttu-id="618b5-170">opcional</span><span class="sxs-lookup"><span data-stu-id="618b5-170">optional</span></span>  <br/> ||<span data-ttu-id="618b5-171">Valores del tipo XSD: int.</span><span class="sxs-lookup"><span data-stu-id="618b5-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="618b5-172">Ancho</span><span class="sxs-lookup"><span data-stu-id="618b5-172">Width</span></span>  <br/> |<span data-ttu-id="618b5-173">xsd: int</span><span class="sxs-lookup"><span data-stu-id="618b5-173">xsd:int</span></span>  <br/> |<span data-ttu-id="618b5-174">opcional</span><span class="sxs-lookup"><span data-stu-id="618b5-174">optional</span></span>  <br/> ||<span data-ttu-id="618b5-175">Valores del tipo XSD: int.</span><span class="sxs-lookup"><span data-stu-id="618b5-175">Values of the xsd:int type.</span></span>  <br/> |
   

