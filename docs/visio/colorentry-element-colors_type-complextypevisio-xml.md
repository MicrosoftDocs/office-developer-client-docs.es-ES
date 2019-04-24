---
title: Elemento ColorEntry (complexType Colors_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f325ad8-bbc7-28bf-9e48-1fde4fbdbdc0
description: Contiene una entrada de la tabla de colores.
ms.openlocfilehash: 14ef92069ce8d963ce4a0770324843321804c5cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358089"
---
# <a name="colorentry-element-colorstype-complextype-visio-xml"></a><span data-ttu-id="569c5-103">Elemento ColorEntry (complexType Colors_Type) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="569c5-103">ColorEntry element (Colors_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="569c5-104">Contiene una entrada de la tabla de colores.</span><span class="sxs-lookup"><span data-stu-id="569c5-104">Contains a color table entry.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="569c5-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="569c5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="569c5-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="569c5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="569c5-107">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="569c5-107">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="569c5-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="569c5-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="569c5-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="569c5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="569c5-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="569c5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="569c5-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="569c5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="569c5-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="569c5-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="569c5-113">Definición</span><span class="sxs-lookup"><span data-stu-id="569c5-113">Definition</span></span>

```XML
< xs:element name="ColorEntry" type="ColorEntry_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="569c5-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="569c5-114">Elements and attributes</span></span>

<span data-ttu-id="569c5-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="569c5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="569c5-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="569c5-116">Parent elements</span></span>

|<span data-ttu-id="569c5-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="569c5-117">**Element**</span></span>|<span data-ttu-id="569c5-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="569c5-118">**Type**</span></span>|<span data-ttu-id="569c5-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="569c5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="569c5-120">Colors</span><span class="sxs-lookup"><span data-stu-id="569c5-120">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="569c5-121">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="569c5-121">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="569c5-122">Contiene la tabla de colores del documento.</span><span class="sxs-lookup"><span data-stu-id="569c5-122">Contains the document's color table.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="569c5-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="569c5-123">Child elements</span></span>

<span data-ttu-id="569c5-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="569c5-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="569c5-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="569c5-125">Attributes</span></span>

|<span data-ttu-id="569c5-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="569c5-126">**Attribute**</span></span>|<span data-ttu-id="569c5-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="569c5-127">**Type**</span></span>|<span data-ttu-id="569c5-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="569c5-128">**Required**</span></span>|<span data-ttu-id="569c5-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="569c5-129">**Description**</span></span>|<span data-ttu-id="569c5-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="569c5-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="569c5-131">IX</span><span class="sxs-lookup"><span data-stu-id="569c5-131">IX</span></span>  <br/> |<span data-ttu-id="569c5-132">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="569c5-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="569c5-133">necesario</span><span class="sxs-lookup"><span data-stu-id="569c5-133">required</span></span>  <br/> |<span data-ttu-id="569c5-134">Índice de base cero del elemento dentro de su elemento primario.</span><span class="sxs-lookup"><span data-stu-id="569c5-134">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="569c5-135">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="569c5-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="569c5-136">RGB</span><span class="sxs-lookup"><span data-stu-id="569c5-136">RGB</span></span>  <br/> |<span data-ttu-id="569c5-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="569c5-137">xsd:string</span></span>  <br/> |<span data-ttu-id="569c5-138">necesario</span><span class="sxs-lookup"><span data-stu-id="569c5-138">required</span></span>  <br/> |<span data-ttu-id="569c5-139">Valor hexadecimal de la entrada de la tabla de colores.</span><span class="sxs-lookup"><span data-stu-id="569c5-139">The hexadecimal value of the color table entry.</span></span>  <br/> |<span data-ttu-id="569c5-140">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="569c5-140">Values of the xsd:string type.</span></span>  <br/> |
   

