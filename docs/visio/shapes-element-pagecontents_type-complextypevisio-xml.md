---
title: Elemento Shapes (PageContents_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f9d51d7-e2b7-bc68-dede-c79fb9dbcf60
description: Contiene una colección de elementos Shape.
ms.openlocfilehash: 5d248dd2683a1ccc153d15477c888e1b13d24d0f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542124"
---
# <a name="shapes-element-pagecontents_type-complextype-visio-xml"></a><span data-ttu-id="2a0c0-103">Elemento Shapes (PageContents_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="2a0c0-103">Shapes element (PageContents_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="2a0c0-104">Contiene una colección de elementos Shape.</span><span class="sxs-lookup"><span data-stu-id="2a0c0-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2a0c0-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2a0c0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a0c0-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="2a0c0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2a0c0-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="2a0c0-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2a0c0-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2a0c0-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2a0c0-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2a0c0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2a0c0-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="2a0c0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2a0c0-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="2a0c0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="2a0c0-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="2a0c0-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2a0c0-113">Definición</span><span class="sxs-lookup"><span data-stu-id="2a0c0-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2a0c0-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="2a0c0-114">Elements and attributes</span></span>

<span data-ttu-id="2a0c0-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="2a0c0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2a0c0-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2a0c0-116">Parent elements</span></span>

|<span data-ttu-id="2a0c0-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2a0c0-117">**Element**</span></span>|<span data-ttu-id="2a0c0-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2a0c0-118">**Type**</span></span>|<span data-ttu-id="2a0c0-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2a0c0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2a0c0-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="2a0c0-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="2a0c0-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="2a0c0-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2a0c0-122">Especifica información sobre las formas de un patrón en un dibujo web.</span><span class="sxs-lookup"><span data-stu-id="2a0c0-122">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
|[<span data-ttu-id="2a0c0-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="2a0c0-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="2a0c0-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="2a0c0-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2a0c0-125">Especifica información sobre las formas de un patrón en un dibujo web.</span><span class="sxs-lookup"><span data-stu-id="2a0c0-125">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2a0c0-126">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2a0c0-126">Child elements</span></span>

|<span data-ttu-id="2a0c0-127">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2a0c0-127">**Element**</span></span>|<span data-ttu-id="2a0c0-128">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2a0c0-128">**Type**</span></span>|<span data-ttu-id="2a0c0-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2a0c0-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2a0c0-130">Shape</span><span class="sxs-lookup"><span data-stu-id="2a0c0-130">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2a0c0-131">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="2a0c0-131">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2a0c0-132">Contiene elementos que definen una forma en un **elemento Master**, **Page** o forma de grupo.</span><span class="sxs-lookup"><span data-stu-id="2a0c0-132">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="2a0c0-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="2a0c0-133">Attributes</span></span>

<span data-ttu-id="2a0c0-134">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2a0c0-134">None.</span></span>
  

