---
title: Elemento PageSheet (complexType Page_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 99a6549b-099b-1546-cc30-db0010fe3ce1
description: Especifica las propiedades de la página de dibujo asociada a la página de dibujo.
ms.openlocfilehash: 8b60795c02717e4b752c09af19fa932f87924d1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326120"
---
# <a name="pagesheet-element-pagetype-complextype-visio-xml"></a><span data-ttu-id="cf566-103">Elemento PageSheet (complexType Page_Type) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="cf566-103">PageSheet element (Page_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="cf566-104">Especifica las propiedades de la página de dibujo asociada a la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="cf566-104">Specifies the properties of the drawing page associated with the drawing page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cf566-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cf566-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cf566-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="cf566-106">**Element type**</span></span> <br/> |[<span data-ttu-id="cf566-107">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="cf566-107">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="cf566-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cf566-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="cf566-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="cf566-109">**Schema file**</span></span> <br/> |<span data-ttu-id="cf566-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="cf566-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="cf566-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="cf566-111">**Document parts**</span></span> <br/> |<span data-ttu-id="cf566-112">Pages. XML</span><span class="sxs-lookup"><span data-stu-id="cf566-112">pages.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cf566-113">Definición</span><span class="sxs-lookup"><span data-stu-id="cf566-113">Definition</span></span>

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element > 
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cf566-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="cf566-114">Elements and attributes</span></span>

<span data-ttu-id="cf566-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="cf566-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="cf566-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cf566-116">Parent elements</span></span>

|<span data-ttu-id="cf566-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cf566-117">**Element**</span></span>|<span data-ttu-id="cf566-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cf566-118">**Type**</span></span>|<span data-ttu-id="cf566-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cf566-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cf566-120">Page</span><span class="sxs-lookup"><span data-stu-id="cf566-120">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cf566-121">Page_Type</span><span class="sxs-lookup"><span data-stu-id="cf566-121">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cf566-122">Contiene los elementos que definen una página en el documento.</span><span class="sxs-lookup"><span data-stu-id="cf566-122">Contains elements that define a page in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cf566-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cf566-123">Child elements</span></span>

<span data-ttu-id="cf566-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cf566-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cf566-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="cf566-125">Attributes</span></span>

|<span data-ttu-id="cf566-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="cf566-126">**Attribute**</span></span>|<span data-ttu-id="cf566-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cf566-127">**Type**</span></span>|<span data-ttu-id="cf566-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="cf566-128">**Required**</span></span>|<span data-ttu-id="cf566-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cf566-129">**Description**</span></span>|<span data-ttu-id="cf566-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="cf566-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cf566-131">FillStyle</span><span class="sxs-lookup"><span data-stu-id="cf566-131">FillStyle</span></span>  <br/> |<span data-ttu-id="cf566-132">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cf566-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cf566-133">opcional</span><span class="sxs-lookup"><span data-stu-id="cf566-133">optional</span></span>  <br/> |<span data-ttu-id="cf566-134">Especifica el identificador de la hoja de estilos de la que se va a heredar el formato de relleno.</span><span class="sxs-lookup"><span data-stu-id="cf566-134">Specifies the ID of the style sheet from which to inherit fill formatting.</span></span> <span data-ttu-id="cf566-135">DEBE ser el valor del atributo **ID** asociado con un **StyleSheet_Type** en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="cf566-135">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="cf566-136">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cf566-136">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cf566-137">LineStyle</span><span class="sxs-lookup"><span data-stu-id="cf566-137">LineStyle</span></span>  <br/> |<span data-ttu-id="cf566-138">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cf566-138">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cf566-139">opcional</span><span class="sxs-lookup"><span data-stu-id="cf566-139">optional</span></span>  <br/> |<span data-ttu-id="cf566-140">Especifica el identificador de la hoja de estilos de la que se va a heredar el formato de línea.</span><span class="sxs-lookup"><span data-stu-id="cf566-140">Specifies the ID of the style sheet from which to inherit line formatting.</span></span> <span data-ttu-id="cf566-141">DEBE ser el valor del atributo **ID** asociado con un **StyleSheet_Type** en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="cf566-141">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="cf566-142">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cf566-142">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cf566-143">TextStyle</span><span class="sxs-lookup"><span data-stu-id="cf566-143">TextStyle</span></span>  <br/> |<span data-ttu-id="cf566-144">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cf566-144">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cf566-145">opcional</span><span class="sxs-lookup"><span data-stu-id="cf566-145">optional</span></span>  <br/> |<span data-ttu-id="cf566-146">Especifica el identificador de la hoja de estilos de la que se va a heredar el formato de texto.</span><span class="sxs-lookup"><span data-stu-id="cf566-146">Specifies the ID of the style sheet from which to inherit text formatting.</span></span> <span data-ttu-id="cf566-147">DEBE ser el valor del atributo **ID** asociado con un **StyleSheet_Type** en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="cf566-147">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="cf566-148">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cf566-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cf566-149">UniqueID</span><span class="sxs-lookup"><span data-stu-id="cf566-149">UniqueID</span></span>  <br/> |<span data-ttu-id="cf566-150">xsd: String</span><span class="sxs-lookup"><span data-stu-id="cf566-150">xsd:string</span></span>  <br/> |<span data-ttu-id="cf566-151">opcional</span><span class="sxs-lookup"><span data-stu-id="cf566-151">optional</span></span>  <br/> |<span data-ttu-id="cf566-152">IDENTIFICADOR único del elemento dentro de su elemento primario.</span><span class="sxs-lookup"><span data-stu-id="cf566-152">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="cf566-153">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="cf566-153">Values of the xsd:string type.</span></span>  <br/> |
   

