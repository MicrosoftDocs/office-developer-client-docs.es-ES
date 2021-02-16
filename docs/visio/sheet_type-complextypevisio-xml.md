---
title: Sheet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4855350c-8204-ef1f-4d08-4ab6540249e9
ms.openlocfilehash: b747f2257f2b09083b72a17a59856be0a985b270
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540409"
---
# <a name="sheet_type-complextype-visio-xml"></a><span data-ttu-id="da5d5-102">Sheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="da5d5-102">Sheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="da5d5-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="da5d5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="da5d5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="da5d5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="da5d5-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="da5d5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="da5d5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="da5d5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="da5d5-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="da5d5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="da5d5-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="da5d5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="da5d5-109">Definición</span><span class="sxs-lookup"><span data-stu-id="da5d5-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="da5d5-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="da5d5-110">Elements and attributes</span></span>

<span data-ttu-id="da5d5-111">Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="da5d5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="da5d5-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="da5d5-112">Child elements</span></span>

|<span data-ttu-id="da5d5-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="da5d5-113">**Element**</span></span>|<span data-ttu-id="da5d5-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="da5d5-114">**Type**</span></span>|<span data-ttu-id="da5d5-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="da5d5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="da5d5-116">Cell</span><span class="sxs-lookup"><span data-stu-id="da5d5-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="da5d5-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="da5d5-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="da5d5-118">Section</span><span class="sxs-lookup"><span data-stu-id="da5d5-118">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="da5d5-119">Section_Type</span><span class="sxs-lookup"><span data-stu-id="da5d5-119">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="da5d5-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="da5d5-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="da5d5-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="da5d5-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="da5d5-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="da5d5-122">Attributes</span></span>

|<span data-ttu-id="da5d5-123">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="da5d5-123">**Attribute**</span></span>|<span data-ttu-id="da5d5-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="da5d5-124">**Type**</span></span>|<span data-ttu-id="da5d5-125">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="da5d5-125">**Required**</span></span>|<span data-ttu-id="da5d5-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="da5d5-126">**Description**</span></span>|<span data-ttu-id="da5d5-127">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="da5d5-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="da5d5-128">FillStyle</span><span class="sxs-lookup"><span data-stu-id="da5d5-128">FillStyle</span></span>  <br/> |<span data-ttu-id="da5d5-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="da5d5-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="da5d5-130">opcional</span><span class="sxs-lookup"><span data-stu-id="da5d5-130">optional</span></span>  <br/> ||<span data-ttu-id="da5d5-131">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="da5d5-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="da5d5-132">LineStyle</span><span class="sxs-lookup"><span data-stu-id="da5d5-132">LineStyle</span></span>  <br/> |<span data-ttu-id="da5d5-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="da5d5-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="da5d5-134">opcional</span><span class="sxs-lookup"><span data-stu-id="da5d5-134">optional</span></span>  <br/> ||<span data-ttu-id="da5d5-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="da5d5-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="da5d5-136">TextStyle</span><span class="sxs-lookup"><span data-stu-id="da5d5-136">TextStyle</span></span>  <br/> |<span data-ttu-id="da5d5-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="da5d5-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="da5d5-138">opcional</span><span class="sxs-lookup"><span data-stu-id="da5d5-138">optional</span></span>  <br/> ||<span data-ttu-id="da5d5-139">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="da5d5-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

