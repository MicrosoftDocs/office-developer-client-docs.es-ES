---
title: ComplexType DocumentSheet_Type (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 57af2ed5-7d89-9538-e51b-0bc70f067b40
ms.openlocfilehash: 18e7f064b1b6c9ac8e084c96011c1b18a646aecb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540010"
---
# <a name="documentsheettype-complextype-visio-xml"></a><span data-ttu-id="cf7b0-102">ComplexType DocumentSheet_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="cf7b0-102">DocumentSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="cf7b0-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="cf7b0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cf7b0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cf7b0-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cf7b0-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="cf7b0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cf7b0-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="cf7b0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cf7b0-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="cf7b0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cf7b0-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="cf7b0-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cf7b0-109">Definición</span><span class="sxs-lookup"><span data-stu-id="cf7b0-109">Definition</span></span>

```XML
      <xs:complexType name="DocumentSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cf7b0-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="cf7b0-110">Elements and attributes</span></span>

<span data-ttu-id="cf7b0-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="cf7b0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cf7b0-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cf7b0-112">Child elements</span></span>

<span data-ttu-id="cf7b0-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cf7b0-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cf7b0-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="cf7b0-114">Attributes</span></span>

|<span data-ttu-id="cf7b0-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="cf7b0-115">**Attribute**</span></span>|<span data-ttu-id="cf7b0-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cf7b0-116">**Type**</span></span>|<span data-ttu-id="cf7b0-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="cf7b0-117">**Required**</span></span>|<span data-ttu-id="cf7b0-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cf7b0-118">**Description**</span></span>|<span data-ttu-id="cf7b0-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="cf7b0-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cf7b0-120">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="cf7b0-120">IsCustomName</span></span>  <br/> |<span data-ttu-id="cf7b0-121">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="cf7b0-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="cf7b0-122">opcional</span><span class="sxs-lookup"><span data-stu-id="cf7b0-122">optional</span></span>  <br/> ||<span data-ttu-id="cf7b0-123">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="cf7b0-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="cf7b0-124">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="cf7b0-124">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="cf7b0-125">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="cf7b0-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="cf7b0-126">opcional</span><span class="sxs-lookup"><span data-stu-id="cf7b0-126">optional</span></span>  <br/> ||<span data-ttu-id="cf7b0-127">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="cf7b0-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="cf7b0-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="cf7b0-128">Name</span></span>  <br/> |<span data-ttu-id="cf7b0-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="cf7b0-129">xsd:string</span></span>  <br/> |<span data-ttu-id="cf7b0-130">opcional</span><span class="sxs-lookup"><span data-stu-id="cf7b0-130">optional</span></span>  <br/> ||<span data-ttu-id="cf7b0-131">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="cf7b0-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cf7b0-132">NameU</span><span class="sxs-lookup"><span data-stu-id="cf7b0-132">NameU</span></span>  <br/> |<span data-ttu-id="cf7b0-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="cf7b0-133">xsd:string</span></span>  <br/> |<span data-ttu-id="cf7b0-134">opcional</span><span class="sxs-lookup"><span data-stu-id="cf7b0-134">optional</span></span>  <br/> ||<span data-ttu-id="cf7b0-135">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="cf7b0-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cf7b0-136">UniqueID</span><span class="sxs-lookup"><span data-stu-id="cf7b0-136">UniqueID</span></span>  <br/> |<span data-ttu-id="cf7b0-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="cf7b0-137">xsd:string</span></span>  <br/> |<span data-ttu-id="cf7b0-138">opcional</span><span class="sxs-lookup"><span data-stu-id="cf7b0-138">optional</span></span>  <br/> ||<span data-ttu-id="cf7b0-139">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="cf7b0-139">Values of the xsd:string type.</span></span>  <br/> |
   

