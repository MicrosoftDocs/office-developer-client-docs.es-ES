---
title: Elemento ColorEntry (Colors_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f325ad8-bbc7-28bf-9e48-1fde4fbdbdc0
description: Contiene una entrada de tabla de colores.
ms.openlocfilehash: f2221d8d32823e5eec4a100eaf4e8f62b914df28
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540185"
---
# <a name="colorentry-element-colors_type-complextype-visio-xml"></a><span data-ttu-id="5be91-103">Elemento ColorEntry (Colors_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5be91-103">ColorEntry element (Colors_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="5be91-104">Contiene una entrada de tabla de colores.</span><span class="sxs-lookup"><span data-stu-id="5be91-104">Contains a color table entry.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5be91-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5be91-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5be91-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="5be91-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5be91-107">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="5be91-107">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5be91-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5be91-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5be91-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="5be91-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5be91-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="5be91-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5be91-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="5be91-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5be91-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="5be91-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5be91-113">Definición</span><span class="sxs-lookup"><span data-stu-id="5be91-113">Definition</span></span>

```XML
< xs:element name="ColorEntry" type="ColorEntry_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5be91-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="5be91-114">Elements and attributes</span></span>

<span data-ttu-id="5be91-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="5be91-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5be91-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5be91-116">Parent elements</span></span>

|<span data-ttu-id="5be91-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5be91-117">**Element**</span></span>|<span data-ttu-id="5be91-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5be91-118">**Type**</span></span>|<span data-ttu-id="5be91-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5be91-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5be91-120">Colors</span><span class="sxs-lookup"><span data-stu-id="5be91-120">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5be91-121">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="5be91-121">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5be91-122">Contiene la tabla de colores del documento.</span><span class="sxs-lookup"><span data-stu-id="5be91-122">Contains the document's color table.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5be91-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5be91-123">Child elements</span></span>

<span data-ttu-id="5be91-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5be91-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5be91-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="5be91-125">Attributes</span></span>

|<span data-ttu-id="5be91-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="5be91-126">**Attribute**</span></span>|<span data-ttu-id="5be91-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5be91-127">**Type**</span></span>|<span data-ttu-id="5be91-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="5be91-128">**Required**</span></span>|<span data-ttu-id="5be91-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5be91-129">**Description**</span></span>|<span data-ttu-id="5be91-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="5be91-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5be91-131">IX</span><span class="sxs-lookup"><span data-stu-id="5be91-131">IX</span></span>  <br/> |<span data-ttu-id="5be91-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5be91-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5be91-133">necesario</span><span class="sxs-lookup"><span data-stu-id="5be91-133">required</span></span>  <br/> |<span data-ttu-id="5be91-134">Índice basado en cero del elemento dentro de su elemento primario.</span><span class="sxs-lookup"><span data-stu-id="5be91-134">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="5be91-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5be91-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5be91-136">RGB</span><span class="sxs-lookup"><span data-stu-id="5be91-136">RGB</span></span>  <br/> |<span data-ttu-id="5be91-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5be91-137">xsd:string</span></span>  <br/> |<span data-ttu-id="5be91-138">necesario</span><span class="sxs-lookup"><span data-stu-id="5be91-138">required</span></span>  <br/> |<span data-ttu-id="5be91-139">Valor hexadecimal de la entrada de la tabla de colores.</span><span class="sxs-lookup"><span data-stu-id="5be91-139">The hexadecimal value of the color table entry.</span></span>  <br/> |<span data-ttu-id="5be91-140">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="5be91-140">Values of the xsd:string type.</span></span>  <br/> |
   

