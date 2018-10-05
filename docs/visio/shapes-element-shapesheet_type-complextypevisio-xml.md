---
title: Elemento de formas (ShapeSheet_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 85aa7df3-d9bd-acb3-61b3-2bd5fa256435
description: Contiene una colección de elementos de la forma.
ms.openlocfilehash: d4de4436079ec6290b52dd74bf3ee015c5b0d3f5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392098"
---
# <a name="shapes-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="f7f6d-103">Elemento de formas (ShapeSheet_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="f7f6d-103">Shapes element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="f7f6d-104">Contiene una colección de elementos de la forma.</span><span class="sxs-lookup"><span data-stu-id="f7f6d-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f7f6d-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f7f6d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f7f6d-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="f7f6d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f7f6d-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="f7f6d-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f7f6d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f7f6d-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f7f6d-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f7f6d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f7f6d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f7f6d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f7f6d-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="f7f6d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f7f6d-112">página # .xml, master # .xml</span><span class="sxs-lookup"><span data-stu-id="f7f6d-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f7f6d-113">Definición</span><span class="sxs-lookup"><span data-stu-id="f7f6d-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f7f6d-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="f7f6d-114">Elements and attributes</span></span>

<span data-ttu-id="f7f6d-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="f7f6d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f7f6d-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f7f6d-116">Parent elements</span></span>

|<span data-ttu-id="f7f6d-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="f7f6d-117">**Element**</span></span>|<span data-ttu-id="f7f6d-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f7f6d-118">**Type**</span></span>|<span data-ttu-id="f7f6d-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f7f6d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f7f6d-120">Shape</span><span class="sxs-lookup"><span data-stu-id="f7f6d-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f7f6d-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="f7f6d-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f7f6d-122">Especifica una colección de las propiedades asociadas con una forma.</span><span class="sxs-lookup"><span data-stu-id="f7f6d-122">Specifies a collection of properties associated with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f7f6d-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f7f6d-123">Child elements</span></span>

|<span data-ttu-id="f7f6d-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="f7f6d-124">**Element**</span></span>|<span data-ttu-id="f7f6d-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f7f6d-125">**Type**</span></span>|<span data-ttu-id="f7f6d-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f7f6d-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f7f6d-127">Shape</span><span class="sxs-lookup"><span data-stu-id="f7f6d-127">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f7f6d-128">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="f7f6d-128">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f7f6d-129">Contiene elementos que definen una forma en un **patrón**, una **página**o un elemento de la forma de grupo.</span><span class="sxs-lookup"><span data-stu-id="f7f6d-129">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="f7f6d-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="f7f6d-130">Attributes</span></span>

<span data-ttu-id="f7f6d-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f7f6d-131">None.</span></span>
  

