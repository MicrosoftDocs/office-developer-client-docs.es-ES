---
title: Elemento de formas (PageContents_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f9d51d7-e2b7-bc68-dede-c79fb9dbcf60
description: Contiene una colección de elementos de la forma.
ms.openlocfilehash: 7abece2a9fc8d88817f22c654567272becce981e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397572"
---
# <a name="shapes-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="5cd40-103">Elemento de formas (PageContents_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="5cd40-103">Shapes element (PageContents_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="5cd40-104">Contiene una colección de elementos de la forma.</span><span class="sxs-lookup"><span data-stu-id="5cd40-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5cd40-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5cd40-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5cd40-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="5cd40-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5cd40-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="5cd40-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5cd40-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5cd40-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5cd40-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="5cd40-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5cd40-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="5cd40-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5cd40-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="5cd40-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5cd40-112">página # .xml, master # .xml</span><span class="sxs-lookup"><span data-stu-id="5cd40-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5cd40-113">Definición</span><span class="sxs-lookup"><span data-stu-id="5cd40-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5cd40-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="5cd40-114">Elements and attributes</span></span>

<span data-ttu-id="5cd40-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="5cd40-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5cd40-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5cd40-116">Parent elements</span></span>

|<span data-ttu-id="5cd40-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="5cd40-117">**Element**</span></span>|<span data-ttu-id="5cd40-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5cd40-118">**Type**</span></span>|<span data-ttu-id="5cd40-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5cd40-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5cd40-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="5cd40-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="5cd40-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="5cd40-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5cd40-122">Especifica información acerca de las formas de un patrón en un dibujo Web.</span><span class="sxs-lookup"><span data-stu-id="5cd40-122">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
|[<span data-ttu-id="5cd40-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="5cd40-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="5cd40-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="5cd40-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5cd40-125">Especifica información acerca de las formas de un patrón en un dibujo Web.</span><span class="sxs-lookup"><span data-stu-id="5cd40-125">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5cd40-126">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5cd40-126">Child elements</span></span>

|<span data-ttu-id="5cd40-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="5cd40-127">**Element**</span></span>|<span data-ttu-id="5cd40-128">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5cd40-128">**Type**</span></span>|<span data-ttu-id="5cd40-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5cd40-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5cd40-130">Shape</span><span class="sxs-lookup"><span data-stu-id="5cd40-130">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5cd40-131">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="5cd40-131">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5cd40-132">Contiene elementos que definen una forma en un **patrón**, una **página**o un elemento de la forma de grupo.</span><span class="sxs-lookup"><span data-stu-id="5cd40-132">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="5cd40-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="5cd40-133">Attributes</span></span>

<span data-ttu-id="5cd40-134">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5cd40-134">None.</span></span>
  

