---
title: Elemento PageSheet (complexType Page_Type) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 99a6549b-099b-1546-cc30-db0010fe3ce1
description: Especifica las propiedades de la página de dibujo asociada a la página de dibujo.
ms.openlocfilehash: 2f49d152a0fcb30e3f5aea98cdc251d3b65b8f69
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540626"
---
# <a name="pagesheet-element-pagetype-complextype-visio-xml"></a><span data-ttu-id="1313e-103">Elemento PageSheet (complexType Page_Type) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="1313e-103">PageSheet element (Page_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="1313e-104">Especifica las propiedades de la página de dibujo asociada a la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="1313e-104">Specifies the properties of the drawing page associated with the drawing page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1313e-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1313e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1313e-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="1313e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1313e-107">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="1313e-107">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1313e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1313e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1313e-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1313e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1313e-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="1313e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1313e-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="1313e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1313e-112">Pages. XML</span><span class="sxs-lookup"><span data-stu-id="1313e-112">pages.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1313e-113">Definición</span><span class="sxs-lookup"><span data-stu-id="1313e-113">Definition</span></span>

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element > 
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1313e-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="1313e-114">Elements and attributes</span></span>

<span data-ttu-id="1313e-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="1313e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1313e-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1313e-116">Parent elements</span></span>

|<span data-ttu-id="1313e-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1313e-117">**Element**</span></span>|<span data-ttu-id="1313e-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1313e-118">**Type**</span></span>|<span data-ttu-id="1313e-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1313e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1313e-120">Page</span><span class="sxs-lookup"><span data-stu-id="1313e-120">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1313e-121">Page_Type</span><span class="sxs-lookup"><span data-stu-id="1313e-121">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1313e-122">Contiene los elementos que definen una página en el documento.</span><span class="sxs-lookup"><span data-stu-id="1313e-122">Contains elements that define a page in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1313e-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1313e-123">Child elements</span></span>

<span data-ttu-id="1313e-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1313e-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1313e-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="1313e-125">Attributes</span></span>

|<span data-ttu-id="1313e-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="1313e-126">**Attribute**</span></span>|<span data-ttu-id="1313e-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1313e-127">**Type**</span></span>|<span data-ttu-id="1313e-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="1313e-128">**Required**</span></span>|<span data-ttu-id="1313e-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1313e-129">**Description**</span></span>|<span data-ttu-id="1313e-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="1313e-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1313e-131">FillStyle</span><span class="sxs-lookup"><span data-stu-id="1313e-131">FillStyle</span></span>  <br/> |<span data-ttu-id="1313e-132">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1313e-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1313e-133">opcional</span><span class="sxs-lookup"><span data-stu-id="1313e-133">optional</span></span>  <br/> |<span data-ttu-id="1313e-134">Especifica el identificador de la hoja de estilos de la que se va a heredar el formato de relleno.</span><span class="sxs-lookup"><span data-stu-id="1313e-134">Specifies the ID of the style sheet from which to inherit fill formatting.</span></span> <span data-ttu-id="1313e-135">DEBE ser el valor del atributo **ID** asociado con un **StyleSheet_Type** en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="1313e-135">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="1313e-136">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1313e-136">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1313e-137">LineStyle</span><span class="sxs-lookup"><span data-stu-id="1313e-137">LineStyle</span></span>  <br/> |<span data-ttu-id="1313e-138">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1313e-138">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1313e-139">opcional</span><span class="sxs-lookup"><span data-stu-id="1313e-139">optional</span></span>  <br/> |<span data-ttu-id="1313e-140">Especifica el identificador de la hoja de estilos de la que se va a heredar el formato de línea.</span><span class="sxs-lookup"><span data-stu-id="1313e-140">Specifies the ID of the style sheet from which to inherit line formatting.</span></span> <span data-ttu-id="1313e-141">DEBE ser el valor del atributo **ID** asociado con un **StyleSheet_Type** en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="1313e-141">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="1313e-142">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1313e-142">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1313e-143">TextStyle</span><span class="sxs-lookup"><span data-stu-id="1313e-143">TextStyle</span></span>  <br/> |<span data-ttu-id="1313e-144">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1313e-144">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1313e-145">opcional</span><span class="sxs-lookup"><span data-stu-id="1313e-145">optional</span></span>  <br/> |<span data-ttu-id="1313e-146">Especifica el identificador de la hoja de estilos de la que se va a heredar el formato de texto.</span><span class="sxs-lookup"><span data-stu-id="1313e-146">Specifies the ID of the style sheet from which to inherit text formatting.</span></span> <span data-ttu-id="1313e-147">DEBE ser el valor del atributo **ID** asociado con un **StyleSheet_Type** en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="1313e-147">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="1313e-148">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1313e-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1313e-149">UniqueID</span><span class="sxs-lookup"><span data-stu-id="1313e-149">UniqueID</span></span>  <br/> |<span data-ttu-id="1313e-150">xsd: String</span><span class="sxs-lookup"><span data-stu-id="1313e-150">xsd:string</span></span>  <br/> |<span data-ttu-id="1313e-151">opcional</span><span class="sxs-lookup"><span data-stu-id="1313e-151">optional</span></span>  <br/> |<span data-ttu-id="1313e-152">IDENTIFICADOR único del elemento dentro de su elemento primario.</span><span class="sxs-lookup"><span data-stu-id="1313e-152">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="1313e-153">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="1313e-153">Values of the xsd:string type.</span></span>  <br/> |
   

