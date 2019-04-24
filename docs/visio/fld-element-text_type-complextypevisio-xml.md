---
title: elemento FLD (Text_Type complexType) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92d90240-012b-9598-c893-6e7085813aa5
description: Indica un punto de inserción de campo de texto para el elemento Field correspondiente.
ms.openlocfilehash: a7303697a9471dab68f5b1cf851f60d51650a84e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346217"
---
# <a name="fld-element-texttype-complextype-visio-xml"></a><span data-ttu-id="fb711-103">elemento FLD (Text_Type complexType) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="fb711-103">fld element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="fb711-104">Indica un punto de inserción de campo de texto para el elemento **Field** correspondiente.</span><span class="sxs-lookup"><span data-stu-id="fb711-104">Indicates a text-field insertion point for the corresponding **Field** element.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="fb711-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fb711-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fb711-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="fb711-106">**Element type**</span></span> <br/> |[<span data-ttu-id="fb711-107">fld_Type</span><span class="sxs-lookup"><span data-stu-id="fb711-107">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fb711-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fb711-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fb711-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="fb711-109">**Schema file**</span></span> <br/> |<span data-ttu-id="fb711-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="fb711-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fb711-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="fb711-111">**Document parts**</span></span> <br/> |<span data-ttu-id="fb711-112">Página #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="fb711-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fb711-113">Definición</span><span class="sxs-lookup"><span data-stu-id="fb711-113">Definition</span></span>

```XML
< xs:element name="fld" type="fld_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fb711-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="fb711-114">Elements and attributes</span></span>

<span data-ttu-id="fb711-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="fb711-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fb711-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fb711-116">Parent elements</span></span>

|<span data-ttu-id="fb711-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fb711-117">**Element**</span></span>|<span data-ttu-id="fb711-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fb711-118">**Type**</span></span>|<span data-ttu-id="fb711-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fb711-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fb711-120">Text</span><span class="sxs-lookup"><span data-stu-id="fb711-120">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fb711-121">Text_Type</span><span class="sxs-lookup"><span data-stu-id="fb711-121">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fb711-122">Contiene el texto de una forma.</span><span class="sxs-lookup"><span data-stu-id="fb711-122">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fb711-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fb711-123">Child elements</span></span>

<span data-ttu-id="fb711-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fb711-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fb711-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="fb711-125">Attributes</span></span>

|<span data-ttu-id="fb711-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="fb711-126">**Attribute**</span></span>|<span data-ttu-id="fb711-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fb711-127">**Type**</span></span>|<span data-ttu-id="fb711-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="fb711-128">**Required**</span></span>|<span data-ttu-id="fb711-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fb711-129">**Description**</span></span>|<span data-ttu-id="fb711-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="fb711-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fb711-131">IX</span><span class="sxs-lookup"><span data-stu-id="fb711-131">IX</span></span>  <br/> |<span data-ttu-id="fb711-132">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fb711-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fb711-133">necesario</span><span class="sxs-lookup"><span data-stu-id="fb711-133">required</span></span>  <br/> |<span data-ttu-id="fb711-134">Índice de base cero del elemento dentro de su elemento primario.</span><span class="sxs-lookup"><span data-stu-id="fb711-134">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="fb711-135">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fb711-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

