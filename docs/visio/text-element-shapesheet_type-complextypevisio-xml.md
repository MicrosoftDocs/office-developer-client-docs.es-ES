---
title: Elemento de texto (ShapeSheet_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46211968-9ad8-07da-f725-3ad136b7a8a1
description: Contiene el texto de una forma.
ms.openlocfilehash: f2c809d7db895a3635a5898d83d4583cd38f1249
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385917"
---
# <a name="text-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="05c53-103">Elemento de texto (ShapeSheet_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="05c53-103">Text element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="05c53-104">Contiene el texto de una forma.</span><span class="sxs-lookup"><span data-stu-id="05c53-104">Contains the text of a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="05c53-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="05c53-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="05c53-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="05c53-106">**Element type**</span></span> <br/> |[<span data-ttu-id="05c53-107">Text_Type</span><span class="sxs-lookup"><span data-stu-id="05c53-107">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="05c53-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="05c53-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="05c53-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="05c53-109">**Schema file**</span></span> <br/> |<span data-ttu-id="05c53-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="05c53-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="05c53-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="05c53-111">**Document parts**</span></span> <br/> |<span data-ttu-id="05c53-112">página # .xml, master # .xml</span><span class="sxs-lookup"><span data-stu-id="05c53-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="05c53-113">Definición</span><span class="sxs-lookup"><span data-stu-id="05c53-113">Definition</span></span>

```XML
< xs:element name="Text" type="Text_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="05c53-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="05c53-114">Elements and attributes</span></span>

<span data-ttu-id="05c53-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="05c53-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="05c53-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="05c53-116">Parent elements</span></span>

|<span data-ttu-id="05c53-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="05c53-117">**Element**</span></span>|<span data-ttu-id="05c53-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="05c53-118">**Type**</span></span>|<span data-ttu-id="05c53-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="05c53-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="05c53-120">Shape</span><span class="sxs-lookup"><span data-stu-id="05c53-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="05c53-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="05c53-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="05c53-122">Contiene elementos que definen una forma en un **patrón**, una **página**o un elemento de la forma de grupo.</span><span class="sxs-lookup"><span data-stu-id="05c53-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="05c53-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="05c53-123">Child elements</span></span>

|<span data-ttu-id="05c53-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="05c53-124">**Element**</span></span>|<span data-ttu-id="05c53-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="05c53-125">**Type**</span></span>|<span data-ttu-id="05c53-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="05c53-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="05c53-127">CP</span><span class="sxs-lookup"><span data-stu-id="05c53-127">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="05c53-128">cp_Type</span><span class="sxs-lookup"><span data-stu-id="05c53-128">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="05c53-129">Marca el principio de un propiedades de carácter ejecutar es decir el formato de acuerdo con el correspondiente elemento de Char.</span><span class="sxs-lookup"><span data-stu-id="05c53-129">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span>  <br/> |
|[<span data-ttu-id="05c53-130">fld</span><span class="sxs-lookup"><span data-stu-id="05c53-130">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="05c53-131">fld_Type</span><span class="sxs-lookup"><span data-stu-id="05c53-131">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="05c53-132">Indica un punto de inserción de campos de texto para el elemento correspondiente del campo.</span><span class="sxs-lookup"><span data-stu-id="05c53-132">Indicates a text-field insertion point for the corresponding Field element.</span></span>  <br/> |
|[<span data-ttu-id="05c53-133">PP</span><span class="sxs-lookup"><span data-stu-id="05c53-133">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="05c53-134">pp_Type</span><span class="sxs-lookup"><span data-stu-id="05c53-134">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="05c53-135">Especifica el principio de las propiedades de un párrafo ejecutar.</span><span class="sxs-lookup"><span data-stu-id="05c53-135">Specifies the beginning of a paragraph properties run.</span></span>  <br/> |
|[<span data-ttu-id="05c53-136">TP</span><span class="sxs-lookup"><span data-stu-id="05c53-136">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="05c53-137">tp_Type</span><span class="sxs-lookup"><span data-stu-id="05c53-137">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="05c53-138">Especifica el comienzo de un ejecutar las propiedades de las fichas.</span><span class="sxs-lookup"><span data-stu-id="05c53-138">Specifies the beginning of a tabs properties run.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="05c53-139">Atributos</span><span class="sxs-lookup"><span data-stu-id="05c53-139">Attributes</span></span>

<span data-ttu-id="05c53-140">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="05c53-140">None.</span></span>
  

