---
title: Elemento VisioDocument (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5954685-3a2d-7848-388f-5dd7e536551c
description: El elemento raíz de un documento de Microsoft Visio.
ms.openlocfilehash: 9829fa8960d78777e0fff4306b96978da90a647d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285316"
---
# <a name="visiodocument-element-visio-xml"></a><span data-ttu-id="35d3c-103">Elemento VisioDocument (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="35d3c-103">VisioDocument element ('Visio XML')</span></span>

<span data-ttu-id="35d3c-104">El elemento raíz de un documento de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="35d3c-104">The root element of a Microsoft Visio document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="35d3c-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="35d3c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="35d3c-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="35d3c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="35d3c-107">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="35d3c-107">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="35d3c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="35d3c-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="35d3c-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="35d3c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="35d3c-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="35d3c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="35d3c-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="35d3c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="35d3c-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="35d3c-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="35d3c-113">Definición</span><span class="sxs-lookup"><span data-stu-id="35d3c-113">Definition</span></span>

```XML
< xs:element name="VisioDocument" type="VisioDocument_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="35d3c-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="35d3c-114">Elements and attributes</span></span>

<span data-ttu-id="35d3c-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="35d3c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="35d3c-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="35d3c-116">Parent elements</span></span>

<span data-ttu-id="35d3c-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="35d3c-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="35d3c-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="35d3c-118">Child elements</span></span>

|<span data-ttu-id="35d3c-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="35d3c-119">**Element**</span></span>|<span data-ttu-id="35d3c-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="35d3c-120">**Type**</span></span>|<span data-ttu-id="35d3c-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="35d3c-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="35d3c-122">Colors</span><span class="sxs-lookup"><span data-stu-id="35d3c-122">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="35d3c-123">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="35d3c-123">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="35d3c-124">Contiene la tabla de colores del documento.</span><span class="sxs-lookup"><span data-stu-id="35d3c-124">Contains the document's color table.</span></span>  <br/> |
|[<span data-ttu-id="35d3c-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="35d3c-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="35d3c-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="35d3c-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="35d3c-127">Contiene los elementos que especifican la configuración del documento.</span><span class="sxs-lookup"><span data-stu-id="35d3c-127">Contains elements that specify document settings.</span></span>  <br/> |
|[<span data-ttu-id="35d3c-128">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="35d3c-128">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="35d3c-129">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="35d3c-129">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="35d3c-130">Especifica la estructura de **ShapeSheet** de un documento.</span><span class="sxs-lookup"><span data-stu-id="35d3c-130">Specifies a document's **ShapeSheet** structure.</span></span>  <br/> |
|[<span data-ttu-id="35d3c-131">EventList</span><span class="sxs-lookup"><span data-stu-id="35d3c-131">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="35d3c-132">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="35d3c-132">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="35d3c-133">Contiene un elemento **EventItem** por cada evento al que debe responder un objeto.</span><span class="sxs-lookup"><span data-stu-id="35d3c-133">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
|[<span data-ttu-id="35d3c-134">FaceNames</span><span class="sxs-lookup"><span data-stu-id="35d3c-134">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="35d3c-135">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="35d3c-135">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="35d3c-136">Contiene una colección de elementos **FaceName** .</span><span class="sxs-lookup"><span data-stu-id="35d3c-136">Contains a collection of **FaceName** elements.</span></span>  <br/> |
|[<span data-ttu-id="35d3c-137">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="35d3c-137">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="35d3c-138">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="35d3c-138">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="35d3c-139">Contiene los elementos del encabezado y pie de página de un documento.</span><span class="sxs-lookup"><span data-stu-id="35d3c-139">Contains elements for a document's header and footer.</span></span>  <br/> |
|[<span data-ttu-id="35d3c-140">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="35d3c-140">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="35d3c-141">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="35d3c-141">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="35d3c-142">Especifica el conjunto de páginas de dibujo visibles y de un conjunto de conjuntos de registros que se pueden actualizar en un dibujo.</span><span class="sxs-lookup"><span data-stu-id="35d3c-142">Specifies the set of drawing pages that are viewable and set of recordsets that are refreshable in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="35d3c-143">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="35d3c-143">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="35d3c-144">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="35d3c-144">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="35d3c-145">Contiene una colección de elementos StyleSheet para el documento.</span><span class="sxs-lookup"><span data-stu-id="35d3c-145">Contains a collection of StyleSheet elements for the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="35d3c-146">Atributos</span><span class="sxs-lookup"><span data-stu-id="35d3c-146">Attributes</span></span>

<span data-ttu-id="35d3c-147">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="35d3c-147">None.</span></span>
  

