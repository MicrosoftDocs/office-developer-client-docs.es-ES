---
title: Cell_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 38519bac-ce3e-9ded-d024-93dd7f34b107
ms.openlocfilehash: ae5f481d787ae5d07968df8cd0ef0eba6af26f9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327121"
---
# <a name="celltype-complextype-visio-xml"></a><span data-ttu-id="0d1b2-102">Cell_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="0d1b2-102">Cell_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0d1b2-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="0d1b2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d1b2-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0d1b2-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0d1b2-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="0d1b2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0d1b2-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0d1b2-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="0d1b2-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0d1b2-109">Definición</span><span class="sxs-lookup"><span data-stu-id="0d1b2-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0d1b2-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="0d1b2-110">Elements and attributes</span></span>

<span data-ttu-id="0d1b2-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0d1b2-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0d1b2-112">Child elements</span></span>

|<span data-ttu-id="0d1b2-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-113">**Element**</span></span>|<span data-ttu-id="0d1b2-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-114">**Type**</span></span>|<span data-ttu-id="0d1b2-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0d1b2-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="0d1b2-116">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0d1b2-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="0d1b2-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0d1b2-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="0d1b2-118">Attributes</span></span>

|<span data-ttu-id="0d1b2-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-119">**Attribute**</span></span>|<span data-ttu-id="0d1b2-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-120">**Type**</span></span>|<span data-ttu-id="0d1b2-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-121">**Required**</span></span>|<span data-ttu-id="0d1b2-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-122">**Description**</span></span>|<span data-ttu-id="0d1b2-123">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0d1b2-124">E</span><span class="sxs-lookup"><span data-stu-id="0d1b2-124">E</span></span>  <br/> |<span data-ttu-id="0d1b2-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0d1b2-125">xsd:string</span></span>  <br/> |<span data-ttu-id="0d1b2-126">opcional</span><span class="sxs-lookup"><span data-stu-id="0d1b2-126">optional</span></span>  <br/> ||<span data-ttu-id="0d1b2-127">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0d1b2-128">F</span><span class="sxs-lookup"><span data-stu-id="0d1b2-128">F</span></span>  <br/> |<span data-ttu-id="0d1b2-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0d1b2-129">xsd:string</span></span>  <br/> |<span data-ttu-id="0d1b2-130">opcional</span><span class="sxs-lookup"><span data-stu-id="0d1b2-130">optional</span></span>  <br/> ||<span data-ttu-id="0d1b2-131">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0d1b2-132">N</span><span class="sxs-lookup"><span data-stu-id="0d1b2-132">N</span></span>  <br/> |<span data-ttu-id="0d1b2-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0d1b2-133">xsd:string</span></span>  <br/> |<span data-ttu-id="0d1b2-134">necesario</span><span class="sxs-lookup"><span data-stu-id="0d1b2-134">required</span></span>  <br/> ||<span data-ttu-id="0d1b2-135">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0d1b2-136">U</span><span class="sxs-lookup"><span data-stu-id="0d1b2-136">U</span></span>  <br/> |<span data-ttu-id="0d1b2-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0d1b2-137">xsd:string</span></span>  <br/> |<span data-ttu-id="0d1b2-138">opcional</span><span class="sxs-lookup"><span data-stu-id="0d1b2-138">optional</span></span>  <br/> ||<span data-ttu-id="0d1b2-139">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0d1b2-140">V</span><span class="sxs-lookup"><span data-stu-id="0d1b2-140">V</span></span>  <br/> |<span data-ttu-id="0d1b2-141">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0d1b2-141">xsd:string</span></span>  <br/> |<span data-ttu-id="0d1b2-142">opcional</span><span class="sxs-lookup"><span data-stu-id="0d1b2-142">optional</span></span>  <br/> ||<span data-ttu-id="0d1b2-143">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-143">Values of the xsd:string type.</span></span>  <br/> |
   

