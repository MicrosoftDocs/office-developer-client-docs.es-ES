---
title: elemento PP (Text_Type complexType) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5444543-fcd9-91cc-e7f8-cf860caa9fcc
description: Especifica el principio de un párrafo ejecutar propiedades. La ejecución se define hasta el final del texto o hasta la siguiente etiqueta.
ms.openlocfilehash: bb2b0ab7a76c142b810ecd02dbc1b5ba7463520a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356080"
---
# <a name="pp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="2bc79-104">elemento PP (Text_Type complexType) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="2bc79-104">pp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="2bc79-105">Especifica el principio de un párrafo ejecutar propiedades.</span><span class="sxs-lookup"><span data-stu-id="2bc79-105">Specifies the beginning of a paragraph properties run.</span></span> <span data-ttu-id="2bc79-106">La ejecución se define hasta el final del texto o hasta la siguiente etiqueta.</span><span class="sxs-lookup"><span data-stu-id="2bc79-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2bc79-107">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2bc79-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2bc79-108">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="2bc79-108">**Element type**</span></span> <br/> |[<span data-ttu-id="2bc79-109">pp_Type</span><span class="sxs-lookup"><span data-stu-id="2bc79-109">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2bc79-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2bc79-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2bc79-111">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2bc79-111">**Schema file**</span></span> <br/> |<span data-ttu-id="2bc79-112">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="2bc79-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2bc79-113">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="2bc79-113">**Document parts**</span></span> <br/> |<span data-ttu-id="2bc79-114">Página #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="2bc79-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2bc79-115">Definición</span><span class="sxs-lookup"><span data-stu-id="2bc79-115">Definition</span></span>

```XML
< xs:element name="pp" type="pp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2bc79-116">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="2bc79-116">Elements and attributes</span></span>

<span data-ttu-id="2bc79-117">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="2bc79-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2bc79-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2bc79-118">Parent elements</span></span>

|<span data-ttu-id="2bc79-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2bc79-119">**Element**</span></span>|<span data-ttu-id="2bc79-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2bc79-120">**Type**</span></span>|<span data-ttu-id="2bc79-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2bc79-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2bc79-122">Text</span><span class="sxs-lookup"><span data-stu-id="2bc79-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2bc79-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="2bc79-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2bc79-124">Contiene el texto de una forma.</span><span class="sxs-lookup"><span data-stu-id="2bc79-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2bc79-125">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2bc79-125">Child elements</span></span>

<span data-ttu-id="2bc79-126">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2bc79-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2bc79-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="2bc79-127">Attributes</span></span>

|<span data-ttu-id="2bc79-128">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="2bc79-128">**Attribute**</span></span>|<span data-ttu-id="2bc79-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2bc79-129">**Type**</span></span>|<span data-ttu-id="2bc79-130">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="2bc79-130">**Required**</span></span>|<span data-ttu-id="2bc79-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2bc79-131">**Description**</span></span>|<span data-ttu-id="2bc79-132">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="2bc79-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2bc79-133">IX</span><span class="sxs-lookup"><span data-stu-id="2bc79-133">IX</span></span>  <br/> |<span data-ttu-id="2bc79-134">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2bc79-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2bc79-135">necesario</span><span class="sxs-lookup"><span data-stu-id="2bc79-135">required</span></span>  <br/> |<span data-ttu-id="2bc79-136">Índice del elemento **para** que especifica el formato que se aplica a este segmento.</span><span class="sxs-lookup"><span data-stu-id="2bc79-136">The index of the **Para** element that specifies the formatting applied to this run.</span></span>  <br/> |<span data-ttu-id="2bc79-137">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="2bc79-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

