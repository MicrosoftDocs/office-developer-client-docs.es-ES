---
title: Elemento FaceName (FaceNames_Type complexType) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: Contiene información acerca de una fuente.
ms.openlocfilehash: 773b5f10607cc6d515671d93d7d4abd9e39e72ff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541018"
---
# <a name="facename-element-facenames_type-complextype-visio-xml"></a><span data-ttu-id="b8943-103">Elemento FaceName (FaceNames_Type complexType) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="b8943-103">FaceName element (FaceNames_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="b8943-104">Contiene información acerca de una fuente.</span><span class="sxs-lookup"><span data-stu-id="b8943-104">Contains information about a font.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b8943-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b8943-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b8943-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="b8943-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b8943-107">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="b8943-107">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b8943-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b8943-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b8943-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b8943-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b8943-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b8943-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b8943-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="b8943-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b8943-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="b8943-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b8943-113">Definición</span><span class="sxs-lookup"><span data-stu-id="b8943-113">Definition</span></span>

```XML
< xs:element name="FaceName" type="FaceName_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element > 
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b8943-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="b8943-114">Elements and attributes</span></span>

<span data-ttu-id="b8943-115">Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="b8943-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b8943-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b8943-116">Parent elements</span></span>

|<span data-ttu-id="b8943-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b8943-117">**Element**</span></span>|<span data-ttu-id="b8943-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b8943-118">**Type**</span></span>|<span data-ttu-id="b8943-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b8943-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b8943-120">FaceNames</span><span class="sxs-lookup"><span data-stu-id="b8943-120">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b8943-121">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="b8943-121">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b8943-122">Contiene una colección de **elementos FaceName.**</span><span class="sxs-lookup"><span data-stu-id="b8943-122">Contains a collection of **FaceName** elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b8943-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b8943-123">Child elements</span></span>

<span data-ttu-id="b8943-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b8943-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b8943-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="b8943-125">Attributes</span></span>

|<span data-ttu-id="b8943-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="b8943-126">**Attribute**</span></span>|<span data-ttu-id="b8943-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b8943-127">**Type**</span></span>|<span data-ttu-id="b8943-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="b8943-128">**Required**</span></span>|<span data-ttu-id="b8943-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b8943-129">**Description**</span></span>|<span data-ttu-id="b8943-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="b8943-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b8943-131">CharSets</span><span class="sxs-lookup"><span data-stu-id="b8943-131">CharSets</span></span>  <br/> |<span data-ttu-id="b8943-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b8943-132">xsd:string</span></span>  <br/> |<span data-ttu-id="b8943-133">opcional</span><span class="sxs-lookup"><span data-stu-id="b8943-133">optional</span></span>  <br/> |<span data-ttu-id="b8943-134">Los juegos de caracteres admitidos de la fuente.</span><span class="sxs-lookup"><span data-stu-id="b8943-134">The supported character sets of the font.</span></span>  <br/> |<span data-ttu-id="b8943-135">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="b8943-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b8943-136">Flags</span><span class="sxs-lookup"><span data-stu-id="b8943-136">Flags</span></span>  <br/> |<span data-ttu-id="b8943-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b8943-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b8943-138">opcional</span><span class="sxs-lookup"><span data-stu-id="b8943-138">optional</span></span>  <br/> |<span data-ttu-id="b8943-139">Marcas que indican lo siguiente: fuente que falta, fuente predeterminada, fuente asiática, fuente compleja, fuente vertical y tipo de fuente.</span><span class="sxs-lookup"><span data-stu-id="b8943-139">Flags that indicate the following: missing font, default font, asian font, complex font, vertical font, and font type.</span></span>  <br/> |<span data-ttu-id="b8943-140">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b8943-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b8943-141">NameU</span><span class="sxs-lookup"><span data-stu-id="b8943-141">NameU</span></span>  <br/> |<span data-ttu-id="b8943-142">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b8943-142">xsd:string</span></span>  <br/> |<span data-ttu-id="b8943-143">necesario</span><span class="sxs-lookup"><span data-stu-id="b8943-143">required</span></span>  <br/> |<span data-ttu-id="b8943-144">Nombre de la fuente como una cadena Unicode UTF-16.</span><span class="sxs-lookup"><span data-stu-id="b8943-144">The name of the font as a UTF-16 Unicode string.</span></span>  <br/> ||
|<span data-ttu-id="b8943-145">Panos</span><span class="sxs-lookup"><span data-stu-id="b8943-145">Panos</span></span>  <br/> |<span data-ttu-id="b8943-146">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b8943-146">xsd:string</span></span>  <br/> |<span data-ttu-id="b8943-147">opcional</span><span class="sxs-lookup"><span data-stu-id="b8943-147">optional</span></span>  <br/> |<span data-ttu-id="b8943-148">Firma panose de la fuente.</span><span class="sxs-lookup"><span data-stu-id="b8943-148">The panose signature for the font.</span></span> <span data-ttu-id="b8943-149">Panose es un sistema de clasificación para tipos de letra que los clasifica en función de sus características visuales.</span><span class="sxs-lookup"><span data-stu-id="b8943-149">Panose is a classification system for typefaces that categorizes them based upon their visual characteristics.</span></span>  <br/> |<span data-ttu-id="b8943-150">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="b8943-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b8943-151">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="b8943-151">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="b8943-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b8943-152">xsd:string</span></span>  <br/> |<span data-ttu-id="b8943-153">opcional</span><span class="sxs-lookup"><span data-stu-id="b8943-153">optional</span></span>  <br/> |<span data-ttu-id="b8943-154">Intervalos Unicode admitidos de la fuente.</span><span class="sxs-lookup"><span data-stu-id="b8943-154">The supported Unicode ranges of the font.</span></span>  <br/> |<span data-ttu-id="b8943-155">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="b8943-155">Values of the xsd:string type.</span></span>  <br/> |
   

