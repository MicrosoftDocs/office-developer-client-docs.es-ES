---
title: elemento pp (Text_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5444543-fcd9-91cc-e7f8-cf860caa9fcc
description: Especifica el principio de una ejecución de propiedades de párrafo. La ejecución se define al final del texto o hasta la siguiente etiqueta.
ms.openlocfilehash: 695958c77f730abed03f50d6ad9c71f4de76dd63
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537741"
---
# <a name="pp-element-text_type-complextype-visio-xml"></a><span data-ttu-id="9d702-104">elemento pp (Text_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9d702-104">pp element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="9d702-105">Especifica el principio de una ejecución de propiedades de párrafo.</span><span class="sxs-lookup"><span data-stu-id="9d702-105">Specifies the beginning of a paragraph properties run.</span></span> <span data-ttu-id="9d702-106">La ejecución se define al final del texto o hasta la siguiente etiqueta.</span><span class="sxs-lookup"><span data-stu-id="9d702-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9d702-107">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9d702-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d702-108">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="9d702-108">**Element type**</span></span> <br/> |[<span data-ttu-id="9d702-109">pp_Type</span><span class="sxs-lookup"><span data-stu-id="9d702-109">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9d702-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9d702-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9d702-111">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9d702-111">**Schema file**</span></span> <br/> |<span data-ttu-id="9d702-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9d702-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9d702-113">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="9d702-113">**Document parts**</span></span> <br/> |<span data-ttu-id="9d702-114">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="9d702-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9d702-115">Definición</span><span class="sxs-lookup"><span data-stu-id="9d702-115">Definition</span></span>

```XML
< xs:element name="pp" type="pp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9d702-116">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="9d702-116">Elements and attributes</span></span>

<span data-ttu-id="9d702-117">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="9d702-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9d702-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9d702-118">Parent elements</span></span>

|<span data-ttu-id="9d702-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9d702-119">**Element**</span></span>|<span data-ttu-id="9d702-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9d702-120">**Type**</span></span>|<span data-ttu-id="9d702-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9d702-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9d702-122">Text</span><span class="sxs-lookup"><span data-stu-id="9d702-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9d702-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="9d702-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9d702-124">Contiene el texto de una forma.</span><span class="sxs-lookup"><span data-stu-id="9d702-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9d702-125">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9d702-125">Child elements</span></span>

<span data-ttu-id="9d702-126">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9d702-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9d702-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="9d702-127">Attributes</span></span>

|<span data-ttu-id="9d702-128">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="9d702-128">**Attribute**</span></span>|<span data-ttu-id="9d702-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9d702-129">**Type**</span></span>|<span data-ttu-id="9d702-130">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="9d702-130">**Required**</span></span>|<span data-ttu-id="9d702-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9d702-131">**Description**</span></span>|<span data-ttu-id="9d702-132">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="9d702-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9d702-133">IX</span><span class="sxs-lookup"><span data-stu-id="9d702-133">IX</span></span>  <br/> |<span data-ttu-id="9d702-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9d702-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9d702-135">necesario</span><span class="sxs-lookup"><span data-stu-id="9d702-135">required</span></span>  <br/> |<span data-ttu-id="9d702-136">Índice del elemento **Para** que especifica el formato aplicado a esta ejecución.</span><span class="sxs-lookup"><span data-stu-id="9d702-136">The index of the **Para** element that specifies the formatting applied to this run.</span></span>  <br/> |<span data-ttu-id="9d702-137">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9d702-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

