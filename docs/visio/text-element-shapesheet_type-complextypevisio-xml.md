---
title: Elemento Text (ShapeSheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46211968-9ad8-07da-f725-3ad136b7a8a1
description: Contiene el texto de una forma.
ms.openlocfilehash: 4b03bc2539b80e49daae9d14f3e2ad07a51de9f1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541928"
---
# <a name="text-element-shapesheet_type-complextype-visio-xml"></a><span data-ttu-id="e2499-103">Elemento Text (ShapeSheet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="e2499-103">Text element (ShapeSheet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="e2499-104">Contiene el texto de una forma.</span><span class="sxs-lookup"><span data-stu-id="e2499-104">Contains the text of a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e2499-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e2499-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e2499-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="e2499-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e2499-107">Text_Type</span><span class="sxs-lookup"><span data-stu-id="e2499-107">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e2499-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e2499-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e2499-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="e2499-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e2499-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e2499-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e2499-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="e2499-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e2499-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="e2499-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e2499-113">Definición</span><span class="sxs-lookup"><span data-stu-id="e2499-113">Definition</span></span>

```XML
< xs:element name="Text" type="Text_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e2499-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="e2499-114">Elements and attributes</span></span>

<span data-ttu-id="e2499-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="e2499-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e2499-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e2499-116">Parent elements</span></span>

|<span data-ttu-id="e2499-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e2499-117">**Element**</span></span>|<span data-ttu-id="e2499-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e2499-118">**Type**</span></span>|<span data-ttu-id="e2499-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e2499-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e2499-120">Shape</span><span class="sxs-lookup"><span data-stu-id="e2499-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e2499-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="e2499-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e2499-122">Contiene elementos que definen una forma en un **elemento Master**, **Page** o forma de grupo.</span><span class="sxs-lookup"><span data-stu-id="e2499-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e2499-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e2499-123">Child elements</span></span>

|<span data-ttu-id="e2499-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e2499-124">**Element**</span></span>|<span data-ttu-id="e2499-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e2499-125">**Type**</span></span>|<span data-ttu-id="e2499-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e2499-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e2499-127">cp</span><span class="sxs-lookup"><span data-stu-id="e2499-127">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e2499-128">cp_Type</span><span class="sxs-lookup"><span data-stu-id="e2499-128">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e2499-129">Marca el principio de una ejecución de propiedades de carácter con formato según el elemento Char correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e2499-129">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span>  <br/> |
|[<span data-ttu-id="e2499-130">fld</span><span class="sxs-lookup"><span data-stu-id="e2499-130">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e2499-131">fld_Type</span><span class="sxs-lookup"><span data-stu-id="e2499-131">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e2499-132">Indica un punto de inserción de campo de texto para el elemento Field correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e2499-132">Indicates a text-field insertion point for the corresponding Field element.</span></span>  <br/> |
|[<span data-ttu-id="e2499-133">pp</span><span class="sxs-lookup"><span data-stu-id="e2499-133">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e2499-134">pp_Type</span><span class="sxs-lookup"><span data-stu-id="e2499-134">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e2499-135">Especifica el principio de una ejecución de propiedades de párrafo.</span><span class="sxs-lookup"><span data-stu-id="e2499-135">Specifies the beginning of a paragraph properties run.</span></span>  <br/> |
|[<span data-ttu-id="e2499-136">tp</span><span class="sxs-lookup"><span data-stu-id="e2499-136">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e2499-137">tp_Type</span><span class="sxs-lookup"><span data-stu-id="e2499-137">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e2499-138">Especifica el principio de la ejecución de las propiedades de las pestañas.</span><span class="sxs-lookup"><span data-stu-id="e2499-138">Specifies the beginning of a tabs properties run.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e2499-139">Atributos</span><span class="sxs-lookup"><span data-stu-id="e2499-139">Attributes</span></span>

<span data-ttu-id="e2499-140">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e2499-140">None.</span></span>
  

