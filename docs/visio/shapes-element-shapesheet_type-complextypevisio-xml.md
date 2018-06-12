---
title: Elemento de formas (ShapeSheet_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 85aa7df3-d9bd-acb3-61b3-2bd5fa256435
description: Contiene una colección de elementos de la forma.
ms.openlocfilehash: d2e725a28873cac8dded49587a98400df1d9bf7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823181"
---
# <a name="shapes-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="710bf-103">Elemento de formas (ShapeSheet_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="710bf-103">Shapes element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="710bf-104">Contiene una colección de elementos de la forma.</span><span class="sxs-lookup"><span data-stu-id="710bf-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="710bf-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="710bf-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="710bf-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="710bf-106">**Element type**</span></span> <br/> |[<span data-ttu-id="710bf-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="710bf-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="710bf-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="710bf-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="710bf-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="710bf-109">**Schema file**</span></span> <br/> |<span data-ttu-id="710bf-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="710bf-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="710bf-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="710bf-111">**Document parts**</span></span> <br/> |<span data-ttu-id="710bf-112">página # .xml, master # .xml</span><span class="sxs-lookup"><span data-stu-id="710bf-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="710bf-113">Definición</span><span class="sxs-lookup"><span data-stu-id="710bf-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="710bf-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="710bf-114">Elements and attributes</span></span>

<span data-ttu-id="710bf-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="710bf-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="710bf-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="710bf-116">Parent elements</span></span>

|<span data-ttu-id="710bf-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="710bf-117">**Element**</span></span>|<span data-ttu-id="710bf-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="710bf-118">**Type**</span></span>|<span data-ttu-id="710bf-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="710bf-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="710bf-120">Shape</span><span class="sxs-lookup"><span data-stu-id="710bf-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="710bf-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="710bf-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="710bf-122">Especifica una colección de las propiedades asociadas con una forma.</span><span class="sxs-lookup"><span data-stu-id="710bf-122">Specifies a collection of properties associated with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="710bf-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="710bf-123">Child elements</span></span>

|<span data-ttu-id="710bf-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="710bf-124">**Element**</span></span>|<span data-ttu-id="710bf-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="710bf-125">**Type**</span></span>|<span data-ttu-id="710bf-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="710bf-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="710bf-127">Shape</span><span class="sxs-lookup"><span data-stu-id="710bf-127">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="710bf-128">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="710bf-128">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="710bf-129">Contiene elementos que definen una forma en un **patrón**, una **página**o un elemento de la forma de grupo.</span><span class="sxs-lookup"><span data-stu-id="710bf-129">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="710bf-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="710bf-130">Attributes</span></span>

<span data-ttu-id="710bf-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="710bf-131">None.</span></span>
  

