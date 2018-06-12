---
title: Elemento de formas (PageContents_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f9d51d7-e2b7-bc68-dede-c79fb9dbcf60
description: Contiene una colección de elementos de la forma.
ms.openlocfilehash: eae86d230c19f1db8c7ed43cca8682460c3f7af1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823176"
---
# <a name="shapes-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="9393c-103">Elemento de formas (PageContents_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="9393c-103">Shapes element (PageContents_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="9393c-104">Contiene una colección de elementos de la forma.</span><span class="sxs-lookup"><span data-stu-id="9393c-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9393c-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9393c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9393c-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="9393c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9393c-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="9393c-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9393c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9393c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9393c-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9393c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9393c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9393c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9393c-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="9393c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9393c-112">página # .xml, master # .xml</span><span class="sxs-lookup"><span data-stu-id="9393c-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9393c-113">Definición</span><span class="sxs-lookup"><span data-stu-id="9393c-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9393c-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="9393c-114">Elements and attributes</span></span>

<span data-ttu-id="9393c-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="9393c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9393c-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9393c-116">Parent elements</span></span>

|<span data-ttu-id="9393c-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="9393c-117">**Element**</span></span>|<span data-ttu-id="9393c-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9393c-118">**Type**</span></span>|<span data-ttu-id="9393c-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9393c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9393c-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="9393c-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="9393c-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="9393c-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9393c-122">Especifica información acerca de las formas de un patrón en un dibujo Web.</span><span class="sxs-lookup"><span data-stu-id="9393c-122">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
|[<span data-ttu-id="9393c-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="9393c-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="9393c-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="9393c-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9393c-125">Especifica información acerca de las formas de un patrón en un dibujo Web.</span><span class="sxs-lookup"><span data-stu-id="9393c-125">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9393c-126">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9393c-126">Child elements</span></span>

|<span data-ttu-id="9393c-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="9393c-127">**Element**</span></span>|<span data-ttu-id="9393c-128">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9393c-128">**Type**</span></span>|<span data-ttu-id="9393c-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9393c-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9393c-130">Shape</span><span class="sxs-lookup"><span data-stu-id="9393c-130">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9393c-131">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="9393c-131">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9393c-132">Contiene elementos que definen una forma en un **patrón**, una **página**o un elemento de la forma de grupo.</span><span class="sxs-lookup"><span data-stu-id="9393c-132">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9393c-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="9393c-133">Attributes</span></span>

<span data-ttu-id="9393c-134">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9393c-134">None.</span></span>
  

