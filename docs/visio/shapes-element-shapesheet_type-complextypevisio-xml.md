---
title: Elemento Shapes (complexType ShapeSheet_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 85aa7df3-d9bd-acb3-61b3-2bd5fa256435
description: Contiene una colección de elementos Shape.
ms.openlocfilehash: d4de4436079ec6290b52dd74bf3ee015c5b0d3f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348254"
---
# <a name="shapes-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="8fddc-103">Elemento Shapes (complexType ShapeSheet_Type) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="8fddc-103">Shapes element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="8fddc-104">Contiene una colección de elementos Shape.</span><span class="sxs-lookup"><span data-stu-id="8fddc-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8fddc-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8fddc-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8fddc-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="8fddc-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8fddc-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="8fddc-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8fddc-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8fddc-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8fddc-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="8fddc-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8fddc-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="8fddc-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8fddc-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="8fddc-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8fddc-112">Página #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="8fddc-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8fddc-113">Definición</span><span class="sxs-lookup"><span data-stu-id="8fddc-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8fddc-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="8fddc-114">Elements and attributes</span></span>

<span data-ttu-id="8fddc-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="8fddc-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8fddc-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8fddc-116">Parent elements</span></span>

|<span data-ttu-id="8fddc-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8fddc-117">**Element**</span></span>|<span data-ttu-id="8fddc-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8fddc-118">**Type**</span></span>|<span data-ttu-id="8fddc-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8fddc-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8fddc-120">Shape</span><span class="sxs-lookup"><span data-stu-id="8fddc-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8fddc-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="8fddc-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8fddc-122">Especifica una colección de propiedades asociadas con una forma.</span><span class="sxs-lookup"><span data-stu-id="8fddc-122">Specifies a collection of properties associated with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8fddc-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8fddc-123">Child elements</span></span>

|<span data-ttu-id="8fddc-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8fddc-124">**Element**</span></span>|<span data-ttu-id="8fddc-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8fddc-125">**Type**</span></span>|<span data-ttu-id="8fddc-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8fddc-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8fddc-127">Shape</span><span class="sxs-lookup"><span data-stu-id="8fddc-127">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8fddc-128">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="8fddc-128">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8fddc-129">Contiene elementos que definen una forma en un elemento de forma de grupo, **página**o **patrón**.</span><span class="sxs-lookup"><span data-stu-id="8fddc-129">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8fddc-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="8fddc-130">Attributes</span></span>

<span data-ttu-id="8fddc-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8fddc-131">None.</span></span>
  

