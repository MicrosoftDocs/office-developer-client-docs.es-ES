---
title: ComplexType HeaderFooter_Type (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5fcf3d9-c11a-ed5e-0bf5-e706259ef30b
ms.openlocfilehash: c95e4fee38a345aa2a634a8d0a2c213b49cc5277
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541123"
---
# <a name="headerfootertype-complextype-visio-xml"></a><span data-ttu-id="9fc97-102">ComplexType HeaderFooter_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="9fc97-102">HeaderFooter_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="9fc97-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="9fc97-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9fc97-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9fc97-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9fc97-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9fc97-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9fc97-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="9fc97-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9fc97-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="9fc97-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9fc97-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9fc97-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9fc97-109">Definición</span><span class="sxs-lookup"><span data-stu-id="9fc97-109">Definition</span></span>

```XML
          <xs:complexType name="HeaderFooter_Type">
          
          <xs:all>
    <xs:element name="HeaderMargin"  type="HeaderMargin_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterMargin"  type="FooterMargin_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderLeft"  type="HeaderLeft_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderCenter"  type="HeaderCenter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderRight"  type="HeaderRight_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterLeft"  type="FooterLeft_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterCenter"  type="FooterCenter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterRight"  type="FooterRight_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderFooterFont"  type="HeaderFooterFont_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="HeaderFooterColor"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9fc97-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="9fc97-110">Elements and attributes</span></span>

<span data-ttu-id="9fc97-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="9fc97-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9fc97-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9fc97-112">Child elements</span></span>

|<span data-ttu-id="9fc97-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9fc97-113">**Element**</span></span>|<span data-ttu-id="9fc97-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9fc97-114">**Type**</span></span>|<span data-ttu-id="9fc97-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9fc97-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9fc97-116">FooterCenter</span><span class="sxs-lookup"><span data-stu-id="9fc97-116">FooterCenter</span></span>](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9fc97-117">FooterCenter_Type</span><span class="sxs-lookup"><span data-stu-id="9fc97-117">FooterCenter_Type</span></span>](footercenter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9fc97-118">FooterLeft</span><span class="sxs-lookup"><span data-stu-id="9fc97-118">FooterLeft</span></span>](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9fc97-119">FooterLeft_Type</span><span class="sxs-lookup"><span data-stu-id="9fc97-119">FooterLeft_Type</span></span>](footerleft_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9fc97-120">FooterMargin</span><span class="sxs-lookup"><span data-stu-id="9fc97-120">FooterMargin</span></span>](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9fc97-121">FooterMargin_Type</span><span class="sxs-lookup"><span data-stu-id="9fc97-121">FooterMargin_Type</span></span>](footermargin_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9fc97-122">FooterRight</span><span class="sxs-lookup"><span data-stu-id="9fc97-122">FooterRight</span></span>](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9fc97-123">FooterRight_Type</span><span class="sxs-lookup"><span data-stu-id="9fc97-123">FooterRight_Type</span></span>](footerright_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9fc97-124">HeaderCenter</span><span class="sxs-lookup"><span data-stu-id="9fc97-124">HeaderCenter</span></span>](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9fc97-125">HeaderCenter_Type</span><span class="sxs-lookup"><span data-stu-id="9fc97-125">HeaderCenter_Type</span></span>](headercenter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9fc97-126">HeaderFooterFont</span><span class="sxs-lookup"><span data-stu-id="9fc97-126">HeaderFooterFont</span></span>](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9fc97-127">HeaderFooterFont_Type</span><span class="sxs-lookup"><span data-stu-id="9fc97-127">HeaderFooterFont_Type</span></span>](headerfooterfont_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9fc97-128">HeaderLeft</span><span class="sxs-lookup"><span data-stu-id="9fc97-128">HeaderLeft</span></span>](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9fc97-129">HeaderLeft_Type</span><span class="sxs-lookup"><span data-stu-id="9fc97-129">HeaderLeft_Type</span></span>](headerleft_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9fc97-130">HeaderMargin</span><span class="sxs-lookup"><span data-stu-id="9fc97-130">HeaderMargin</span></span>](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9fc97-131">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="9fc97-131">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9fc97-132">HeaderRight</span><span class="sxs-lookup"><span data-stu-id="9fc97-132">HeaderRight</span></span>](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9fc97-133">HeaderRight_Type</span><span class="sxs-lookup"><span data-stu-id="9fc97-133">HeaderRight_Type</span></span>](headerright_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9fc97-134">Atributos</span><span class="sxs-lookup"><span data-stu-id="9fc97-134">Attributes</span></span>

|<span data-ttu-id="9fc97-135">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="9fc97-135">**Attribute**</span></span>|<span data-ttu-id="9fc97-136">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9fc97-136">**Type**</span></span>|<span data-ttu-id="9fc97-137">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="9fc97-137">**Required**</span></span>|<span data-ttu-id="9fc97-138">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9fc97-138">**Description**</span></span>|<span data-ttu-id="9fc97-139">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="9fc97-139">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9fc97-140">HeaderFooterColor</span><span class="sxs-lookup"><span data-stu-id="9fc97-140">HeaderFooterColor</span></span>  <br/> |<span data-ttu-id="9fc97-141">xsd: String</span><span class="sxs-lookup"><span data-stu-id="9fc97-141">xsd:string</span></span>  <br/> |<span data-ttu-id="9fc97-142">opcional</span><span class="sxs-lookup"><span data-stu-id="9fc97-142">optional</span></span>  <br/> ||<span data-ttu-id="9fc97-143">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="9fc97-143">Values of the xsd:string type.</span></span>  <br/> |
   

