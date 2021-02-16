---
title: Section_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f8e855f-064c-d286-560f-9f89e7fce7b7
ms.openlocfilehash: 48dd7a0ffc487b4a7a4200505f08d0aca42fd3c6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542131"
---
# <a name="section_type-complextype-visio-xml"></a><span data-ttu-id="edd41-102">Section_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="edd41-102">Section_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="edd41-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="edd41-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="edd41-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="edd41-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="edd41-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="edd41-105">**Schema file**</span></span> <br/> |<span data-ttu-id="edd41-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="edd41-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="edd41-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="edd41-107">**Extension base**</span></span> <br/> |<span data-ttu-id="edd41-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="edd41-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="edd41-109">Definición</span><span class="sxs-lookup"><span data-stu-id="edd41-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="edd41-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="edd41-110">Elements and attributes</span></span>

<span data-ttu-id="edd41-111">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="edd41-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="edd41-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="edd41-112">Child elements</span></span>

|<span data-ttu-id="edd41-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="edd41-113">**Element**</span></span>|<span data-ttu-id="edd41-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="edd41-114">**Type**</span></span>|<span data-ttu-id="edd41-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="edd41-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="edd41-116">Cell</span><span class="sxs-lookup"><span data-stu-id="edd41-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="edd41-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="edd41-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="edd41-118">Fila</span><span class="sxs-lookup"><span data-stu-id="edd41-118">Row</span></span>](https://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[<span data-ttu-id="edd41-119">Row_Type</span><span class="sxs-lookup"><span data-stu-id="edd41-119">Row_Type</span></span>](row_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="edd41-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="edd41-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="edd41-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="edd41-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="edd41-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="edd41-122">Attributes</span></span>

|<span data-ttu-id="edd41-123">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="edd41-123">**Attribute**</span></span>|<span data-ttu-id="edd41-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="edd41-124">**Type**</span></span>|<span data-ttu-id="edd41-125">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="edd41-125">**Required**</span></span>|<span data-ttu-id="edd41-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="edd41-126">**Description**</span></span>|<span data-ttu-id="edd41-127">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="edd41-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="edd41-128">Supr</span><span class="sxs-lookup"><span data-stu-id="edd41-128">Del</span></span>  <br/> |<span data-ttu-id="edd41-129">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="edd41-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="edd41-130">opcional</span><span class="sxs-lookup"><span data-stu-id="edd41-130">optional</span></span>  <br/> ||<span data-ttu-id="edd41-131">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="edd41-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="edd41-132">IX</span><span class="sxs-lookup"><span data-stu-id="edd41-132">IX</span></span>  <br/> |<span data-ttu-id="edd41-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="edd41-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="edd41-134">opcional</span><span class="sxs-lookup"><span data-stu-id="edd41-134">optional</span></span>  <br/> ||<span data-ttu-id="edd41-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="edd41-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="edd41-136">N</span><span class="sxs-lookup"><span data-stu-id="edd41-136">N</span></span>  <br/> |<span data-ttu-id="edd41-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="edd41-137">xsd:string</span></span>  <br/> |<span data-ttu-id="edd41-138">necesario</span><span class="sxs-lookup"><span data-stu-id="edd41-138">required</span></span>  <br/> ||<span data-ttu-id="edd41-139">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="edd41-139">Values of the xsd:string type.</span></span>  <br/> |
   

