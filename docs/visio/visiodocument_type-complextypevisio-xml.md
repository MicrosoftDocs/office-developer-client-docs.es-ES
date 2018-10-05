---
title: VisioDocument_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5003f98e-4fed-73f8-be55-5b068d9cbffe
ms.openlocfilehash: 3b794f4e7843b89dda2c23216478bc1b72f8753a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389851"
---
# <a name="visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="2745c-102">VisioDocument_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="2745c-102">VisioDocument_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2745c-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="2745c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2745c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2745c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2745c-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2745c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2745c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2745c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2745c-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="2745c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2745c-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2745c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2745c-109">Definición</span><span class="sxs-lookup"><span data-stu-id="2745c-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="2745c-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="2745c-110">Elements and attributes</span></span>

<span data-ttu-id="2745c-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="2745c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2745c-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2745c-112">Child elements</span></span>

|<span data-ttu-id="2745c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2745c-113">**Element**</span></span>|<span data-ttu-id="2745c-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2745c-114">**Type**</span></span>|<span data-ttu-id="2745c-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2745c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2745c-116">Colores</span><span class="sxs-lookup"><span data-stu-id="2745c-116">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2745c-117">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="2745c-117">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="2745c-118">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="2745c-118">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2745c-119">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="2745c-119">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="2745c-120">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="2745c-120">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2745c-121">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="2745c-121">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="2745c-122">EventList</span><span class="sxs-lookup"><span data-stu-id="2745c-122">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2745c-123">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="2745c-123">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="2745c-124">FaceNames</span><span class="sxs-lookup"><span data-stu-id="2745c-124">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2745c-125">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="2745c-125">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="2745c-126">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="2745c-126">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2745c-127">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="2745c-127">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="2745c-128">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="2745c-128">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2745c-129">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="2745c-129">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="2745c-130">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="2745c-130">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2745c-131">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="2745c-131">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2745c-132">Atributos</span><span class="sxs-lookup"><span data-stu-id="2745c-132">Attributes</span></span>

<span data-ttu-id="2745c-133">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2745c-133">None.</span></span>
  

