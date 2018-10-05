---
title: Elemento HeaderFooter (VisioDocument_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 026926cf-3d0b-984c-897e-9d28346b7ba7
description: Contiene elementos de encabezado y pie de página de un documento.
ms.openlocfilehash: eabb19100c4b37a546c0a271cfba5a0c865a7e83
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384447"
---
# <a name="headerfooter-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="7475d-103">Elemento HeaderFooter (VisioDocument_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="7475d-103">HeaderFooter element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="7475d-104">Contiene elementos de encabezado y pie de página de un documento.</span><span class="sxs-lookup"><span data-stu-id="7475d-104">Contains elements for a document's header and footer.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7475d-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7475d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7475d-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="7475d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7475d-107">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="7475d-107">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7475d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7475d-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7475d-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7475d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7475d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7475d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7475d-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="7475d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7475d-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="7475d-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7475d-113">Definición</span><span class="sxs-lookup"><span data-stu-id="7475d-113">Definition</span></span>

```XML
< xs:element name="HeaderFooter" type="HeaderFooter_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7475d-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="7475d-114">Elements and attributes</span></span>

<span data-ttu-id="7475d-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="7475d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7475d-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7475d-116">Parent elements</span></span>

|<span data-ttu-id="7475d-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="7475d-117">**Element**</span></span>|<span data-ttu-id="7475d-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7475d-118">**Type**</span></span>|<span data-ttu-id="7475d-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7475d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7475d-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="7475d-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="7475d-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="7475d-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7475d-122">El elemento raíz de un documento de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="7475d-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7475d-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7475d-123">Child elements</span></span>

|<span data-ttu-id="7475d-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="7475d-124">**Element**</span></span>|<span data-ttu-id="7475d-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7475d-125">**Type**</span></span>|<span data-ttu-id="7475d-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7475d-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7475d-127">FooterCenter</span><span class="sxs-lookup"><span data-stu-id="7475d-127">FooterCenter</span></span>](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7475d-128">FooterCenter_Type</span><span class="sxs-lookup"><span data-stu-id="7475d-128">FooterCenter_Type</span></span>](footercenter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7475d-129">Contiene la cadena de texto que aparece en la parte central del pie de página de un documento.</span><span class="sxs-lookup"><span data-stu-id="7475d-129">Contains the text string that appears in the center portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="7475d-130">FooterLeft</span><span class="sxs-lookup"><span data-stu-id="7475d-130">FooterLeft</span></span>](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7475d-131">FooterLeft_Type</span><span class="sxs-lookup"><span data-stu-id="7475d-131">FooterLeft_Type</span></span>](footerleft_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7475d-132">Contiene la cadena de texto que aparece en la parte izquierda del pie de página de un documento.</span><span class="sxs-lookup"><span data-stu-id="7475d-132">Contains the text string that appears in the left portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="7475d-133">FooterMargin</span><span class="sxs-lookup"><span data-stu-id="7475d-133">FooterMargin</span></span>](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7475d-134">FooterMargin_Type</span><span class="sxs-lookup"><span data-stu-id="7475d-134">FooterMargin_Type</span></span>](footermargin_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7475d-135">Especifica el margen del pie de página de un documento.</span><span class="sxs-lookup"><span data-stu-id="7475d-135">Specifies the margin of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="7475d-136">FooterRight</span><span class="sxs-lookup"><span data-stu-id="7475d-136">FooterRight</span></span>](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7475d-137">FooterRight_Type</span><span class="sxs-lookup"><span data-stu-id="7475d-137">FooterRight_Type</span></span>](footerright_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7475d-138">Contiene la cadena de texto que aparece en la parte derecha del pie de página de un documento.</span><span class="sxs-lookup"><span data-stu-id="7475d-138">Contains the text string that appears in the right portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="7475d-139">HeaderCenter</span><span class="sxs-lookup"><span data-stu-id="7475d-139">HeaderCenter</span></span>](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7475d-140">HeaderCenter_Type</span><span class="sxs-lookup"><span data-stu-id="7475d-140">HeaderCenter_Type</span></span>](headercenter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7475d-141">Contiene la cadena de texto que aparece en la parte central del encabezado de un documento.</span><span class="sxs-lookup"><span data-stu-id="7475d-141">Contains the text string that appears in the center portion of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="7475d-142">HeaderFooterFont</span><span class="sxs-lookup"><span data-stu-id="7475d-142">HeaderFooterFont</span></span>](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7475d-143">HeaderFooterFont_Type</span><span class="sxs-lookup"><span data-stu-id="7475d-143">HeaderFooterFont_Type</span></span>](headerfooterfont_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7475d-144">Especifica la fuente utilizada para el texto de encabezado y pie de página.</span><span class="sxs-lookup"><span data-stu-id="7475d-144">Specifies the font used for the header and footer text.</span></span>  <br/> |
|[<span data-ttu-id="7475d-145">HeaderLeft</span><span class="sxs-lookup"><span data-stu-id="7475d-145">HeaderLeft</span></span>](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7475d-146">HeaderLeft_Type</span><span class="sxs-lookup"><span data-stu-id="7475d-146">HeaderLeft_Type</span></span>](headerleft_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7475d-147">Contiene la cadena de texto que aparece en la parte izquierda del encabezado de un documento.</span><span class="sxs-lookup"><span data-stu-id="7475d-147">Contains the text string that appears in the left portion of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="7475d-148">HeaderMargin</span><span class="sxs-lookup"><span data-stu-id="7475d-148">HeaderMargin</span></span>](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7475d-149">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="7475d-149">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7475d-150">Especifica el margen del encabezado de un documento.</span><span class="sxs-lookup"><span data-stu-id="7475d-150">Specifies the margin of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="7475d-151">HeaderRight</span><span class="sxs-lookup"><span data-stu-id="7475d-151">HeaderRight</span></span>](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7475d-152">HeaderRight_Type</span><span class="sxs-lookup"><span data-stu-id="7475d-152">HeaderRight_Type</span></span>](headerright_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7475d-153">Contiene la cadena de texto que aparece en la parte derecha del encabezado de un documento.</span><span class="sxs-lookup"><span data-stu-id="7475d-153">Contains the text string that appears in the right portion of a document's header.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="7475d-154">Atributos</span><span class="sxs-lookup"><span data-stu-id="7475d-154">Attributes</span></span>

|<span data-ttu-id="7475d-155">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="7475d-155">**Attribute**</span></span>|<span data-ttu-id="7475d-156">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7475d-156">**Type**</span></span>|<span data-ttu-id="7475d-157">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="7475d-157">**Required**</span></span>|<span data-ttu-id="7475d-158">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7475d-158">**Description**</span></span>|<span data-ttu-id="7475d-159">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="7475d-159">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7475d-160">HeaderFooterColor</span><span class="sxs-lookup"><span data-stu-id="7475d-160">HeaderFooterColor</span></span>  <br/> |<span data-ttu-id="7475d-161">xsd: String</span><span class="sxs-lookup"><span data-stu-id="7475d-161">xsd:string</span></span>  <br/> |<span data-ttu-id="7475d-162">opcional</span><span class="sxs-lookup"><span data-stu-id="7475d-162">optional</span></span>  <br/> |<span data-ttu-id="7475d-163">El valor RGB del color del texto del encabezado y pie de página en notación hexadecimal; Por ejemplo, #rrggbb.</span><span class="sxs-lookup"><span data-stu-id="7475d-163">The RGB value of the text color for the header and footer in hexadecimal notation; for example, #rrggbb.</span></span>  <br/> |<span data-ttu-id="7475d-164">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="7475d-164">Values of the xsd:string type.</span></span>  <br/> |
   

