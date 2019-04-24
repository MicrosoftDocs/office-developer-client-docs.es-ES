---
title: Sheet_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4855350c-8204-ef1f-4d08-4ab6540249e9
ms.openlocfilehash: dc8930ffa89baf059074a12bb285e6b53e329e41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342871"
---
# <a name="sheettype-complextype-visio-xml"></a><span data-ttu-id="448bd-102">Sheet_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="448bd-102">Sheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="448bd-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="448bd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="448bd-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="448bd-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="448bd-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="448bd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="448bd-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="448bd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="448bd-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="448bd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="448bd-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="448bd-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="448bd-109">Definición</span><span class="sxs-lookup"><span data-stu-id="448bd-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="448bd-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="448bd-110">Elements and attributes</span></span>

<span data-ttu-id="448bd-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="448bd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="448bd-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="448bd-112">Child elements</span></span>

|<span data-ttu-id="448bd-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="448bd-113">**Element**</span></span>|<span data-ttu-id="448bd-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="448bd-114">**Type**</span></span>|<span data-ttu-id="448bd-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="448bd-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="448bd-116">Cell</span><span class="sxs-lookup"><span data-stu-id="448bd-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="448bd-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="448bd-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="448bd-118">Section</span><span class="sxs-lookup"><span data-stu-id="448bd-118">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="448bd-119">Section_Type</span><span class="sxs-lookup"><span data-stu-id="448bd-119">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="448bd-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="448bd-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="448bd-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="448bd-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="448bd-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="448bd-122">Attributes</span></span>

|<span data-ttu-id="448bd-123">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="448bd-123">**Attribute**</span></span>|<span data-ttu-id="448bd-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="448bd-124">**Type**</span></span>|<span data-ttu-id="448bd-125">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="448bd-125">**Required**</span></span>|<span data-ttu-id="448bd-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="448bd-126">**Description**</span></span>|<span data-ttu-id="448bd-127">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="448bd-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="448bd-128">FillStyle</span><span class="sxs-lookup"><span data-stu-id="448bd-128">FillStyle</span></span>  <br/> |<span data-ttu-id="448bd-129">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="448bd-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="448bd-130">opcional</span><span class="sxs-lookup"><span data-stu-id="448bd-130">optional</span></span>  <br/> ||<span data-ttu-id="448bd-131">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="448bd-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="448bd-132">LineStyle</span><span class="sxs-lookup"><span data-stu-id="448bd-132">LineStyle</span></span>  <br/> |<span data-ttu-id="448bd-133">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="448bd-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="448bd-134">opcional</span><span class="sxs-lookup"><span data-stu-id="448bd-134">optional</span></span>  <br/> ||<span data-ttu-id="448bd-135">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="448bd-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="448bd-136">TextStyle</span><span class="sxs-lookup"><span data-stu-id="448bd-136">TextStyle</span></span>  <br/> |<span data-ttu-id="448bd-137">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="448bd-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="448bd-138">opcional</span><span class="sxs-lookup"><span data-stu-id="448bd-138">optional</span></span>  <br/> ||<span data-ttu-id="448bd-139">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="448bd-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

