---
title: elemento de PP (Text_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5444543-fcd9-91cc-e7f8-cf860caa9fcc
description: Especifica el principio de las propiedades de un párrafo ejecutar. La ejecución se define al final del texto o hasta la siguiente etiqueta.
ms.openlocfilehash: bb2b0ab7a76c142b810ecd02dbc1b5ba7463520a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400108"
---
# <a name="pp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="a4dc3-104">elemento de PP (Text_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="a4dc3-104">pp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a4dc3-105">Especifica el principio de las propiedades de un párrafo ejecutar.</span><span class="sxs-lookup"><span data-stu-id="a4dc3-105">Specifies the beginning of a paragraph properties run.</span></span> <span data-ttu-id="a4dc3-106">La ejecución se define al final del texto o hasta la siguiente etiqueta.</span><span class="sxs-lookup"><span data-stu-id="a4dc3-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a4dc3-107">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a4dc3-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a4dc3-108">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="a4dc3-108">**Element type**</span></span> <br/> |[<span data-ttu-id="a4dc3-109">pp_Type</span><span class="sxs-lookup"><span data-stu-id="a4dc3-109">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a4dc3-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a4dc3-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a4dc3-111">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a4dc3-111">**Schema file**</span></span> <br/> |<span data-ttu-id="a4dc3-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a4dc3-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a4dc3-113">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="a4dc3-113">**Document parts**</span></span> <br/> |<span data-ttu-id="a4dc3-114">página # .xml, master # .xml</span><span class="sxs-lookup"><span data-stu-id="a4dc3-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a4dc3-115">Definición</span><span class="sxs-lookup"><span data-stu-id="a4dc3-115">Definition</span></span>

```XML
< xs:element name="pp" type="pp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a4dc3-116">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="a4dc3-116">Elements and attributes</span></span>

<span data-ttu-id="a4dc3-117">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="a4dc3-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a4dc3-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a4dc3-118">Parent elements</span></span>

|<span data-ttu-id="a4dc3-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="a4dc3-119">**Element**</span></span>|<span data-ttu-id="a4dc3-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a4dc3-120">**Type**</span></span>|<span data-ttu-id="a4dc3-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a4dc3-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a4dc3-122">Text</span><span class="sxs-lookup"><span data-stu-id="a4dc3-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a4dc3-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="a4dc3-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a4dc3-124">Contiene el texto de una forma.</span><span class="sxs-lookup"><span data-stu-id="a4dc3-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a4dc3-125">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a4dc3-125">Child elements</span></span>

<span data-ttu-id="a4dc3-126">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a4dc3-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a4dc3-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="a4dc3-127">Attributes</span></span>

|<span data-ttu-id="a4dc3-128">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="a4dc3-128">**Attribute**</span></span>|<span data-ttu-id="a4dc3-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a4dc3-129">**Type**</span></span>|<span data-ttu-id="a4dc3-130">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="a4dc3-130">**Required**</span></span>|<span data-ttu-id="a4dc3-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a4dc3-131">**Description**</span></span>|<span data-ttu-id="a4dc3-132">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="a4dc3-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a4dc3-133">IX</span><span class="sxs-lookup"><span data-stu-id="a4dc3-133">IX</span></span>  <br/> |<span data-ttu-id="a4dc3-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a4dc3-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a4dc3-135">necesario</span><span class="sxs-lookup"><span data-stu-id="a4dc3-135">required</span></span>  <br/> |<span data-ttu-id="a4dc3-136">El índice del elemento **Para** que especifica el formato aplicado a esta ejecución.</span><span class="sxs-lookup"><span data-stu-id="a4dc3-136">The index of the **Para** element that specifies the formatting applied to this run.</span></span>  <br/> |<span data-ttu-id="a4dc3-137">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a4dc3-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

