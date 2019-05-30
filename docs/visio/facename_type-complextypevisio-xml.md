---
title: ComplexType FaceName_Type (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: f0a136cec6d620ba7001ed0e6fae01af82c2180d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542901"
---
# <a name="facenametype-complextype-visio-xml"></a><span data-ttu-id="cb6af-102">ComplexType FaceName_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="cb6af-102">FaceName_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="cb6af-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="cb6af-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb6af-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cb6af-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cb6af-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="cb6af-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cb6af-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="cb6af-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cb6af-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="cb6af-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cb6af-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="cb6af-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cb6af-109">Definición</span><span class="sxs-lookup"><span data-stu-id="cb6af-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="cb6af-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="cb6af-110">Elements and attributes</span></span>

<span data-ttu-id="cb6af-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="cb6af-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cb6af-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cb6af-112">Child elements</span></span>

<span data-ttu-id="cb6af-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cb6af-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cb6af-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="cb6af-114">Attributes</span></span>

|<span data-ttu-id="cb6af-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="cb6af-115">**Attribute**</span></span>|<span data-ttu-id="cb6af-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cb6af-116">**Type**</span></span>|<span data-ttu-id="cb6af-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="cb6af-117">**Required**</span></span>|<span data-ttu-id="cb6af-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cb6af-118">**Description**</span></span>|<span data-ttu-id="cb6af-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="cb6af-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cb6af-120">Juegos de caracteres</span><span class="sxs-lookup"><span data-stu-id="cb6af-120">CharSets</span></span>  <br/> |<span data-ttu-id="cb6af-121">xsd: String</span><span class="sxs-lookup"><span data-stu-id="cb6af-121">xsd:string</span></span>  <br/> |<span data-ttu-id="cb6af-122">opcional</span><span class="sxs-lookup"><span data-stu-id="cb6af-122">optional</span></span>  <br/> ||<span data-ttu-id="cb6af-123">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="cb6af-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cb6af-124">Flags</span><span class="sxs-lookup"><span data-stu-id="cb6af-124">Flags</span></span>  <br/> |<span data-ttu-id="cb6af-125">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cb6af-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cb6af-126">opcional</span><span class="sxs-lookup"><span data-stu-id="cb6af-126">optional</span></span>  <br/> ||<span data-ttu-id="cb6af-127">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cb6af-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cb6af-128">NameU</span><span class="sxs-lookup"><span data-stu-id="cb6af-128">NameU</span></span>  <br/> |<span data-ttu-id="cb6af-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="cb6af-129">xsd:string</span></span>  <br/> |<span data-ttu-id="cb6af-130">necesario</span><span class="sxs-lookup"><span data-stu-id="cb6af-130">required</span></span>  <br/> ||<span data-ttu-id="cb6af-131">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="cb6af-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cb6af-132">Panos</span><span class="sxs-lookup"><span data-stu-id="cb6af-132">Panos</span></span>  <br/> |<span data-ttu-id="cb6af-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="cb6af-133">xsd:string</span></span>  <br/> |<span data-ttu-id="cb6af-134">opcional</span><span class="sxs-lookup"><span data-stu-id="cb6af-134">optional</span></span>  <br/> ||<span data-ttu-id="cb6af-135">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="cb6af-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cb6af-136">Panose</span><span class="sxs-lookup"><span data-stu-id="cb6af-136">Panose</span></span>  <br/> |<span data-ttu-id="cb6af-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="cb6af-137">xsd:string</span></span>  <br/> |<span data-ttu-id="cb6af-138">opcional</span><span class="sxs-lookup"><span data-stu-id="cb6af-138">optional</span></span>  <br/> ||<span data-ttu-id="cb6af-139">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="cb6af-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cb6af-140">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="cb6af-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="cb6af-141">xsd: String</span><span class="sxs-lookup"><span data-stu-id="cb6af-141">xsd:string</span></span>  <br/> |<span data-ttu-id="cb6af-142">opcional</span><span class="sxs-lookup"><span data-stu-id="cb6af-142">optional</span></span>  <br/> ||<span data-ttu-id="cb6af-143">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="cb6af-143">Values of the xsd:string type.</span></span>  <br/> |
   

