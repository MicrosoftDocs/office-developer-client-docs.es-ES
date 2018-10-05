---
title: Elemento de nombre de fuente (FaceNames_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: Contiene información acerca de una fuente.
ms.openlocfilehash: 4c8f047d655be167dc058b3e29ac62161887ce99
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389781"
---
# <a name="facename-element-facenamestype-complextype-visio-xml"></a><span data-ttu-id="df01a-103">Elemento de nombre de fuente (FaceNames_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="df01a-103">FaceName element (FaceNames_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="df01a-104">Contiene información acerca de una fuente.</span><span class="sxs-lookup"><span data-stu-id="df01a-104">Contains information about a font.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="df01a-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="df01a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="df01a-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="df01a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="df01a-107">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="df01a-107">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="df01a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="df01a-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="df01a-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="df01a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="df01a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="df01a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="df01a-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="df01a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="df01a-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="df01a-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="df01a-113">Definición</span><span class="sxs-lookup"><span data-stu-id="df01a-113">Definition</span></span>

```XML
< xs:element name="FaceName" type="FaceName_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element > 
```

## <a name="elements-and-attributes"></a><span data-ttu-id="df01a-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="df01a-114">Elements and attributes</span></span>

<span data-ttu-id="df01a-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="df01a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="df01a-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="df01a-116">Parent elements</span></span>

|<span data-ttu-id="df01a-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="df01a-117">**Element**</span></span>|<span data-ttu-id="df01a-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="df01a-118">**Type**</span></span>|<span data-ttu-id="df01a-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="df01a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="df01a-120">FaceNames</span><span class="sxs-lookup"><span data-stu-id="df01a-120">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="df01a-121">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="df01a-121">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="df01a-122">Contiene una colección de elementos de **nombre de fuente** .</span><span class="sxs-lookup"><span data-stu-id="df01a-122">Contains a collection of **FaceName** elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="df01a-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="df01a-123">Child elements</span></span>

<span data-ttu-id="df01a-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="df01a-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="df01a-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="df01a-125">Attributes</span></span>

|<span data-ttu-id="df01a-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="df01a-126">**Attribute**</span></span>|<span data-ttu-id="df01a-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="df01a-127">**Type**</span></span>|<span data-ttu-id="df01a-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="df01a-128">**Required**</span></span>|<span data-ttu-id="df01a-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="df01a-129">**Description**</span></span>|<span data-ttu-id="df01a-130">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="df01a-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="df01a-131">Juegos de caracteres</span><span class="sxs-lookup"><span data-stu-id="df01a-131">CharSets</span></span>  <br/> |<span data-ttu-id="df01a-132">xsd: String</span><span class="sxs-lookup"><span data-stu-id="df01a-132">xsd:string</span></span>  <br/> |<span data-ttu-id="df01a-133">opcional</span><span class="sxs-lookup"><span data-stu-id="df01a-133">optional</span></span>  <br/> |<span data-ttu-id="df01a-134">Los conjuntos de caracteres compatibles de la fuente.</span><span class="sxs-lookup"><span data-stu-id="df01a-134">The supported character sets of the font.</span></span>  <br/> |<span data-ttu-id="df01a-135">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="df01a-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="df01a-136">Marcas</span><span class="sxs-lookup"><span data-stu-id="df01a-136">Flags</span></span>  <br/> |<span data-ttu-id="df01a-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="df01a-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="df01a-138">opcional</span><span class="sxs-lookup"><span data-stu-id="df01a-138">optional</span></span>  <br/> |<span data-ttu-id="df01a-139">Marcas que muestran lo siguiente: falta una fuente, fuente predeterminada, fuente asiática, fuente complejo, fuente vertical y tipo de fuente.</span><span class="sxs-lookup"><span data-stu-id="df01a-139">Flags that indicate the following: missing font, default font, asian font, complex font, vertical font, and font type.</span></span>  <br/> |<span data-ttu-id="df01a-140">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="df01a-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="df01a-141">NameU</span><span class="sxs-lookup"><span data-stu-id="df01a-141">NameU</span></span>  <br/> |<span data-ttu-id="df01a-142">xsd: String</span><span class="sxs-lookup"><span data-stu-id="df01a-142">xsd:string</span></span>  <br/> |<span data-ttu-id="df01a-143">necesario</span><span class="sxs-lookup"><span data-stu-id="df01a-143">required</span></span>  <br/> |<span data-ttu-id="df01a-144">El nombre de la fuente como una cadena Unicode UTF-16.</span><span class="sxs-lookup"><span data-stu-id="df01a-144">The name of the font as a UTF-16 Unicode string.</span></span>  <br/> ||
|<span data-ttu-id="df01a-145">Panos</span><span class="sxs-lookup"><span data-stu-id="df01a-145">Panos</span></span>  <br/> |<span data-ttu-id="df01a-146">xsd: String</span><span class="sxs-lookup"><span data-stu-id="df01a-146">xsd:string</span></span>  <br/> |<span data-ttu-id="df01a-147">opcional</span><span class="sxs-lookup"><span data-stu-id="df01a-147">optional</span></span>  <br/> |<span data-ttu-id="df01a-148">La firma panose para la fuente.</span><span class="sxs-lookup"><span data-stu-id="df01a-148">The panose signature for the font.</span></span> <span data-ttu-id="df01a-149">Panose es un sistema de clasificación para los tipos de letra que categorice a ellos en función de sus características visuales.</span><span class="sxs-lookup"><span data-stu-id="df01a-149">Panose is a classification system for typefaces that categorizes them based upon their visual characteristics.</span></span>  <br/> |<span data-ttu-id="df01a-150">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="df01a-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="df01a-151">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="df01a-151">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="df01a-152">xsd: String</span><span class="sxs-lookup"><span data-stu-id="df01a-152">xsd:string</span></span>  <br/> |<span data-ttu-id="df01a-153">opcional</span><span class="sxs-lookup"><span data-stu-id="df01a-153">optional</span></span>  <br/> |<span data-ttu-id="df01a-154">Los intervalos admitidos de Unicode de la fuente.</span><span class="sxs-lookup"><span data-stu-id="df01a-154">The supported Unicode ranges of the font.</span></span>  <br/> |<span data-ttu-id="df01a-155">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="df01a-155">Values of the xsd:string type.</span></span>  <br/> |
   

