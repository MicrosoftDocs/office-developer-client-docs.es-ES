---
title: StyleSheet_Type complexType (Visio XML)
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
# <a name="stylesheet_type-complextype-visio-xml"></a><span data-ttu-id="130fe-102">StyleSheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="130fe-102">StyleSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="130fe-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="130fe-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="130fe-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="130fe-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="130fe-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="130fe-105">**Schema file**</span></span> <br/> |<span data-ttu-id="130fe-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="130fe-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="130fe-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="130fe-107">**Extension base**</span></span> <br/> |<span data-ttu-id="130fe-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="130fe-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="130fe-109">Definición</span><span class="sxs-lookup"><span data-stu-id="130fe-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="130fe-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="130fe-110">Elements and attributes</span></span>

<span data-ttu-id="130fe-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="130fe-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="130fe-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="130fe-112">Child elements</span></span>

<span data-ttu-id="130fe-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="130fe-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="130fe-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="130fe-114">Attributes</span></span>

|<span data-ttu-id="130fe-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="130fe-115">**Attribute**</span></span>|<span data-ttu-id="130fe-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="130fe-116">**Type**</span></span>|<span data-ttu-id="130fe-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="130fe-117">**Required**</span></span>|<span data-ttu-id="130fe-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="130fe-118">**Description**</span></span>|<span data-ttu-id="130fe-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="130fe-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="130fe-120">ID</span><span class="sxs-lookup"><span data-stu-id="130fe-120">ID</span></span>  <br/> |<span data-ttu-id="130fe-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="130fe-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="130fe-122">necesario</span><span class="sxs-lookup"><span data-stu-id="130fe-122">required</span></span>  <br/> ||<span data-ttu-id="130fe-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="130fe-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="130fe-124">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="130fe-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="130fe-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="130fe-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="130fe-126">opcional</span><span class="sxs-lookup"><span data-stu-id="130fe-126">optional</span></span>  <br/> ||<span data-ttu-id="130fe-127">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="130fe-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="130fe-128">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="130fe-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="130fe-129">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="130fe-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="130fe-130">opcional</span><span class="sxs-lookup"><span data-stu-id="130fe-130">optional</span></span>  <br/> ||<span data-ttu-id="130fe-131">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="130fe-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="130fe-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="130fe-132">Name</span></span>  <br/> |<span data-ttu-id="130fe-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="130fe-133">xsd:string</span></span>  <br/> |<span data-ttu-id="130fe-134">opcional</span><span class="sxs-lookup"><span data-stu-id="130fe-134">optional</span></span>  <br/> ||<span data-ttu-id="130fe-135">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="130fe-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="130fe-136">NameU</span><span class="sxs-lookup"><span data-stu-id="130fe-136">NameU</span></span>  <br/> |<span data-ttu-id="130fe-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="130fe-137">xsd:string</span></span>  <br/> |<span data-ttu-id="130fe-138">opcional</span><span class="sxs-lookup"><span data-stu-id="130fe-138">optional</span></span>  <br/> ||<span data-ttu-id="130fe-139">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="130fe-139">Values of the xsd:string type.</span></span>  <br/> |
   

