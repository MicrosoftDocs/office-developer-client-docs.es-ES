---
title: Cell_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 38519bac-ce3e-9ded-d024-93dd7f34b107
ms.openlocfilehash: 4e0cedaab755dab669d79ff52742b8ac2b9f9725
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542306"
---
# <a name="cell_type-complextype-visio-xml"></a><span data-ttu-id="9f5ab-102">Cell_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9f5ab-102">Cell_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="9f5ab-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="9f5ab-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9f5ab-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9f5ab-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9f5ab-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9f5ab-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9f5ab-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9f5ab-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9f5ab-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="9f5ab-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9f5ab-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9f5ab-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9f5ab-109">Definición</span><span class="sxs-lookup"><span data-stu-id="9f5ab-109">Definition</span></span>

```XML
          <xs:complexType name="Cell_Type">
          
          <xs:sequence>
    <xs:element name="RefBy"  type="RefBy_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="U"
  type="xsd:string"
    />
    <xs:attribute name="E"
  type="xsd:string"
    />
    <xs:attribute name="F"
  type="xsd:string"
    />
    <xs:attribute name="V"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9f5ab-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="9f5ab-110">Elements and attributes</span></span>

<span data-ttu-id="9f5ab-111">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="9f5ab-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9f5ab-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9f5ab-112">Child elements</span></span>

|<span data-ttu-id="9f5ab-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9f5ab-113">**Element**</span></span>|<span data-ttu-id="9f5ab-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9f5ab-114">**Type**</span></span>|<span data-ttu-id="9f5ab-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9f5ab-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9f5ab-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="9f5ab-116">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9f5ab-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="9f5ab-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9f5ab-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="9f5ab-118">Attributes</span></span>

|<span data-ttu-id="9f5ab-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="9f5ab-119">**Attribute**</span></span>|<span data-ttu-id="9f5ab-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9f5ab-120">**Type**</span></span>|<span data-ttu-id="9f5ab-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="9f5ab-121">**Required**</span></span>|<span data-ttu-id="9f5ab-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9f5ab-122">**Description**</span></span>|<span data-ttu-id="9f5ab-123">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="9f5ab-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9f5ab-124">E</span><span class="sxs-lookup"><span data-stu-id="9f5ab-124">E</span></span>  <br/> |<span data-ttu-id="9f5ab-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9f5ab-125">xsd:string</span></span>  <br/> |<span data-ttu-id="9f5ab-126">opcional</span><span class="sxs-lookup"><span data-stu-id="9f5ab-126">optional</span></span>  <br/> ||<span data-ttu-id="9f5ab-127">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9f5ab-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9f5ab-128">F</span><span class="sxs-lookup"><span data-stu-id="9f5ab-128">F</span></span>  <br/> |<span data-ttu-id="9f5ab-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9f5ab-129">xsd:string</span></span>  <br/> |<span data-ttu-id="9f5ab-130">opcional</span><span class="sxs-lookup"><span data-stu-id="9f5ab-130">optional</span></span>  <br/> ||<span data-ttu-id="9f5ab-131">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9f5ab-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9f5ab-132">N</span><span class="sxs-lookup"><span data-stu-id="9f5ab-132">N</span></span>  <br/> |<span data-ttu-id="9f5ab-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9f5ab-133">xsd:string</span></span>  <br/> |<span data-ttu-id="9f5ab-134">necesario</span><span class="sxs-lookup"><span data-stu-id="9f5ab-134">required</span></span>  <br/> ||<span data-ttu-id="9f5ab-135">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9f5ab-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9f5ab-136">U</span><span class="sxs-lookup"><span data-stu-id="9f5ab-136">U</span></span>  <br/> |<span data-ttu-id="9f5ab-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9f5ab-137">xsd:string</span></span>  <br/> |<span data-ttu-id="9f5ab-138">opcional</span><span class="sxs-lookup"><span data-stu-id="9f5ab-138">optional</span></span>  <br/> ||<span data-ttu-id="9f5ab-139">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9f5ab-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9f5ab-140">V</span><span class="sxs-lookup"><span data-stu-id="9f5ab-140">V</span></span>  <br/> |<span data-ttu-id="9f5ab-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9f5ab-141">xsd:string</span></span>  <br/> |<span data-ttu-id="9f5ab-142">opcional</span><span class="sxs-lookup"><span data-stu-id="9f5ab-142">optional</span></span>  <br/> ||<span data-ttu-id="9f5ab-143">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9f5ab-143">Values of the xsd:string type.</span></span>  <br/> |
   

