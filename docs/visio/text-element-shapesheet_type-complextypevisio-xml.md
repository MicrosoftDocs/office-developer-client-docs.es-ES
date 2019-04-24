---
title: Elemento Text (ShapeSheet_Type complexType) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46211968-9ad8-07da-f725-3ad136b7a8a1
description: Contiene el texto de una forma.
ms.openlocfilehash: f2c809d7db895a3635a5898d83d4583cd38f1249
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332374"
---
# <a name="text-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="05ae0-103">Elemento Text (ShapeSheet_Type complexType) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="05ae0-103">Text element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="05ae0-104">Contiene el texto de una forma.</span><span class="sxs-lookup"><span data-stu-id="05ae0-104">Contains the text of a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="05ae0-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="05ae0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="05ae0-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="05ae0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="05ae0-107">Text_Type</span><span class="sxs-lookup"><span data-stu-id="05ae0-107">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="05ae0-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="05ae0-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="05ae0-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="05ae0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="05ae0-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="05ae0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="05ae0-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="05ae0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="05ae0-112">Página #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="05ae0-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="05ae0-113">Definición</span><span class="sxs-lookup"><span data-stu-id="05ae0-113">Definition</span></span>

```XML
< xs:element name="Text" type="Text_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="05ae0-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="05ae0-114">Elements and attributes</span></span>

<span data-ttu-id="05ae0-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="05ae0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="05ae0-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="05ae0-116">Parent elements</span></span>

|<span data-ttu-id="05ae0-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="05ae0-117">**Element**</span></span>|<span data-ttu-id="05ae0-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="05ae0-118">**Type**</span></span>|<span data-ttu-id="05ae0-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="05ae0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="05ae0-120">Shape</span><span class="sxs-lookup"><span data-stu-id="05ae0-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="05ae0-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="05ae0-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="05ae0-122">Contiene elementos que definen una forma en un elemento de forma de grupo, **página**o **patrón**.</span><span class="sxs-lookup"><span data-stu-id="05ae0-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="05ae0-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="05ae0-123">Child elements</span></span>

|<span data-ttu-id="05ae0-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="05ae0-124">**Element**</span></span>|<span data-ttu-id="05ae0-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="05ae0-125">**Type**</span></span>|<span data-ttu-id="05ae0-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="05ae0-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="05ae0-127">cruzada</span><span class="sxs-lookup"><span data-stu-id="05ae0-127">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="05ae0-128">cp_Type</span><span class="sxs-lookup"><span data-stu-id="05ae0-128">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="05ae0-129">Marca el principio de una ejecución de propiedades de carácter que tiene un formato conforme al elemento char correspondiente.</span><span class="sxs-lookup"><span data-stu-id="05ae0-129">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span>  <br/> |
|[<span data-ttu-id="05ae0-130">FLD</span><span class="sxs-lookup"><span data-stu-id="05ae0-130">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="05ae0-131">fld_Type</span><span class="sxs-lookup"><span data-stu-id="05ae0-131">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="05ae0-132">Indica un punto de inserción de campo de texto para el elemento Field correspondiente.</span><span class="sxs-lookup"><span data-stu-id="05ae0-132">Indicates a text-field insertion point for the corresponding Field element.</span></span>  <br/> |
|[<span data-ttu-id="05ae0-133">VP</span><span class="sxs-lookup"><span data-stu-id="05ae0-133">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="05ae0-134">pp_Type</span><span class="sxs-lookup"><span data-stu-id="05ae0-134">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="05ae0-135">Especifica el principio de un párrafo ejecutar propiedades.</span><span class="sxs-lookup"><span data-stu-id="05ae0-135">Specifies the beginning of a paragraph properties run.</span></span>  <br/> |
|[<span data-ttu-id="05ae0-136">PAM</span><span class="sxs-lookup"><span data-stu-id="05ae0-136">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="05ae0-137">tp_Type</span><span class="sxs-lookup"><span data-stu-id="05ae0-137">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="05ae0-138">Especifica el principio de una ejecución de propiedades de tabulaciones.</span><span class="sxs-lookup"><span data-stu-id="05ae0-138">Specifies the beginning of a tabs properties run.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="05ae0-139">Atributos</span><span class="sxs-lookup"><span data-stu-id="05ae0-139">Attributes</span></span>

<span data-ttu-id="05ae0-140">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="05ae0-140">None.</span></span>
  

