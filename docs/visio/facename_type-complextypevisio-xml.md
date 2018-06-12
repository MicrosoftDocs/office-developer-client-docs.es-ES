---
title: FaceName_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: 554a8144fd38c34d59aa2fd0ae25d171c20cd8ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822097"
---
# <a name="facenametype-complextype-visio-xml"></a><span data-ttu-id="494c6-102">FaceName_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="494c6-102">FaceName_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="494c6-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="494c6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="494c6-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="494c6-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="494c6-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="494c6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="494c6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="494c6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="494c6-107">**Base de la extensión**</span><span class="sxs-lookup"><span data-stu-id="494c6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="494c6-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="494c6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="494c6-109">Definición</span><span class="sxs-lookup"><span data-stu-id="494c6-109">Definition</span></span>

```XML
      <xs:complexType name="FaceName_Type">
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="UnicodeRanges"
  type="xsd:string"
    />
    <xs:attribute name="CharSets"
  type="xsd:string"
    />
    <xs:attribute name="Panos"
  type="xsd:string"
    />
    <xs:attribute name="Panose"
  type="xsd:string"
    />
    <xs:attribute name="Flags"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="494c6-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="494c6-110">Elements and attributes</span></span>

<span data-ttu-id="494c6-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="494c6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="494c6-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="494c6-112">Child elements</span></span>

<span data-ttu-id="494c6-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="494c6-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="494c6-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="494c6-114">Attributes</span></span>

|<span data-ttu-id="494c6-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="494c6-115">**Attribute**</span></span>|<span data-ttu-id="494c6-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="494c6-116">**Type**</span></span>|<span data-ttu-id="494c6-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="494c6-117">**Required**</span></span>|<span data-ttu-id="494c6-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="494c6-118">**Description**</span></span>|<span data-ttu-id="494c6-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="494c6-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="494c6-120">Juegos de caracteres</span><span class="sxs-lookup"><span data-stu-id="494c6-120">CharSets</span></span>  <br/> |<span data-ttu-id="494c6-121">xsd: String</span><span class="sxs-lookup"><span data-stu-id="494c6-121">xsd:string</span></span>  <br/> |<span data-ttu-id="494c6-122">opcional</span><span class="sxs-lookup"><span data-stu-id="494c6-122">optional</span></span>  <br/> ||<span data-ttu-id="494c6-123">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="494c6-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="494c6-124">Marcas</span><span class="sxs-lookup"><span data-stu-id="494c6-124">Flags</span></span>  <br/> |<span data-ttu-id="494c6-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="494c6-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="494c6-126">opcional</span><span class="sxs-lookup"><span data-stu-id="494c6-126">optional</span></span>  <br/> ||<span data-ttu-id="494c6-127">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="494c6-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="494c6-128">NameU</span><span class="sxs-lookup"><span data-stu-id="494c6-128">NameU</span></span>  <br/> |<span data-ttu-id="494c6-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="494c6-129">xsd:string</span></span>  <br/> |<span data-ttu-id="494c6-130">necesario</span><span class="sxs-lookup"><span data-stu-id="494c6-130">required</span></span>  <br/> ||<span data-ttu-id="494c6-131">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="494c6-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="494c6-132">Panos</span><span class="sxs-lookup"><span data-stu-id="494c6-132">Panos</span></span>  <br/> |<span data-ttu-id="494c6-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="494c6-133">xsd:string</span></span>  <br/> |<span data-ttu-id="494c6-134">opcional</span><span class="sxs-lookup"><span data-stu-id="494c6-134">optional</span></span>  <br/> ||<span data-ttu-id="494c6-135">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="494c6-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="494c6-136">Panose</span><span class="sxs-lookup"><span data-stu-id="494c6-136">Panose</span></span>  <br/> |<span data-ttu-id="494c6-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="494c6-137">xsd:string</span></span>  <br/> |<span data-ttu-id="494c6-138">opcional</span><span class="sxs-lookup"><span data-stu-id="494c6-138">optional</span></span>  <br/> ||<span data-ttu-id="494c6-139">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="494c6-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="494c6-140">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="494c6-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="494c6-141">xsd: String</span><span class="sxs-lookup"><span data-stu-id="494c6-141">xsd:string</span></span>  <br/> |<span data-ttu-id="494c6-142">opcional</span><span class="sxs-lookup"><span data-stu-id="494c6-142">optional</span></span>  <br/> ||<span data-ttu-id="494c6-143">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="494c6-143">Values of the xsd:string type.</span></span>  <br/> |
   

