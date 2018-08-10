---
title: Sheet_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4855350c-8204-ef1f-4d08-4ab6540249e9
ms.openlocfilehash: f171f250fbe37ebf1d0d434709b06ab56804407f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823213"
---
# <a name="sheettype-complextype-visio-xml"></a><span data-ttu-id="0f780-102">Sheet_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="0f780-102">Sheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0f780-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="0f780-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0f780-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0f780-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0f780-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0f780-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0f780-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0f780-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0f780-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="0f780-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0f780-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="0f780-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0f780-109">Definición</span><span class="sxs-lookup"><span data-stu-id="0f780-109">Definition</span></span>

```XML
        <xs:complexType name="Sheet_Type" abstract="true">
        
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Trigger"  type="Trigger_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Section"  type="Section_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs: name="" >
    </xs:>
    
      </xs:sequence>
    <xs:attribute name="LineStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="FillStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="TextStyle"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0f780-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="0f780-110">Elements and attributes</span></span>

<span data-ttu-id="0f780-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="0f780-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0f780-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0f780-112">Child elements</span></span>

|<span data-ttu-id="0f780-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0f780-113">**Element**</span></span>|<span data-ttu-id="0f780-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0f780-114">**Type**</span></span>|<span data-ttu-id="0f780-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0f780-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0f780-116">Cell</span><span class="sxs-lookup"><span data-stu-id="0f780-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="0f780-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="0f780-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0f780-118">Section</span><span class="sxs-lookup"><span data-stu-id="0f780-118">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0f780-119">Section_Type</span><span class="sxs-lookup"><span data-stu-id="0f780-119">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0f780-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="0f780-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="0f780-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="0f780-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0f780-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="0f780-122">Attributes</span></span>

|<span data-ttu-id="0f780-123">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="0f780-123">**Attribute**</span></span>|<span data-ttu-id="0f780-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0f780-124">**Type**</span></span>|<span data-ttu-id="0f780-125">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="0f780-125">**Required**</span></span>|<span data-ttu-id="0f780-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0f780-126">**Description**</span></span>|<span data-ttu-id="0f780-127">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="0f780-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0f780-128">FillStyle</span><span class="sxs-lookup"><span data-stu-id="0f780-128">FillStyle</span></span>  <br/> |<span data-ttu-id="0f780-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0f780-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0f780-130">opcional</span><span class="sxs-lookup"><span data-stu-id="0f780-130">optional</span></span>  <br/> ||<span data-ttu-id="0f780-131">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0f780-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0f780-132">LineStyle</span><span class="sxs-lookup"><span data-stu-id="0f780-132">LineStyle</span></span>  <br/> |<span data-ttu-id="0f780-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0f780-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0f780-134">opcional</span><span class="sxs-lookup"><span data-stu-id="0f780-134">optional</span></span>  <br/> ||<span data-ttu-id="0f780-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0f780-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0f780-136">TextStyle</span><span class="sxs-lookup"><span data-stu-id="0f780-136">TextStyle</span></span>  <br/> |<span data-ttu-id="0f780-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0f780-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0f780-138">opcional</span><span class="sxs-lookup"><span data-stu-id="0f780-138">optional</span></span>  <br/> ||<span data-ttu-id="0f780-139">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0f780-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   
