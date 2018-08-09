---
title: Elemento de nombre de fuente (FaceNames_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: Contiene información acerca de una fuente.
ms.openlocfilehash: 8a66d5294e239e4540939cc7053e1f67a777144d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822086"
---
# <a name="facename-element-facenamestype-complextype-visio-xml"></a><span data-ttu-id="ee31d-103">Elemento de nombre de fuente (FaceNames_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="ee31d-103">FaceName element (FaceNames_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ee31d-104">Contiene información acerca de una fuente.</span><span class="sxs-lookup"><span data-stu-id="ee31d-104">Contains information about a font.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ee31d-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ee31d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ee31d-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="ee31d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ee31d-107">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="ee31d-107">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ee31d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ee31d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ee31d-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ee31d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ee31d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ee31d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ee31d-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="ee31d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ee31d-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="ee31d-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ee31d-113">Definición</span><span class="sxs-lookup"><span data-stu-id="ee31d-113">Definition</span></span>

```XML
< xs:element name="FaceName" type="FaceName_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element > 
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ee31d-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="ee31d-114">Elements and attributes</span></span>

<span data-ttu-id="ee31d-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="ee31d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ee31d-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ee31d-116">Parent elements</span></span>

|<span data-ttu-id="ee31d-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="ee31d-117">**Element**</span></span>|<span data-ttu-id="ee31d-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ee31d-118">**Type**</span></span>|<span data-ttu-id="ee31d-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ee31d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ee31d-120">FaceNames</span><span class="sxs-lookup"><span data-stu-id="ee31d-120">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ee31d-121">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="ee31d-121">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ee31d-122">Contiene una colección de elementos de **nombre de fuente** .</span><span class="sxs-lookup"><span data-stu-id="ee31d-122">Contains a collection of **FaceName** elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ee31d-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ee31d-123">Child elements</span></span>

<span data-ttu-id="ee31d-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ee31d-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ee31d-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="ee31d-125">Attributes</span></span>

|<span data-ttu-id="ee31d-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="ee31d-126">**Attribute**</span></span>|<span data-ttu-id="ee31d-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ee31d-127">**Type**</span></span>|<span data-ttu-id="ee31d-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="ee31d-128">**Required**</span></span>|<span data-ttu-id="ee31d-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ee31d-129">**Description**</span></span>|<span data-ttu-id="ee31d-130">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="ee31d-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ee31d-131">Juegos de caracteres</span><span class="sxs-lookup"><span data-stu-id="ee31d-131">CharSets</span></span>  <br/> |<span data-ttu-id="ee31d-132">xsd: String</span><span class="sxs-lookup"><span data-stu-id="ee31d-132">xsd:string</span></span>  <br/> |<span data-ttu-id="ee31d-133">opcional</span><span class="sxs-lookup"><span data-stu-id="ee31d-133">optional</span></span>  <br/> |<span data-ttu-id="ee31d-134">Los conjuntos de caracteres compatibles de la fuente.</span><span class="sxs-lookup"><span data-stu-id="ee31d-134">The supported character sets of the font.</span></span>  <br/> |<span data-ttu-id="ee31d-135">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="ee31d-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ee31d-136">Marcas</span><span class="sxs-lookup"><span data-stu-id="ee31d-136">Flags</span></span>  <br/> |<span data-ttu-id="ee31d-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ee31d-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ee31d-138">opcional</span><span class="sxs-lookup"><span data-stu-id="ee31d-138">optional</span></span>  <br/> |<span data-ttu-id="ee31d-139">Marcas que muestran lo siguiente: falta una fuente, fuente predeterminada, fuente asiática, fuente complejo, fuente vertical y tipo de fuente.</span><span class="sxs-lookup"><span data-stu-id="ee31d-139">Flags that indicate the following: missing font, default font, asian font, complex font, vertical font, and font type.</span></span>  <br/> |<span data-ttu-id="ee31d-140">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ee31d-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ee31d-141">NameU</span><span class="sxs-lookup"><span data-stu-id="ee31d-141">NameU</span></span>  <br/> |<span data-ttu-id="ee31d-142">xsd: String</span><span class="sxs-lookup"><span data-stu-id="ee31d-142">xsd:string</span></span>  <br/> |<span data-ttu-id="ee31d-143">necesario</span><span class="sxs-lookup"><span data-stu-id="ee31d-143">required</span></span>  <br/> |<span data-ttu-id="ee31d-144">El nombre de la fuente como una cadena Unicode UTF-16.</span><span class="sxs-lookup"><span data-stu-id="ee31d-144">The name of the font as a UTF-16 Unicode string.</span></span>  <br/> ||
|<span data-ttu-id="ee31d-145">Panos</span><span class="sxs-lookup"><span data-stu-id="ee31d-145">Panos</span></span>  <br/> |<span data-ttu-id="ee31d-146">xsd: String</span><span class="sxs-lookup"><span data-stu-id="ee31d-146">xsd:string</span></span>  <br/> |<span data-ttu-id="ee31d-147">opcional</span><span class="sxs-lookup"><span data-stu-id="ee31d-147">optional</span></span>  <br/> |<span data-ttu-id="ee31d-148">La firma panose para la fuente.</span><span class="sxs-lookup"><span data-stu-id="ee31d-148">The panose signature for the font.</span></span> <span data-ttu-id="ee31d-149">Panose es un sistema de clasificación para los tipos de letra que categorice a ellos en función de sus características visuales.</span><span class="sxs-lookup"><span data-stu-id="ee31d-149">Panose is a classification system for typefaces that categorizes them based upon their visual characteristics.</span></span>  <br/> |<span data-ttu-id="ee31d-150">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="ee31d-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ee31d-151">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="ee31d-151">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="ee31d-152">xsd: String</span><span class="sxs-lookup"><span data-stu-id="ee31d-152">xsd:string</span></span>  <br/> |<span data-ttu-id="ee31d-153">opcional</span><span class="sxs-lookup"><span data-stu-id="ee31d-153">optional</span></span>  <br/> |<span data-ttu-id="ee31d-154">Los intervalos admitidos de Unicode de la fuente.</span><span class="sxs-lookup"><span data-stu-id="ee31d-154">The supported Unicode ranges of the font.</span></span>  <br/> |<span data-ttu-id="ee31d-155">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="ee31d-155">Values of the xsd:string type.</span></span>  <br/> |
   

