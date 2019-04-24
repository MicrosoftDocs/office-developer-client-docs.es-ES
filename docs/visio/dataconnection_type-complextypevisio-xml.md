---
title: DataConnection_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 0253bf261868ec335bcc295c479cdfc98da79490
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344607"
---
# <a name="dataconnectiontype-complextype-visio-xml"></a><span data-ttu-id="a8f9c-102">DataConnection_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="a8f9c-102">DataConnection_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a8f9c-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="a8f9c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8f9c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a8f9c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a8f9c-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a8f9c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a8f9c-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="a8f9c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a8f9c-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="a8f9c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a8f9c-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="a8f9c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a8f9c-109">Definición</span><span class="sxs-lookup"><span data-stu-id="a8f9c-109">Definition</span></span>

```XML
      <xs:complexType name="DataConnection_Type">
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="FileName"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ConnectionString"
  type="xsd:string"
    />
    <xs:attribute name="Command"
  type="xsd:string"
    />
    <xs:attribute name="FriendlyName"
  type="xsd:string"
    />
    <xs:attribute name="Timeout"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="AlwaysUseConnectionFile"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a8f9c-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="a8f9c-110">Elements and attributes</span></span>

<span data-ttu-id="a8f9c-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="a8f9c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a8f9c-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a8f9c-112">Child elements</span></span>

<span data-ttu-id="a8f9c-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a8f9c-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a8f9c-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="a8f9c-114">Attributes</span></span>

|<span data-ttu-id="a8f9c-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="a8f9c-115">**Attribute**</span></span>|<span data-ttu-id="a8f9c-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a8f9c-116">**Type**</span></span>|<span data-ttu-id="a8f9c-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="a8f9c-117">**Required**</span></span>|<span data-ttu-id="a8f9c-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a8f9c-118">**Description**</span></span>|<span data-ttu-id="a8f9c-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="a8f9c-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a8f9c-120">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="a8f9c-120">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="a8f9c-121">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="a8f9c-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a8f9c-122">opcional</span><span class="sxs-lookup"><span data-stu-id="a8f9c-122">optional</span></span>  <br/> ||<span data-ttu-id="a8f9c-123">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="a8f9c-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a8f9c-124">Command</span><span class="sxs-lookup"><span data-stu-id="a8f9c-124">Command</span></span>  <br/> |<span data-ttu-id="a8f9c-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="a8f9c-125">xsd:string</span></span>  <br/> |<span data-ttu-id="a8f9c-126">opcional</span><span class="sxs-lookup"><span data-stu-id="a8f9c-126">optional</span></span>  <br/> ||<span data-ttu-id="a8f9c-127">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="a8f9c-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a8f9c-128">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="a8f9c-128">ConnectionString</span></span>  <br/> |<span data-ttu-id="a8f9c-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="a8f9c-129">xsd:string</span></span>  <br/> |<span data-ttu-id="a8f9c-130">opcional</span><span class="sxs-lookup"><span data-stu-id="a8f9c-130">optional</span></span>  <br/> ||<span data-ttu-id="a8f9c-131">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="a8f9c-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a8f9c-132">FileName</span><span class="sxs-lookup"><span data-stu-id="a8f9c-132">FileName</span></span>  <br/> |<span data-ttu-id="a8f9c-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="a8f9c-133">xsd:string</span></span>  <br/> |<span data-ttu-id="a8f9c-134">necesario</span><span class="sxs-lookup"><span data-stu-id="a8f9c-134">required</span></span>  <br/> ||<span data-ttu-id="a8f9c-135">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="a8f9c-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a8f9c-136">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a8f9c-136">FriendlyName</span></span>  <br/> |<span data-ttu-id="a8f9c-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="a8f9c-137">xsd:string</span></span>  <br/> |<span data-ttu-id="a8f9c-138">opcional</span><span class="sxs-lookup"><span data-stu-id="a8f9c-138">optional</span></span>  <br/> ||<span data-ttu-id="a8f9c-139">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="a8f9c-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a8f9c-140">ID</span><span class="sxs-lookup"><span data-stu-id="a8f9c-140">ID</span></span>  <br/> |<span data-ttu-id="a8f9c-141">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a8f9c-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a8f9c-142">necesario</span><span class="sxs-lookup"><span data-stu-id="a8f9c-142">required</span></span>  <br/> ||<span data-ttu-id="a8f9c-143">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a8f9c-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a8f9c-144">Timeout</span><span class="sxs-lookup"><span data-stu-id="a8f9c-144">Timeout</span></span>  <br/> |<span data-ttu-id="a8f9c-145">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a8f9c-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a8f9c-146">opcional</span><span class="sxs-lookup"><span data-stu-id="a8f9c-146">optional</span></span>  <br/> ||<span data-ttu-id="a8f9c-147">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a8f9c-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

