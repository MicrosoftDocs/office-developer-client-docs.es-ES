---
title: elemento fld (Text_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92d90240-012b-9598-c893-6e7085813aa5
description: Indica un punto de inserción de campo de texto para el elemento Field correspondiente.
ms.openlocfilehash: efacb7ed11968dec5d5c2f62b0ca3e3bcd8580c0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539617"
---
# <a name="fld-element-text_type-complextype-visio-xml"></a><span data-ttu-id="8bfa7-103">elemento fld (Text_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="8bfa7-103">fld element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="8bfa7-104">Indica un punto de inserción de campo de texto para el elemento **Field** correspondiente.</span><span class="sxs-lookup"><span data-stu-id="8bfa7-104">Indicates a text-field insertion point for the corresponding **Field** element.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="8bfa7-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8bfa7-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8bfa7-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="8bfa7-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8bfa7-107">fld_Type</span><span class="sxs-lookup"><span data-stu-id="8bfa7-107">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8bfa7-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8bfa7-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8bfa7-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="8bfa7-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8bfa7-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8bfa7-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8bfa7-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="8bfa7-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8bfa7-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="8bfa7-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8bfa7-113">Definición</span><span class="sxs-lookup"><span data-stu-id="8bfa7-113">Definition</span></span>

```XML
< xs:element name="fld" type="fld_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8bfa7-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="8bfa7-114">Elements and attributes</span></span>

<span data-ttu-id="8bfa7-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="8bfa7-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8bfa7-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8bfa7-116">Parent elements</span></span>

|<span data-ttu-id="8bfa7-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8bfa7-117">**Element**</span></span>|<span data-ttu-id="8bfa7-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8bfa7-118">**Type**</span></span>|<span data-ttu-id="8bfa7-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8bfa7-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8bfa7-120">Text</span><span class="sxs-lookup"><span data-stu-id="8bfa7-120">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8bfa7-121">Text_Type</span><span class="sxs-lookup"><span data-stu-id="8bfa7-121">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8bfa7-122">Contiene el texto de una forma.</span><span class="sxs-lookup"><span data-stu-id="8bfa7-122">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8bfa7-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8bfa7-123">Child elements</span></span>

<span data-ttu-id="8bfa7-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8bfa7-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8bfa7-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="8bfa7-125">Attributes</span></span>

|<span data-ttu-id="8bfa7-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="8bfa7-126">**Attribute**</span></span>|<span data-ttu-id="8bfa7-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8bfa7-127">**Type**</span></span>|<span data-ttu-id="8bfa7-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="8bfa7-128">**Required**</span></span>|<span data-ttu-id="8bfa7-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8bfa7-129">**Description**</span></span>|<span data-ttu-id="8bfa7-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="8bfa7-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8bfa7-131">IX</span><span class="sxs-lookup"><span data-stu-id="8bfa7-131">IX</span></span>  <br/> |<span data-ttu-id="8bfa7-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8bfa7-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8bfa7-133">necesario</span><span class="sxs-lookup"><span data-stu-id="8bfa7-133">required</span></span>  <br/> |<span data-ttu-id="8bfa7-134">Índice basado en cero del elemento dentro de su elemento primario.</span><span class="sxs-lookup"><span data-stu-id="8bfa7-134">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="8bfa7-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8bfa7-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

