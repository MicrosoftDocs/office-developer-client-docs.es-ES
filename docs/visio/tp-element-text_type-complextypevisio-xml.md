---
title: elemento TP (complexType Text_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b13b9328-c6a0-e282-257c-2de55901df6a
description: Especifica el principio de una ejecución de propiedades de tabulaciones. La ejecución se define hasta el final del texto o hasta la siguiente etiqueta.
ms.openlocfilehash: 3f27ea0babefa0ea69cbbc361031c57602649107
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307703"
---
# <a name="tp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="f3ba2-104">elemento TP (complexType Text_Type) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="f3ba2-104">tp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="f3ba2-105">Especifica el principio de una ejecución de propiedades de tabulaciones.</span><span class="sxs-lookup"><span data-stu-id="f3ba2-105">Specifies the beginning of a tabs properties run.</span></span> <span data-ttu-id="f3ba2-106">La ejecución se define hasta el final del texto o hasta la siguiente etiqueta.</span><span class="sxs-lookup"><span data-stu-id="f3ba2-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f3ba2-107">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f3ba2-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f3ba2-108">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="f3ba2-108">**Element type**</span></span> <br/> |[<span data-ttu-id="f3ba2-109">tp_Type</span><span class="sxs-lookup"><span data-stu-id="f3ba2-109">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f3ba2-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f3ba2-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f3ba2-111">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f3ba2-111">**Schema file**</span></span> <br/> |<span data-ttu-id="f3ba2-112">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="f3ba2-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f3ba2-113">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="f3ba2-113">**Document parts**</span></span> <br/> |<span data-ttu-id="f3ba2-114">Página #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="f3ba2-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f3ba2-115">Definición</span><span class="sxs-lookup"><span data-stu-id="f3ba2-115">Definition</span></span>

```XML
< xs:element name="tp" type="tp_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f3ba2-116">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="f3ba2-116">Elements and attributes</span></span>

<span data-ttu-id="f3ba2-117">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="f3ba2-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f3ba2-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f3ba2-118">Parent elements</span></span>

|<span data-ttu-id="f3ba2-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f3ba2-119">**Element**</span></span>|<span data-ttu-id="f3ba2-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f3ba2-120">**Type**</span></span>|<span data-ttu-id="f3ba2-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f3ba2-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f3ba2-122">Text</span><span class="sxs-lookup"><span data-stu-id="f3ba2-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f3ba2-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="f3ba2-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f3ba2-124">Contiene el texto de una forma.</span><span class="sxs-lookup"><span data-stu-id="f3ba2-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f3ba2-125">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f3ba2-125">Child elements</span></span>

<span data-ttu-id="f3ba2-126">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f3ba2-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f3ba2-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="f3ba2-127">Attributes</span></span>

|<span data-ttu-id="f3ba2-128">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="f3ba2-128">**Attribute**</span></span>|<span data-ttu-id="f3ba2-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f3ba2-129">**Type**</span></span>|<span data-ttu-id="f3ba2-130">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="f3ba2-130">**Required**</span></span>|<span data-ttu-id="f3ba2-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f3ba2-131">**Description**</span></span>|<span data-ttu-id="f3ba2-132">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="f3ba2-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f3ba2-133">IX</span><span class="sxs-lookup"><span data-stu-id="f3ba2-133">IX</span></span>  <br/> |<span data-ttu-id="f3ba2-134">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f3ba2-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f3ba2-135">necesario</span><span class="sxs-lookup"><span data-stu-id="f3ba2-135">required</span></span>  <br/> |<span data-ttu-id="f3ba2-136">Índice de base cero del elemento dentro de su elemento primario.</span><span class="sxs-lookup"><span data-stu-id="f3ba2-136">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="f3ba2-137">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f3ba2-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

