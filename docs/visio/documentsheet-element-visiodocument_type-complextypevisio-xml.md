---
title: Elemento DocumentSheet (complexType VisioDocument_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: Especifica una estructura DocumentSheet.
ms.openlocfilehash: a2594e0325cc2743036a03998eb7ac71ed2183c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356367"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="a8c53-103">Elemento DocumentSheet (complexType VisioDocument_Type) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="a8c53-103">DocumentSheet element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a8c53-104">Especifica una estructura DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="a8c53-104">Specifies a DocumentSheet structure.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a8c53-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a8c53-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8c53-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="a8c53-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a8c53-107">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="a8c53-107">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a8c53-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a8c53-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a8c53-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a8c53-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a8c53-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="a8c53-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a8c53-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="a8c53-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a8c53-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="a8c53-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a8c53-113">Definición</span><span class="sxs-lookup"><span data-stu-id="a8c53-113">Definition</span></span>

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a8c53-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="a8c53-114">Elements and attributes</span></span>

<span data-ttu-id="a8c53-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="a8c53-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a8c53-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a8c53-116">Parent elements</span></span>

|<span data-ttu-id="a8c53-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a8c53-117">**Element**</span></span>|<span data-ttu-id="a8c53-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a8c53-118">**Type**</span></span>|<span data-ttu-id="a8c53-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a8c53-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a8c53-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="a8c53-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="a8c53-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="a8c53-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a8c53-122">El elemento raíz de un documento de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="a8c53-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a8c53-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a8c53-123">Child elements</span></span>

|<span data-ttu-id="a8c53-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a8c53-124">**Element**</span></span>|<span data-ttu-id="a8c53-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a8c53-125">**Type**</span></span>|<span data-ttu-id="a8c53-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a8c53-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a8c53-127">Cell</span><span class="sxs-lookup"><span data-stu-id="a8c53-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="a8c53-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="a8c53-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a8c53-129">Especifica una celda en un DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="a8c53-129">Specifies a cell in a DocumentSheet.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a8c53-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="a8c53-130">Attributes</span></span>

|<span data-ttu-id="a8c53-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="a8c53-131">**Attribute**</span></span>|<span data-ttu-id="a8c53-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a8c53-132">**Type**</span></span>|<span data-ttu-id="a8c53-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="a8c53-133">**Required**</span></span>|<span data-ttu-id="a8c53-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a8c53-134">**Description**</span></span>|<span data-ttu-id="a8c53-135">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="a8c53-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a8c53-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="a8c53-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="a8c53-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="a8c53-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a8c53-138">opcional</span><span class="sxs-lookup"><span data-stu-id="a8c53-138">optional</span></span>  <br/> |<span data-ttu-id="a8c53-139">Describe si el usuario ha personalizado el nombre.</span><span class="sxs-lookup"><span data-stu-id="a8c53-139">Describes whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="a8c53-140">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="a8c53-140">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="a8c53-141">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="a8c53-141">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="a8c53-142">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="a8c53-142">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a8c53-143">opcional</span><span class="sxs-lookup"><span data-stu-id="a8c53-143">optional</span></span>  <br/> |<span data-ttu-id="a8c53-144">Describe si el usuario ha personalizado el nombre universal.</span><span class="sxs-lookup"><span data-stu-id="a8c53-144">Describes whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="a8c53-145">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="a8c53-145">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="a8c53-146">Nombre</span><span class="sxs-lookup"><span data-stu-id="a8c53-146">Name</span></span>  <br/> |<span data-ttu-id="a8c53-147">xsd: String</span><span class="sxs-lookup"><span data-stu-id="a8c53-147">xsd:string</span></span>  <br/> |<span data-ttu-id="a8c53-148">opcional</span><span class="sxs-lookup"><span data-stu-id="a8c53-148">optional</span></span>  <br/> |<span data-ttu-id="a8c53-149">Especifica el nombre dependiente del idioma de DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="a8c53-149">Specifies the language-dependent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="a8c53-150">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="a8c53-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a8c53-151">NameU</span><span class="sxs-lookup"><span data-stu-id="a8c53-151">NameU</span></span>  <br/> |<span data-ttu-id="a8c53-152">xsd: String</span><span class="sxs-lookup"><span data-stu-id="a8c53-152">xsd:string</span></span>  <br/> |<span data-ttu-id="a8c53-153">opcional</span><span class="sxs-lookup"><span data-stu-id="a8c53-153">optional</span></span>  <br/> |<span data-ttu-id="a8c53-154">Especifica el nombre independiente del idioma de DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="a8c53-154">Specifies the language- independent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="a8c53-155">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="a8c53-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a8c53-156">UniqueID</span><span class="sxs-lookup"><span data-stu-id="a8c53-156">UniqueID</span></span>  <br/> |<span data-ttu-id="a8c53-157">xsd: String</span><span class="sxs-lookup"><span data-stu-id="a8c53-157">xsd:string</span></span>  <br/> |<span data-ttu-id="a8c53-158">opcional</span><span class="sxs-lookup"><span data-stu-id="a8c53-158">optional</span></span>  <br/> |<span data-ttu-id="a8c53-159">String opcional.</span><span class="sxs-lookup"><span data-stu-id="a8c53-159">Optional string.</span></span> <span data-ttu-id="a8c53-160">Un GUID (identificador único global) que identifica la forma.</span><span class="sxs-lookup"><span data-stu-id="a8c53-160">A GUID (globally unique identifier) identifying the shape.</span></span>  <br/> |<span data-ttu-id="a8c53-161">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="a8c53-161">Values of the xsd:string type.</span></span>  <br/> |
   

