---
title: EventItem_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f157db03-e7d0-d39f-cbde-2a22f45b40ed
ms.openlocfilehash: f0fd618cc2a86d3695d0d6f6c446f118475ffc1f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541795"
---
# <a name="eventitem_type-complextype-visio-xml"></a><span data-ttu-id="52698-102">EventItem_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="52698-102">EventItem_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="52698-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="52698-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52698-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="52698-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="52698-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="52698-105">**Schema file**</span></span> <br/> |<span data-ttu-id="52698-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="52698-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="52698-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="52698-107">**Extension base**</span></span> <br/> |<span data-ttu-id="52698-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="52698-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="52698-109">Definición</span><span class="sxs-lookup"><span data-stu-id="52698-109">Definition</span></span>

```XML
      <xs:complexType name="EventItem_Type">
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Action"
  type="xsd:unsignedShort"
     use="required"
    />
    <xs:attribute name="EventCode"
  type="xsd:unsignedShort"
     use="required"
    />
    <xs:attribute name="Enabled"
  type="xsd:boolean"
    />
    <xs:attribute name="Target"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="TargetArgs"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="52698-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="52698-110">Elements and attributes</span></span>

<span data-ttu-id="52698-111">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="52698-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="52698-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="52698-112">Child elements</span></span>

<span data-ttu-id="52698-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="52698-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="52698-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="52698-114">Attributes</span></span>

|<span data-ttu-id="52698-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="52698-115">**Attribute**</span></span>|<span data-ttu-id="52698-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="52698-116">**Type**</span></span>|<span data-ttu-id="52698-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="52698-117">**Required**</span></span>|<span data-ttu-id="52698-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="52698-118">**Description**</span></span>|<span data-ttu-id="52698-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="52698-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="52698-120">Action</span><span class="sxs-lookup"><span data-stu-id="52698-120">Action</span></span>  <br/> |<span data-ttu-id="52698-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="52698-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="52698-122">necesario</span><span class="sxs-lookup"><span data-stu-id="52698-122">required</span></span>  <br/> ||<span data-ttu-id="52698-123">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="52698-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="52698-124">Habilitado</span><span class="sxs-lookup"><span data-stu-id="52698-124">Enabled</span></span>  <br/> |<span data-ttu-id="52698-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="52698-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="52698-126">opcional</span><span class="sxs-lookup"><span data-stu-id="52698-126">optional</span></span>  <br/> ||<span data-ttu-id="52698-127">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="52698-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="52698-128">EventCode</span><span class="sxs-lookup"><span data-stu-id="52698-128">EventCode</span></span>  <br/> |<span data-ttu-id="52698-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="52698-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="52698-130">necesario</span><span class="sxs-lookup"><span data-stu-id="52698-130">required</span></span>  <br/> ||<span data-ttu-id="52698-131">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="52698-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="52698-132">ID</span><span class="sxs-lookup"><span data-stu-id="52698-132">ID</span></span>  <br/> |<span data-ttu-id="52698-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="52698-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="52698-134">necesario</span><span class="sxs-lookup"><span data-stu-id="52698-134">required</span></span>  <br/> ||<span data-ttu-id="52698-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="52698-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="52698-136">Target</span><span class="sxs-lookup"><span data-stu-id="52698-136">Target</span></span>  <br/> |<span data-ttu-id="52698-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="52698-137">xsd:string</span></span>  <br/> |<span data-ttu-id="52698-138">necesario</span><span class="sxs-lookup"><span data-stu-id="52698-138">required</span></span>  <br/> ||<span data-ttu-id="52698-139">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="52698-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="52698-140">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="52698-140">TargetArgs</span></span>  <br/> |<span data-ttu-id="52698-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="52698-141">xsd:string</span></span>  <br/> |<span data-ttu-id="52698-142">necesario</span><span class="sxs-lookup"><span data-stu-id="52698-142">required</span></span>  <br/> ||<span data-ttu-id="52698-143">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="52698-143">Values of the xsd:string type.</span></span>  <br/> |
   

