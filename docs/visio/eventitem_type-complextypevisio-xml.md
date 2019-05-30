---
title: ComplexType EventItem_Type (XML de Visio)
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
# <a name="eventitemtype-complextype-visio-xml"></a><span data-ttu-id="30995-102">ComplexType EventItem_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="30995-102">EventItem_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="30995-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="30995-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30995-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="30995-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="30995-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="30995-105">**Schema file**</span></span> <br/> |<span data-ttu-id="30995-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="30995-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="30995-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="30995-107">**Extension base**</span></span> <br/> |<span data-ttu-id="30995-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="30995-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="30995-109">Definición</span><span class="sxs-lookup"><span data-stu-id="30995-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="30995-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="30995-110">Elements and attributes</span></span>

<span data-ttu-id="30995-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="30995-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="30995-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="30995-112">Child elements</span></span>

<span data-ttu-id="30995-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="30995-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="30995-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="30995-114">Attributes</span></span>

|<span data-ttu-id="30995-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="30995-115">**Attribute**</span></span>|<span data-ttu-id="30995-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="30995-116">**Type**</span></span>|<span data-ttu-id="30995-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="30995-117">**Required**</span></span>|<span data-ttu-id="30995-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="30995-118">**Description**</span></span>|<span data-ttu-id="30995-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="30995-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="30995-120">Acción</span><span class="sxs-lookup"><span data-stu-id="30995-120">Action</span></span>  <br/> |<span data-ttu-id="30995-121">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="30995-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="30995-122">necesario</span><span class="sxs-lookup"><span data-stu-id="30995-122">required</span></span>  <br/> ||<span data-ttu-id="30995-123">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="30995-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="30995-124">Habilitado</span><span class="sxs-lookup"><span data-stu-id="30995-124">Enabled</span></span>  <br/> |<span data-ttu-id="30995-125">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="30995-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="30995-126">opcional</span><span class="sxs-lookup"><span data-stu-id="30995-126">optional</span></span>  <br/> ||<span data-ttu-id="30995-127">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="30995-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="30995-128">EventCode</span><span class="sxs-lookup"><span data-stu-id="30995-128">EventCode</span></span>  <br/> |<span data-ttu-id="30995-129">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="30995-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="30995-130">necesario</span><span class="sxs-lookup"><span data-stu-id="30995-130">required</span></span>  <br/> ||<span data-ttu-id="30995-131">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="30995-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="30995-132">ID</span><span class="sxs-lookup"><span data-stu-id="30995-132">ID</span></span>  <br/> |<span data-ttu-id="30995-133">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="30995-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="30995-134">necesario</span><span class="sxs-lookup"><span data-stu-id="30995-134">required</span></span>  <br/> ||<span data-ttu-id="30995-135">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="30995-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="30995-136">Target</span><span class="sxs-lookup"><span data-stu-id="30995-136">Target</span></span>  <br/> |<span data-ttu-id="30995-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="30995-137">xsd:string</span></span>  <br/> |<span data-ttu-id="30995-138">necesario</span><span class="sxs-lookup"><span data-stu-id="30995-138">required</span></span>  <br/> ||<span data-ttu-id="30995-139">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="30995-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="30995-140">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="30995-140">TargetArgs</span></span>  <br/> |<span data-ttu-id="30995-141">xsd: String</span><span class="sxs-lookup"><span data-stu-id="30995-141">xsd:string</span></span>  <br/> |<span data-ttu-id="30995-142">necesario</span><span class="sxs-lookup"><span data-stu-id="30995-142">required</span></span>  <br/> ||<span data-ttu-id="30995-143">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="30995-143">Values of the xsd:string type.</span></span>  <br/> |
   

