---
title: Elemento DocumentSheet (VisioDocument_Type complexType) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: Especifica una estructura DocumentSheet.
ms.openlocfilehash: 279fca457163d5bcbdda885c11c589bfcde0baa9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540045"
---
# <a name="documentsheet-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="193e5-103">Elemento DocumentSheet (VisioDocument_Type complexType) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="193e5-103">DocumentSheet element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="193e5-104">Especifica una estructura DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="193e5-104">Specifies a DocumentSheet structure.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="193e5-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="193e5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="193e5-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="193e5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="193e5-107">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="193e5-107">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="193e5-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="193e5-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="193e5-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="193e5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="193e5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="193e5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="193e5-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="193e5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="193e5-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="193e5-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="193e5-113">Definición</span><span class="sxs-lookup"><span data-stu-id="193e5-113">Definition</span></span>

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="193e5-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="193e5-114">Elements and attributes</span></span>

<span data-ttu-id="193e5-115">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="193e5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="193e5-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="193e5-116">Parent elements</span></span>

|<span data-ttu-id="193e5-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="193e5-117">**Element**</span></span>|<span data-ttu-id="193e5-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="193e5-118">**Type**</span></span>|<span data-ttu-id="193e5-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="193e5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="193e5-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="193e5-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="193e5-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="193e5-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="193e5-122">Elemento raíz de un documento de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="193e5-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="193e5-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="193e5-123">Child elements</span></span>

|<span data-ttu-id="193e5-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="193e5-124">**Element**</span></span>|<span data-ttu-id="193e5-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="193e5-125">**Type**</span></span>|<span data-ttu-id="193e5-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="193e5-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="193e5-127">Cell</span><span class="sxs-lookup"><span data-stu-id="193e5-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="193e5-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="193e5-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="193e5-129">Especifica una celda de una hoja de documentos.</span><span class="sxs-lookup"><span data-stu-id="193e5-129">Specifies a cell in a DocumentSheet.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="193e5-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="193e5-130">Attributes</span></span>

|<span data-ttu-id="193e5-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="193e5-131">**Attribute**</span></span>|<span data-ttu-id="193e5-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="193e5-132">**Type**</span></span>|<span data-ttu-id="193e5-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="193e5-133">**Required**</span></span>|<span data-ttu-id="193e5-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="193e5-134">**Description**</span></span>|<span data-ttu-id="193e5-135">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="193e5-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="193e5-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="193e5-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="193e5-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="193e5-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="193e5-138">opcional</span><span class="sxs-lookup"><span data-stu-id="193e5-138">optional</span></span>  <br/> |<span data-ttu-id="193e5-139">Describe si el usuario ha personalizado el nombre.</span><span class="sxs-lookup"><span data-stu-id="193e5-139">Describes whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="193e5-140">Valores del tipo xsd:Boolean.</span><span class="sxs-lookup"><span data-stu-id="193e5-140">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="193e5-141">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="193e5-141">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="193e5-142">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="193e5-142">xsd:boolean</span></span>  <br/> |<span data-ttu-id="193e5-143">opcional</span><span class="sxs-lookup"><span data-stu-id="193e5-143">optional</span></span>  <br/> |<span data-ttu-id="193e5-144">Describe si el usuario ha personalizado el nombre universal.</span><span class="sxs-lookup"><span data-stu-id="193e5-144">Describes whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="193e5-145">Valores del tipo xsd:Boolean.</span><span class="sxs-lookup"><span data-stu-id="193e5-145">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="193e5-146">Nombre</span><span class="sxs-lookup"><span data-stu-id="193e5-146">Name</span></span>  <br/> |<span data-ttu-id="193e5-147">xsd:string</span><span class="sxs-lookup"><span data-stu-id="193e5-147">xsd:string</span></span>  <br/> |<span data-ttu-id="193e5-148">opcional</span><span class="sxs-lookup"><span data-stu-id="193e5-148">optional</span></span>  <br/> |<span data-ttu-id="193e5-149">Especifica el nombre dependiente del idioma de documentSheet.</span><span class="sxs-lookup"><span data-stu-id="193e5-149">Specifies the language-dependent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="193e5-150">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="193e5-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="193e5-151">NameU</span><span class="sxs-lookup"><span data-stu-id="193e5-151">NameU</span></span>  <br/> |<span data-ttu-id="193e5-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="193e5-152">xsd:string</span></span>  <br/> |<span data-ttu-id="193e5-153">opcional</span><span class="sxs-lookup"><span data-stu-id="193e5-153">optional</span></span>  <br/> |<span data-ttu-id="193e5-154">Especifica el nombre independiente del idioma de documentSheet.</span><span class="sxs-lookup"><span data-stu-id="193e5-154">Specifies the language- independent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="193e5-155">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="193e5-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="193e5-156">UniqueID</span><span class="sxs-lookup"><span data-stu-id="193e5-156">UniqueID</span></span>  <br/> |<span data-ttu-id="193e5-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="193e5-157">xsd:string</span></span>  <br/> |<span data-ttu-id="193e5-158">opcional</span><span class="sxs-lookup"><span data-stu-id="193e5-158">optional</span></span>  <br/> |<span data-ttu-id="193e5-159">Cadena opcional.</span><span class="sxs-lookup"><span data-stu-id="193e5-159">Optional string.</span></span> <span data-ttu-id="193e5-160">GUID (identificador único global) que identifica la forma.</span><span class="sxs-lookup"><span data-stu-id="193e5-160">A GUID (globally unique identifier) identifying the shape.</span></span>  <br/> |<span data-ttu-id="193e5-161">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="193e5-161">Values of the xsd:string type.</span></span>  <br/> |
   

