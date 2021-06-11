---
title: elemento tp (Text_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b13b9328-c6a0-e282-257c-2de55901df6a
description: Especifica el principio de la ejecución de las propiedades de las pestañas. La ejecución se define al final del texto o hasta la siguiente etiqueta.
ms.openlocfilehash: dad7a3de715473a75c601c1e391c9d51fc1cab85
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542978"
---
# <a name="tp-element-text_type-complextype-visio-xml"></a><span data-ttu-id="f2127-104">elemento tp (Text_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f2127-104">tp element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="f2127-105">Especifica el principio de la ejecución de las propiedades de las pestañas.</span><span class="sxs-lookup"><span data-stu-id="f2127-105">Specifies the beginning of a tabs properties run.</span></span> <span data-ttu-id="f2127-106">La ejecución se define al final del texto o hasta la siguiente etiqueta.</span><span class="sxs-lookup"><span data-stu-id="f2127-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f2127-107">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f2127-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f2127-108">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="f2127-108">**Element type**</span></span> <br/> |[<span data-ttu-id="f2127-109">tp_Type</span><span class="sxs-lookup"><span data-stu-id="f2127-109">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f2127-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f2127-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f2127-111">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f2127-111">**Schema file**</span></span> <br/> |<span data-ttu-id="f2127-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f2127-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f2127-113">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="f2127-113">**Document parts**</span></span> <br/> |<span data-ttu-id="f2127-114">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="f2127-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f2127-115">Definición</span><span class="sxs-lookup"><span data-stu-id="f2127-115">Definition</span></span>

```XML
< xs:element name="tp" type="tp_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f2127-116">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="f2127-116">Elements and attributes</span></span>

<span data-ttu-id="f2127-117">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="f2127-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f2127-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f2127-118">Parent elements</span></span>

|<span data-ttu-id="f2127-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f2127-119">**Element**</span></span>|<span data-ttu-id="f2127-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f2127-120">**Type**</span></span>|<span data-ttu-id="f2127-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f2127-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f2127-122">Text</span><span class="sxs-lookup"><span data-stu-id="f2127-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f2127-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="f2127-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f2127-124">Contiene el texto de una forma.</span><span class="sxs-lookup"><span data-stu-id="f2127-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f2127-125">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f2127-125">Child elements</span></span>

<span data-ttu-id="f2127-126">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f2127-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f2127-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="f2127-127">Attributes</span></span>

|<span data-ttu-id="f2127-128">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="f2127-128">**Attribute**</span></span>|<span data-ttu-id="f2127-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f2127-129">**Type**</span></span>|<span data-ttu-id="f2127-130">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="f2127-130">**Required**</span></span>|<span data-ttu-id="f2127-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f2127-131">**Description**</span></span>|<span data-ttu-id="f2127-132">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="f2127-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f2127-133">IX</span><span class="sxs-lookup"><span data-stu-id="f2127-133">IX</span></span>  <br/> |<span data-ttu-id="f2127-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f2127-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f2127-135">necesario</span><span class="sxs-lookup"><span data-stu-id="f2127-135">required</span></span>  <br/> |<span data-ttu-id="f2127-136">Índice basado en cero del elemento dentro de su elemento primario.</span><span class="sxs-lookup"><span data-stu-id="f2127-136">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="f2127-137">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f2127-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

