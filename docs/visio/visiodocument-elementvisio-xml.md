---
title: Elemento VisioDocument ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5954685-3a2d-7848-388f-5dd7e536551c
description: El elemento raíz de un documento de Microsoft Visio.
ms.openlocfilehash: 5a325b78ec64708246f0c8a6f5396c2ce1569121
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823541"
---
# <a name="visiodocument-element-visio-xml"></a><span data-ttu-id="75851-103">Elemento VisioDocument ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="75851-103">VisioDocument element ('Visio XML')</span></span>

<span data-ttu-id="75851-104">El elemento raíz de un documento de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="75851-104">The root element of a Microsoft Visio document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="75851-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="75851-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="75851-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="75851-106">**Element type**</span></span> <br/> |[<span data-ttu-id="75851-107">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="75851-107">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="75851-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="75851-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="75851-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="75851-109">**Schema file**</span></span> <br/> |<span data-ttu-id="75851-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="75851-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="75851-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="75851-111">**Document parts**</span></span> <br/> |<span data-ttu-id="75851-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="75851-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="75851-113">Definición</span><span class="sxs-lookup"><span data-stu-id="75851-113">Definition</span></span>

```XML
< xs:element name="VisioDocument" type="VisioDocument_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="75851-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="75851-114">Elements and attributes</span></span>

<span data-ttu-id="75851-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="75851-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="75851-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="75851-116">Parent elements</span></span>

<span data-ttu-id="75851-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="75851-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="75851-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="75851-118">Child elements</span></span>

|<span data-ttu-id="75851-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="75851-119">**Element**</span></span>|<span data-ttu-id="75851-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="75851-120">**Type**</span></span>|<span data-ttu-id="75851-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="75851-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="75851-122">Colores</span><span class="sxs-lookup"><span data-stu-id="75851-122">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="75851-123">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="75851-123">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="75851-124">Contiene la tabla de colores del documento.</span><span class="sxs-lookup"><span data-stu-id="75851-124">Contains the document's color table.</span></span>  <br/> |
|[<span data-ttu-id="75851-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="75851-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="75851-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="75851-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="75851-127">Contiene elementos que especifican la configuración de documentos.</span><span class="sxs-lookup"><span data-stu-id="75851-127">Contains elements that specify document settings.</span></span>  <br/> |
|[<span data-ttu-id="75851-128">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="75851-128">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="75851-129">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="75851-129">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="75851-130">Especifica la estructura de **ShapeSheet** de un documento.</span><span class="sxs-lookup"><span data-stu-id="75851-130">Specifies a document's **ShapeSheet** structure.</span></span>  <br/> |
|[<span data-ttu-id="75851-131">EventList</span><span class="sxs-lookup"><span data-stu-id="75851-131">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="75851-132">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="75851-132">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="75851-133">Contiene un elemento **EventItem** para cada evento al que debe responder un objeto.</span><span class="sxs-lookup"><span data-stu-id="75851-133">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
|[<span data-ttu-id="75851-134">FaceNames</span><span class="sxs-lookup"><span data-stu-id="75851-134">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="75851-135">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="75851-135">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="75851-136">Contiene una colección de elementos de **nombre de fuente** .</span><span class="sxs-lookup"><span data-stu-id="75851-136">Contains a collection of **FaceName** elements.</span></span>  <br/> |
|[<span data-ttu-id="75851-137">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="75851-137">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="75851-138">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="75851-138">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="75851-139">Contiene elementos de encabezado y pie de página de un documento.</span><span class="sxs-lookup"><span data-stu-id="75851-139">Contains elements for a document's header and footer.</span></span>  <br/> |
|[<span data-ttu-id="75851-140">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="75851-140">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="75851-141">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="75851-141">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="75851-142">Especifica el conjunto de páginas que son visibles y establecer de conjuntos de registros son actualizables en un dibujo de dibujo.</span><span class="sxs-lookup"><span data-stu-id="75851-142">Specifies the set of drawing pages that are viewable and set of recordsets that are refreshable in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="75851-143">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="75851-143">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="75851-144">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="75851-144">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="75851-145">Contiene una colección de elementos de la hoja de estilos para el documento.</span><span class="sxs-lookup"><span data-stu-id="75851-145">Contains a collection of StyleSheet elements for the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="75851-146">Atributos</span><span class="sxs-lookup"><span data-stu-id="75851-146">Attributes</span></span>

<span data-ttu-id="75851-147">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="75851-147">None.</span></span>
  

