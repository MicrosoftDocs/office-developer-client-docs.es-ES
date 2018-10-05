---
title: Elemento DocumentSheet (VisioDocument_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: Especifica una estructura DocumentSheet.
ms.openlocfilehash: a2594e0325cc2743036a03998eb7ac71ed2183c8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383467"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="6ae0f-103">Elemento DocumentSheet (VisioDocument_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="6ae0f-103">DocumentSheet element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="6ae0f-104">Especifica una estructura DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="6ae0f-104">Specifies a DocumentSheet structure.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6ae0f-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6ae0f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6ae0f-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="6ae0f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6ae0f-107">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="6ae0f-107">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6ae0f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6ae0f-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6ae0f-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6ae0f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6ae0f-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6ae0f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6ae0f-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="6ae0f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6ae0f-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="6ae0f-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6ae0f-113">Definición</span><span class="sxs-lookup"><span data-stu-id="6ae0f-113">Definition</span></span>

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6ae0f-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="6ae0f-114">Elements and attributes</span></span>

<span data-ttu-id="6ae0f-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="6ae0f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6ae0f-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6ae0f-116">Parent elements</span></span>

|<span data-ttu-id="6ae0f-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="6ae0f-117">**Element**</span></span>|<span data-ttu-id="6ae0f-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6ae0f-118">**Type**</span></span>|<span data-ttu-id="6ae0f-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6ae0f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6ae0f-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="6ae0f-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="6ae0f-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="6ae0f-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6ae0f-122">El elemento raíz de un documento de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="6ae0f-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6ae0f-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6ae0f-123">Child elements</span></span>

|<span data-ttu-id="6ae0f-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="6ae0f-124">**Element**</span></span>|<span data-ttu-id="6ae0f-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6ae0f-125">**Type**</span></span>|<span data-ttu-id="6ae0f-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6ae0f-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6ae0f-127">Cell</span><span class="sxs-lookup"><span data-stu-id="6ae0f-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="6ae0f-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="6ae0f-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6ae0f-129">Especifica una celda en un DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="6ae0f-129">Specifies a cell in a DocumentSheet.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="6ae0f-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="6ae0f-130">Attributes</span></span>

|<span data-ttu-id="6ae0f-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="6ae0f-131">**Attribute**</span></span>|<span data-ttu-id="6ae0f-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6ae0f-132">**Type**</span></span>|<span data-ttu-id="6ae0f-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="6ae0f-133">**Required**</span></span>|<span data-ttu-id="6ae0f-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6ae0f-134">**Description**</span></span>|<span data-ttu-id="6ae0f-135">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="6ae0f-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6ae0f-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="6ae0f-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="6ae0f-137">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="6ae0f-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6ae0f-138">opcional</span><span class="sxs-lookup"><span data-stu-id="6ae0f-138">optional</span></span>  <br/> |<span data-ttu-id="6ae0f-139">Describe si el nombre se ha personalizado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="6ae0f-139">Describes whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="6ae0f-140">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="6ae0f-140">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="6ae0f-141">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="6ae0f-141">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="6ae0f-142">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="6ae0f-142">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6ae0f-143">opcional</span><span class="sxs-lookup"><span data-stu-id="6ae0f-143">optional</span></span>  <br/> |<span data-ttu-id="6ae0f-144">Describe si se ha personalizado el nombre universal por el usuario.</span><span class="sxs-lookup"><span data-stu-id="6ae0f-144">Describes whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="6ae0f-145">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="6ae0f-145">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="6ae0f-146">Nombre</span><span class="sxs-lookup"><span data-stu-id="6ae0f-146">Name</span></span>  <br/> |<span data-ttu-id="6ae0f-147">xsd: String</span><span class="sxs-lookup"><span data-stu-id="6ae0f-147">xsd:string</span></span>  <br/> |<span data-ttu-id="6ae0f-148">opcional</span><span class="sxs-lookup"><span data-stu-id="6ae0f-148">optional</span></span>  <br/> |<span data-ttu-id="6ae0f-149">Especifica el nombre dependen del idioma de la DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="6ae0f-149">Specifies the language-dependent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="6ae0f-150">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="6ae0f-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6ae0f-151">NameU</span><span class="sxs-lookup"><span data-stu-id="6ae0f-151">NameU</span></span>  <br/> |<span data-ttu-id="6ae0f-152">xsd: String</span><span class="sxs-lookup"><span data-stu-id="6ae0f-152">xsd:string</span></span>  <br/> |<span data-ttu-id="6ae0f-153">opcional</span><span class="sxs-lookup"><span data-stu-id="6ae0f-153">optional</span></span>  <br/> |<span data-ttu-id="6ae0f-154">Especifica el nombre independiente del idioma de la DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="6ae0f-154">Specifies the language- independent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="6ae0f-155">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="6ae0f-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6ae0f-156">UniqueID</span><span class="sxs-lookup"><span data-stu-id="6ae0f-156">UniqueID</span></span>  <br/> |<span data-ttu-id="6ae0f-157">xsd: String</span><span class="sxs-lookup"><span data-stu-id="6ae0f-157">xsd:string</span></span>  <br/> |<span data-ttu-id="6ae0f-158">opcional</span><span class="sxs-lookup"><span data-stu-id="6ae0f-158">optional</span></span>  <br/> |<span data-ttu-id="6ae0f-159">String opcional.</span><span class="sxs-lookup"><span data-stu-id="6ae0f-159">Optional string.</span></span> <span data-ttu-id="6ae0f-160">Un GUID (identificador único global) que identifica la forma.</span><span class="sxs-lookup"><span data-stu-id="6ae0f-160">A GUID (globally unique identifier) identifying the shape.</span></span>  <br/> |<span data-ttu-id="6ae0f-161">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="6ae0f-161">Values of the xsd:string type.</span></span>  <br/> |
   

