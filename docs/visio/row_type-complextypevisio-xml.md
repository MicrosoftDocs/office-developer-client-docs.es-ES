---
title: ComplexType Row_Type (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5e5c420e-f384-7b62-c862-35aea16e6d55
ms.openlocfilehash: d728363e6a3e7cd7fca2b95d91469f0d50ae1c39
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538161"
---
# <a name="rowtype-complextype-visio-xml"></a><span data-ttu-id="70a06-102">ComplexType Row_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="70a06-102">Row_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="70a06-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="70a06-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="70a06-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="70a06-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="70a06-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="70a06-105">**Schema file**</span></span> <br/> |<span data-ttu-id="70a06-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="70a06-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="70a06-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="70a06-107">**Extension base**</span></span> <br/> |<span data-ttu-id="70a06-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="70a06-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="70a06-109">Definición</span><span class="sxs-lookup"><span data-stu-id="70a06-109">Definition</span></span>

```XML
          <xs:complexType name="Row_Type">
          
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
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
    />
    <xs:attribute name="LocalName"
  type="xsd:string"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="T"
  type="xsd:string"
    />
    <xs:attribute name="Del"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="70a06-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="70a06-110">Elements and attributes</span></span>

<span data-ttu-id="70a06-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="70a06-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="70a06-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="70a06-112">Child elements</span></span>

|<span data-ttu-id="70a06-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="70a06-113">**Element**</span></span>|<span data-ttu-id="70a06-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="70a06-114">**Type**</span></span>|<span data-ttu-id="70a06-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="70a06-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="70a06-116">Cell</span><span class="sxs-lookup"><span data-stu-id="70a06-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="70a06-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="70a06-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="70a06-118">Trigger</span><span class="sxs-lookup"><span data-stu-id="70a06-118">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="70a06-119">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="70a06-119">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="70a06-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="70a06-120">Attributes</span></span>

|<span data-ttu-id="70a06-121">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="70a06-121">**Attribute**</span></span>|<span data-ttu-id="70a06-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="70a06-122">**Type**</span></span>|<span data-ttu-id="70a06-123">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="70a06-123">**Required**</span></span>|<span data-ttu-id="70a06-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="70a06-124">**Description**</span></span>|<span data-ttu-id="70a06-125">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="70a06-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="70a06-126">Del</span><span class="sxs-lookup"><span data-stu-id="70a06-126">Del</span></span>  <br/> |<span data-ttu-id="70a06-127">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="70a06-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="70a06-128">opcional</span><span class="sxs-lookup"><span data-stu-id="70a06-128">optional</span></span>  <br/> ||<span data-ttu-id="70a06-129">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="70a06-129">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="70a06-130">IX</span><span class="sxs-lookup"><span data-stu-id="70a06-130">IX</span></span>  <br/> |<span data-ttu-id="70a06-131">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="70a06-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="70a06-132">opcional</span><span class="sxs-lookup"><span data-stu-id="70a06-132">optional</span></span>  <br/> ||<span data-ttu-id="70a06-133">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="70a06-133">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="70a06-134">LocalName</span><span class="sxs-lookup"><span data-stu-id="70a06-134">LocalName</span></span>  <br/> |<span data-ttu-id="70a06-135">xsd: String</span><span class="sxs-lookup"><span data-stu-id="70a06-135">xsd:string</span></span>  <br/> |<span data-ttu-id="70a06-136">opcional</span><span class="sxs-lookup"><span data-stu-id="70a06-136">optional</span></span>  <br/> ||<span data-ttu-id="70a06-137">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="70a06-137">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="70a06-138">N</span><span class="sxs-lookup"><span data-stu-id="70a06-138">N</span></span>  <br/> |<span data-ttu-id="70a06-139">xsd: String</span><span class="sxs-lookup"><span data-stu-id="70a06-139">xsd:string</span></span>  <br/> |<span data-ttu-id="70a06-140">opcional</span><span class="sxs-lookup"><span data-stu-id="70a06-140">optional</span></span>  <br/> ||<span data-ttu-id="70a06-141">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="70a06-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="70a06-142">T</span><span class="sxs-lookup"><span data-stu-id="70a06-142">T</span></span>  <br/> |<span data-ttu-id="70a06-143">xsd: String</span><span class="sxs-lookup"><span data-stu-id="70a06-143">xsd:string</span></span>  <br/> |<span data-ttu-id="70a06-144">opcional</span><span class="sxs-lookup"><span data-stu-id="70a06-144">optional</span></span>  <br/> ||<span data-ttu-id="70a06-145">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="70a06-145">Values of the xsd:string type.</span></span>  <br/> |
   

