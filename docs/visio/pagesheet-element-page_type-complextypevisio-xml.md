---
title: Elemento PageSheet (Page_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 99a6549b-099b-1546-cc30-db0010fe3ce1
description: Especifica las propiedades de la página de dibujo asociada con la página de dibujo.
ms.openlocfilehash: ef926af0238b1a44bbaa5c2eae9c0f7c90dc0c08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822722"
---
# <a name="pagesheet-element-pagetype-complextype-visio-xml"></a><span data-ttu-id="86ee3-103">Elemento PageSheet (Page_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="86ee3-103">PageSheet element (Page_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="86ee3-104">Especifica las propiedades de la página de dibujo asociada con la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="86ee3-104">Specifies the properties of the drawing page associated with the drawing page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="86ee3-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="86ee3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="86ee3-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="86ee3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="86ee3-107">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="86ee3-107">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="86ee3-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="86ee3-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="86ee3-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="86ee3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="86ee3-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="86ee3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="86ee3-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="86ee3-111">**Document parts**</span></span> <br/> |<span data-ttu-id="86ee3-112">Pages.Xml</span><span class="sxs-lookup"><span data-stu-id="86ee3-112">pages.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="86ee3-113">Definición</span><span class="sxs-lookup"><span data-stu-id="86ee3-113">Definition</span></span>

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element > 
```

## <a name="elements-and-attributes"></a><span data-ttu-id="86ee3-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="86ee3-114">Elements and attributes</span></span>

<span data-ttu-id="86ee3-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="86ee3-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="86ee3-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="86ee3-116">Parent elements</span></span>

|<span data-ttu-id="86ee3-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="86ee3-117">**Element**</span></span>|<span data-ttu-id="86ee3-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="86ee3-118">**Type**</span></span>|<span data-ttu-id="86ee3-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="86ee3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="86ee3-120">Page</span><span class="sxs-lookup"><span data-stu-id="86ee3-120">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="86ee3-121">Page_Type</span><span class="sxs-lookup"><span data-stu-id="86ee3-121">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="86ee3-122">Contiene elementos que definen una página del documento.</span><span class="sxs-lookup"><span data-stu-id="86ee3-122">Contains elements that define a page in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="86ee3-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="86ee3-123">Child elements</span></span>

<span data-ttu-id="86ee3-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="86ee3-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="86ee3-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="86ee3-125">Attributes</span></span>

|<span data-ttu-id="86ee3-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="86ee3-126">**Attribute**</span></span>|<span data-ttu-id="86ee3-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="86ee3-127">**Type**</span></span>|<span data-ttu-id="86ee3-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="86ee3-128">**Required**</span></span>|<span data-ttu-id="86ee3-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="86ee3-129">**Description**</span></span>|<span data-ttu-id="86ee3-130">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="86ee3-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="86ee3-131">FillStyle</span><span class="sxs-lookup"><span data-stu-id="86ee3-131">FillStyle</span></span>  <br/> |<span data-ttu-id="86ee3-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="86ee3-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="86ee3-133">opcional</span><span class="sxs-lookup"><span data-stu-id="86ee3-133">optional</span></span>  <br/> |<span data-ttu-id="86ee3-134">Especifica el identificador de la hoja de estilos desde la que se heredan de formato de relleno.</span><span class="sxs-lookup"><span data-stu-id="86ee3-134">Specifies the ID of the style sheet from which to inherit fill formatting.</span></span> <span data-ttu-id="86ee3-135">DEBE ser el valor del atributo **ID** asociado con un **StyleSheet_Type** en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="86ee3-135">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="86ee3-136">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="86ee3-136">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="86ee3-137">LineStyle</span><span class="sxs-lookup"><span data-stu-id="86ee3-137">LineStyle</span></span>  <br/> |<span data-ttu-id="86ee3-138">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="86ee3-138">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="86ee3-139">opcional</span><span class="sxs-lookup"><span data-stu-id="86ee3-139">optional</span></span>  <br/> |<span data-ttu-id="86ee3-140">Especifica el identificador de la hoja de estilos desde la que se heredan de formato de línea.</span><span class="sxs-lookup"><span data-stu-id="86ee3-140">Specifies the ID of the style sheet from which to inherit line formatting.</span></span> <span data-ttu-id="86ee3-141">DEBE ser el valor del atributo **ID** asociado con un **StyleSheet_Type** en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="86ee3-141">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="86ee3-142">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="86ee3-142">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="86ee3-143">TextStyle</span><span class="sxs-lookup"><span data-stu-id="86ee3-143">TextStyle</span></span>  <br/> |<span data-ttu-id="86ee3-144">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="86ee3-144">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="86ee3-145">opcional</span><span class="sxs-lookup"><span data-stu-id="86ee3-145">optional</span></span>  <br/> |<span data-ttu-id="86ee3-146">Especifica el identificador de la hoja de estilos desde la que se heredan de formato de texto.</span><span class="sxs-lookup"><span data-stu-id="86ee3-146">Specifies the ID of the style sheet from which to inherit text formatting.</span></span> <span data-ttu-id="86ee3-147">DEBE ser el valor del atributo **ID** asociado con un **StyleSheet_Type** en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="86ee3-147">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="86ee3-148">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="86ee3-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="86ee3-149">UniqueID</span><span class="sxs-lookup"><span data-stu-id="86ee3-149">UniqueID</span></span>  <br/> |<span data-ttu-id="86ee3-150">xsd: String</span><span class="sxs-lookup"><span data-stu-id="86ee3-150">xsd:string</span></span>  <br/> |<span data-ttu-id="86ee3-151">opcional</span><span class="sxs-lookup"><span data-stu-id="86ee3-151">optional</span></span>  <br/> |<span data-ttu-id="86ee3-152">Identificador único del elemento dentro de su elemento primario.</span><span class="sxs-lookup"><span data-stu-id="86ee3-152">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="86ee3-153">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="86ee3-153">Values of the xsd:string type.</span></span>  <br/> |
   

