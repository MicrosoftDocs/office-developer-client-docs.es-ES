---
title: HeaderFooter_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5fcf3d9-c11a-ed5e-0bf5-e706259ef30b
ms.openlocfilehash: 9c567542061ec419de9c4347209059b0486bdf88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822255"
---
# <a name="headerfootertype-complextype-visio-xml"></a><span data-ttu-id="66ad7-102">HeaderFooter_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="66ad7-102">HeaderFooter_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="66ad7-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="66ad7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66ad7-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="66ad7-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="66ad7-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="66ad7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="66ad7-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="66ad7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="66ad7-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="66ad7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="66ad7-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="66ad7-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="66ad7-109">Definición</span><span class="sxs-lookup"><span data-stu-id="66ad7-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="66ad7-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="66ad7-110">Elements and attributes</span></span>

<span data-ttu-id="66ad7-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="66ad7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="66ad7-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="66ad7-112">Child elements</span></span>

|<span data-ttu-id="66ad7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="66ad7-113">**Element**</span></span>|<span data-ttu-id="66ad7-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="66ad7-114">**Type**</span></span>|<span data-ttu-id="66ad7-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="66ad7-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="66ad7-116">FooterCenter</span><span class="sxs-lookup"><span data-stu-id="66ad7-116">FooterCenter</span></span>](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="66ad7-117">FooterCenter_Type</span><span class="sxs-lookup"><span data-stu-id="66ad7-117">FooterCenter_Type</span></span>](footercenter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="66ad7-118">FooterLeft</span><span class="sxs-lookup"><span data-stu-id="66ad7-118">FooterLeft</span></span>](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="66ad7-119">FooterLeft_Type</span><span class="sxs-lookup"><span data-stu-id="66ad7-119">FooterLeft_Type</span></span>](footerleft_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="66ad7-120">FooterMargin</span><span class="sxs-lookup"><span data-stu-id="66ad7-120">FooterMargin</span></span>](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="66ad7-121">FooterMargin_Type</span><span class="sxs-lookup"><span data-stu-id="66ad7-121">FooterMargin_Type</span></span>](footermargin_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="66ad7-122">FooterRight</span><span class="sxs-lookup"><span data-stu-id="66ad7-122">FooterRight</span></span>](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="66ad7-123">FooterRight_Type</span><span class="sxs-lookup"><span data-stu-id="66ad7-123">FooterRight_Type</span></span>](footerright_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="66ad7-124">HeaderCenter</span><span class="sxs-lookup"><span data-stu-id="66ad7-124">HeaderCenter</span></span>](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="66ad7-125">HeaderCenter_Type</span><span class="sxs-lookup"><span data-stu-id="66ad7-125">HeaderCenter_Type</span></span>](headercenter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="66ad7-126">HeaderFooterFont</span><span class="sxs-lookup"><span data-stu-id="66ad7-126">HeaderFooterFont</span></span>](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="66ad7-127">HeaderFooterFont_Type</span><span class="sxs-lookup"><span data-stu-id="66ad7-127">HeaderFooterFont_Type</span></span>](headerfooterfont_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="66ad7-128">HeaderLeft</span><span class="sxs-lookup"><span data-stu-id="66ad7-128">HeaderLeft</span></span>](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="66ad7-129">HeaderLeft_Type</span><span class="sxs-lookup"><span data-stu-id="66ad7-129">HeaderLeft_Type</span></span>](headerleft_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="66ad7-130">HeaderMargin</span><span class="sxs-lookup"><span data-stu-id="66ad7-130">HeaderMargin</span></span>](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="66ad7-131">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="66ad7-131">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="66ad7-132">HeaderRight</span><span class="sxs-lookup"><span data-stu-id="66ad7-132">HeaderRight</span></span>](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="66ad7-133">HeaderRight_Type</span><span class="sxs-lookup"><span data-stu-id="66ad7-133">HeaderRight_Type</span></span>](headerright_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="66ad7-134">Atributos</span><span class="sxs-lookup"><span data-stu-id="66ad7-134">Attributes</span></span>

|<span data-ttu-id="66ad7-135">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="66ad7-135">**Attribute**</span></span>|<span data-ttu-id="66ad7-136">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="66ad7-136">**Type**</span></span>|<span data-ttu-id="66ad7-137">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="66ad7-137">**Required**</span></span>|<span data-ttu-id="66ad7-138">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="66ad7-138">**Description**</span></span>|<span data-ttu-id="66ad7-139">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="66ad7-139">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="66ad7-140">HeaderFooterColor</span><span class="sxs-lookup"><span data-stu-id="66ad7-140">HeaderFooterColor</span></span>  <br/> |<span data-ttu-id="66ad7-141">xsd: String</span><span class="sxs-lookup"><span data-stu-id="66ad7-141">xsd:string</span></span>  <br/> |<span data-ttu-id="66ad7-142">opcional</span><span class="sxs-lookup"><span data-stu-id="66ad7-142">optional</span></span>  <br/> ||<span data-ttu-id="66ad7-143">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="66ad7-143">Values of the xsd:string type.</span></span>  <br/> |
   

