---
title: DataConnection_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 44dceee9a9ef43557e9bc02828f91c2c29d345d6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539652"
---
# <a name="dataconnection_type-complextype-visio-xml"></a><span data-ttu-id="bfacd-102">DataConnection_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="bfacd-102">DataConnection_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="bfacd-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="bfacd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bfacd-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bfacd-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bfacd-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="bfacd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bfacd-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bfacd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bfacd-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="bfacd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bfacd-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="bfacd-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bfacd-109">Definición</span><span class="sxs-lookup"><span data-stu-id="bfacd-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="bfacd-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="bfacd-110">Elements and attributes</span></span>

<span data-ttu-id="bfacd-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="bfacd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bfacd-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bfacd-112">Child elements</span></span>

<span data-ttu-id="bfacd-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bfacd-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bfacd-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="bfacd-114">Attributes</span></span>

|<span data-ttu-id="bfacd-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="bfacd-115">**Attribute**</span></span>|<span data-ttu-id="bfacd-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="bfacd-116">**Type**</span></span>|<span data-ttu-id="bfacd-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="bfacd-117">**Required**</span></span>|<span data-ttu-id="bfacd-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bfacd-118">**Description**</span></span>|<span data-ttu-id="bfacd-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="bfacd-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bfacd-120">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="bfacd-120">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="bfacd-121">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="bfacd-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="bfacd-122">opcional</span><span class="sxs-lookup"><span data-stu-id="bfacd-122">optional</span></span>  <br/> ||<span data-ttu-id="bfacd-123">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="bfacd-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="bfacd-124">Comando</span><span class="sxs-lookup"><span data-stu-id="bfacd-124">Command</span></span>  <br/> |<span data-ttu-id="bfacd-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="bfacd-125">xsd:string</span></span>  <br/> |<span data-ttu-id="bfacd-126">opcional</span><span class="sxs-lookup"><span data-stu-id="bfacd-126">optional</span></span>  <br/> ||<span data-ttu-id="bfacd-127">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="bfacd-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bfacd-128">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="bfacd-128">ConnectionString</span></span>  <br/> |<span data-ttu-id="bfacd-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="bfacd-129">xsd:string</span></span>  <br/> |<span data-ttu-id="bfacd-130">opcional</span><span class="sxs-lookup"><span data-stu-id="bfacd-130">optional</span></span>  <br/> ||<span data-ttu-id="bfacd-131">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="bfacd-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bfacd-132">FileName</span><span class="sxs-lookup"><span data-stu-id="bfacd-132">FileName</span></span>  <br/> |<span data-ttu-id="bfacd-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="bfacd-133">xsd:string</span></span>  <br/> |<span data-ttu-id="bfacd-134">necesario</span><span class="sxs-lookup"><span data-stu-id="bfacd-134">required</span></span>  <br/> ||<span data-ttu-id="bfacd-135">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="bfacd-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bfacd-136">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="bfacd-136">FriendlyName</span></span>  <br/> |<span data-ttu-id="bfacd-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="bfacd-137">xsd:string</span></span>  <br/> |<span data-ttu-id="bfacd-138">opcional</span><span class="sxs-lookup"><span data-stu-id="bfacd-138">optional</span></span>  <br/> ||<span data-ttu-id="bfacd-139">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="bfacd-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bfacd-140">ID</span><span class="sxs-lookup"><span data-stu-id="bfacd-140">ID</span></span>  <br/> |<span data-ttu-id="bfacd-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bfacd-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bfacd-142">necesario</span><span class="sxs-lookup"><span data-stu-id="bfacd-142">required</span></span>  <br/> ||<span data-ttu-id="bfacd-143">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bfacd-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bfacd-144">Timeout</span><span class="sxs-lookup"><span data-stu-id="bfacd-144">Timeout</span></span>  <br/> |<span data-ttu-id="bfacd-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bfacd-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bfacd-146">opcional</span><span class="sxs-lookup"><span data-stu-id="bfacd-146">optional</span></span>  <br/> ||<span data-ttu-id="bfacd-147">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bfacd-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

