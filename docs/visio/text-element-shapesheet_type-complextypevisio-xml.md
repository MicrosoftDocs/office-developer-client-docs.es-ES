---
title: Elemento de texto (ShapeSheet_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46211968-9ad8-07da-f725-3ad136b7a8a1
description: Contiene el texto de una forma.
ms.openlocfilehash: 636f349b0a93719cd157db563b238147af5584cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823367"
---
# <a name="text-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="66681-103">Elemento de texto (ShapeSheet_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="66681-103">Text element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="66681-104">Contiene el texto de una forma.</span><span class="sxs-lookup"><span data-stu-id="66681-104">Contains the text of a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="66681-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="66681-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66681-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="66681-106">**Element type**</span></span> <br/> |[<span data-ttu-id="66681-107">Text_Type</span><span class="sxs-lookup"><span data-stu-id="66681-107">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="66681-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="66681-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="66681-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="66681-109">**Schema file**</span></span> <br/> |<span data-ttu-id="66681-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="66681-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="66681-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="66681-111">**Document parts**</span></span> <br/> |<span data-ttu-id="66681-112">página # .xml, master # .xml</span><span class="sxs-lookup"><span data-stu-id="66681-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="66681-113">Definición</span><span class="sxs-lookup"><span data-stu-id="66681-113">Definition</span></span>

```XML
< xs:element name="Text" type="Text_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="66681-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="66681-114">Elements and attributes</span></span>

<span data-ttu-id="66681-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="66681-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="66681-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="66681-116">Parent elements</span></span>

|<span data-ttu-id="66681-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="66681-117">**Element**</span></span>|<span data-ttu-id="66681-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="66681-118">**Type**</span></span>|<span data-ttu-id="66681-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="66681-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="66681-120">Shape</span><span class="sxs-lookup"><span data-stu-id="66681-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="66681-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="66681-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="66681-122">Contiene elementos que definen una forma en un **patrón**, una **página**o un elemento de la forma de grupo.</span><span class="sxs-lookup"><span data-stu-id="66681-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="66681-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="66681-123">Child elements</span></span>

|<span data-ttu-id="66681-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="66681-124">**Element**</span></span>|<span data-ttu-id="66681-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="66681-125">**Type**</span></span>|<span data-ttu-id="66681-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="66681-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="66681-127">CP</span><span class="sxs-lookup"><span data-stu-id="66681-127">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="66681-128">cp_Type</span><span class="sxs-lookup"><span data-stu-id="66681-128">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="66681-129">Marca el principio de un propiedades de carácter ejecutar es decir el formato de acuerdo con el correspondiente elemento de Char.</span><span class="sxs-lookup"><span data-stu-id="66681-129">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span>  <br/> |
|[<span data-ttu-id="66681-130">fld</span><span class="sxs-lookup"><span data-stu-id="66681-130">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="66681-131">fld_Type</span><span class="sxs-lookup"><span data-stu-id="66681-131">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="66681-132">Indica un punto de inserción de campos de texto para el elemento correspondiente del campo.</span><span class="sxs-lookup"><span data-stu-id="66681-132">Indicates a text-field insertion point for the corresponding Field element.</span></span>  <br/> |
|[<span data-ttu-id="66681-133">PP</span><span class="sxs-lookup"><span data-stu-id="66681-133">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="66681-134">pp_Type</span><span class="sxs-lookup"><span data-stu-id="66681-134">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="66681-135">Especifica el principio de las propiedades de un párrafo ejecutar.</span><span class="sxs-lookup"><span data-stu-id="66681-135">Specifies the beginning of a paragraph properties run.</span></span>  <br/> |
|[<span data-ttu-id="66681-136">TP</span><span class="sxs-lookup"><span data-stu-id="66681-136">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="66681-137">tp_Type</span><span class="sxs-lookup"><span data-stu-id="66681-137">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="66681-138">Especifica el comienzo de un ejecutar las propiedades de las fichas.</span><span class="sxs-lookup"><span data-stu-id="66681-138">Specifies the beginning of a tabs properties run.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="66681-139">Atributos</span><span class="sxs-lookup"><span data-stu-id="66681-139">Attributes</span></span>

<span data-ttu-id="66681-140">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="66681-140">None.</span></span>
  

