---
title: VisioDocument_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5003f98e-4fed-73f8-be55-5b068d9cbffe
ms.openlocfilehash: f56ec2f09ebd14683952c70b62f84cffb97f2e7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823537"
---
# <a name="visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="0f184-102">VisioDocument_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="0f184-102">VisioDocument_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0f184-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="0f184-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0f184-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0f184-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0f184-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0f184-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0f184-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0f184-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0f184-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="0f184-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0f184-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="0f184-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0f184-109">Definición</span><span class="sxs-lookup"><span data-stu-id="0f184-109">Definition</span></span>

```XML
          <xs:complexType name="VisioDocument_Type">
          
          <xs:sequence>
    <xs:element name="DocumentSettings"  type="DocumentSettings_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Colors"  type="Colors_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FaceNames"  type="FaceNames_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="StyleSheets"  type="StyleSheets_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="DocumentSheet"  type="DocumentSheet_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="EventList"  type="EventList_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderFooter"  type="HeaderFooter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="PublishSettings"  type="PublishSettings_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs: name="" >
    </xs:>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0f184-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="0f184-110">Elements and attributes</span></span>

<span data-ttu-id="0f184-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="0f184-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0f184-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0f184-112">Child elements</span></span>

|<span data-ttu-id="0f184-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0f184-113">**Element**</span></span>|<span data-ttu-id="0f184-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0f184-114">**Type**</span></span>|<span data-ttu-id="0f184-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0f184-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0f184-116">Colores</span><span class="sxs-lookup"><span data-stu-id="0f184-116">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0f184-117">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="0f184-117">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0f184-118">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="0f184-118">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0f184-119">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="0f184-119">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0f184-120">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="0f184-120">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0f184-121">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="0f184-121">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0f184-122">EventList</span><span class="sxs-lookup"><span data-stu-id="0f184-122">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0f184-123">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="0f184-123">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0f184-124">FaceNames</span><span class="sxs-lookup"><span data-stu-id="0f184-124">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0f184-125">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="0f184-125">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0f184-126">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="0f184-126">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0f184-127">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="0f184-127">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0f184-128">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="0f184-128">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0f184-129">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="0f184-129">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0f184-130">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="0f184-130">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0f184-131">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="0f184-131">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0f184-132">Atributos</span><span class="sxs-lookup"><span data-stu-id="0f184-132">Attributes</span></span>

<span data-ttu-id="0f184-133">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0f184-133">None.</span></span>
  

