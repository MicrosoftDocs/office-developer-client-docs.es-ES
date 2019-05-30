---
title: ComplexType StyleSheet_Type (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 06a02d07-920e-7d47-d63a-da3596cf20f6
ms.openlocfilehash: 6dcb6bbfd01c37b499dfca4d54d6cb0832e59b5a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541984"
---
# <a name="stylesheettype-complextype-visio-xml"></a><span data-ttu-id="e6131-102">ComplexType StyleSheet_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="e6131-102">StyleSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="e6131-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="e6131-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e6131-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e6131-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e6131-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="e6131-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e6131-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="e6131-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e6131-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="e6131-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e6131-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="e6131-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e6131-109">Definición</span><span class="sxs-lookup"><span data-stu-id="e6131-109">Definition</span></span>

```XML
      <xs:complexType name="StyleSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
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
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e6131-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="e6131-110">Elements and attributes</span></span>

<span data-ttu-id="e6131-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="e6131-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e6131-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e6131-112">Child elements</span></span>

<span data-ttu-id="e6131-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e6131-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e6131-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="e6131-114">Attributes</span></span>

|<span data-ttu-id="e6131-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="e6131-115">**Attribute**</span></span>|<span data-ttu-id="e6131-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e6131-116">**Type**</span></span>|<span data-ttu-id="e6131-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="e6131-117">**Required**</span></span>|<span data-ttu-id="e6131-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e6131-118">**Description**</span></span>|<span data-ttu-id="e6131-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="e6131-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e6131-120">ID</span><span class="sxs-lookup"><span data-stu-id="e6131-120">ID</span></span>  <br/> |<span data-ttu-id="e6131-121">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e6131-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e6131-122">necesario</span><span class="sxs-lookup"><span data-stu-id="e6131-122">required</span></span>  <br/> ||<span data-ttu-id="e6131-123">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e6131-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e6131-124">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="e6131-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="e6131-125">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="e6131-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e6131-126">opcional</span><span class="sxs-lookup"><span data-stu-id="e6131-126">optional</span></span>  <br/> ||<span data-ttu-id="e6131-127">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="e6131-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e6131-128">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="e6131-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="e6131-129">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="e6131-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e6131-130">opcional</span><span class="sxs-lookup"><span data-stu-id="e6131-130">optional</span></span>  <br/> ||<span data-ttu-id="e6131-131">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="e6131-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e6131-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="e6131-132">Name</span></span>  <br/> |<span data-ttu-id="e6131-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="e6131-133">xsd:string</span></span>  <br/> |<span data-ttu-id="e6131-134">opcional</span><span class="sxs-lookup"><span data-stu-id="e6131-134">optional</span></span>  <br/> ||<span data-ttu-id="e6131-135">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="e6131-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e6131-136">NameU</span><span class="sxs-lookup"><span data-stu-id="e6131-136">NameU</span></span>  <br/> |<span data-ttu-id="e6131-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="e6131-137">xsd:string</span></span>  <br/> |<span data-ttu-id="e6131-138">opcional</span><span class="sxs-lookup"><span data-stu-id="e6131-138">optional</span></span>  <br/> ||<span data-ttu-id="e6131-139">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="e6131-139">Values of the xsd:string type.</span></span>  <br/> |
   

