---
title: Section_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f8e855f-064c-d286-560f-9f89e7fce7b7
ms.openlocfilehash: 35cd638d36f4ddd1d90e0c312e65626f7d8b0bff
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384300"
---
# <a name="sectiontype-complextype-visio-xml"></a><span data-ttu-id="f38eb-102">Section_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="f38eb-102">Section_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f38eb-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="f38eb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f38eb-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f38eb-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f38eb-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f38eb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f38eb-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f38eb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f38eb-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="f38eb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f38eb-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f38eb-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f38eb-109">Definición</span><span class="sxs-lookup"><span data-stu-id="f38eb-109">Definition</span></span>

```XML
          <xs:complexType name="Section_Type">
          
          <xs:sequence>
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
    
    <xs:element name="Row"  type="Row_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Del"
  type="xsd:boolean"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f38eb-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="f38eb-110">Elements and attributes</span></span>

<span data-ttu-id="f38eb-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="f38eb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f38eb-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f38eb-112">Child elements</span></span>

|<span data-ttu-id="f38eb-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f38eb-113">**Element**</span></span>|<span data-ttu-id="f38eb-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f38eb-114">**Type**</span></span>|<span data-ttu-id="f38eb-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f38eb-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f38eb-116">Cell</span><span class="sxs-lookup"><span data-stu-id="f38eb-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="f38eb-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="f38eb-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="f38eb-118">Row</span><span class="sxs-lookup"><span data-stu-id="f38eb-118">Row</span></span>](https://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[<span data-ttu-id="f38eb-119">Row_Type</span><span class="sxs-lookup"><span data-stu-id="f38eb-119">Row_Type</span></span>](row_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="f38eb-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="f38eb-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="f38eb-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="f38eb-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f38eb-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="f38eb-122">Attributes</span></span>

|<span data-ttu-id="f38eb-123">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="f38eb-123">**Attribute**</span></span>|<span data-ttu-id="f38eb-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f38eb-124">**Type**</span></span>|<span data-ttu-id="f38eb-125">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="f38eb-125">**Required**</span></span>|<span data-ttu-id="f38eb-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f38eb-126">**Description**</span></span>|<span data-ttu-id="f38eb-127">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="f38eb-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f38eb-128">SUPR</span><span class="sxs-lookup"><span data-stu-id="f38eb-128">Del</span></span>  <br/> |<span data-ttu-id="f38eb-129">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="f38eb-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f38eb-130">opcional</span><span class="sxs-lookup"><span data-stu-id="f38eb-130">optional</span></span>  <br/> ||<span data-ttu-id="f38eb-131">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="f38eb-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f38eb-132">IX</span><span class="sxs-lookup"><span data-stu-id="f38eb-132">IX</span></span>  <br/> |<span data-ttu-id="f38eb-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f38eb-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f38eb-134">opcional</span><span class="sxs-lookup"><span data-stu-id="f38eb-134">optional</span></span>  <br/> ||<span data-ttu-id="f38eb-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f38eb-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f38eb-136">N</span><span class="sxs-lookup"><span data-stu-id="f38eb-136">N</span></span>  <br/> |<span data-ttu-id="f38eb-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="f38eb-137">xsd:string</span></span>  <br/> |<span data-ttu-id="f38eb-138">necesario</span><span class="sxs-lookup"><span data-stu-id="f38eb-138">required</span></span>  <br/> ||<span data-ttu-id="f38eb-139">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="f38eb-139">Values of the xsd:string type.</span></span>  <br/> |
   

