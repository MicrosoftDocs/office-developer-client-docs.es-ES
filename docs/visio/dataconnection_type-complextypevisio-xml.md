---
title: DataConnection_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 0253bf261868ec335bcc295c479cdfc98da79490
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389144"
---
# <a name="dataconnectiontype-complextype-visio-xml"></a><span data-ttu-id="88b37-102">DataConnection_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="88b37-102">DataConnection_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="88b37-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="88b37-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88b37-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="88b37-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="88b37-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="88b37-105">**Schema file**</span></span> <br/> |<span data-ttu-id="88b37-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="88b37-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="88b37-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="88b37-107">**Extension base**</span></span> <br/> |<span data-ttu-id="88b37-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="88b37-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="88b37-109">Definición</span><span class="sxs-lookup"><span data-stu-id="88b37-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="88b37-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="88b37-110">Elements and attributes</span></span>

<span data-ttu-id="88b37-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="88b37-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="88b37-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="88b37-112">Child elements</span></span>

<span data-ttu-id="88b37-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="88b37-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="88b37-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="88b37-114">Attributes</span></span>

|<span data-ttu-id="88b37-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="88b37-115">**Attribute**</span></span>|<span data-ttu-id="88b37-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="88b37-116">**Type**</span></span>|<span data-ttu-id="88b37-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="88b37-117">**Required**</span></span>|<span data-ttu-id="88b37-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="88b37-118">**Description**</span></span>|<span data-ttu-id="88b37-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="88b37-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="88b37-120">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="88b37-120">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="88b37-121">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="88b37-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="88b37-122">opcional</span><span class="sxs-lookup"><span data-stu-id="88b37-122">optional</span></span>  <br/> ||<span data-ttu-id="88b37-123">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="88b37-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="88b37-124">Comando</span><span class="sxs-lookup"><span data-stu-id="88b37-124">Command</span></span>  <br/> |<span data-ttu-id="88b37-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="88b37-125">xsd:string</span></span>  <br/> |<span data-ttu-id="88b37-126">opcional</span><span class="sxs-lookup"><span data-stu-id="88b37-126">optional</span></span>  <br/> ||<span data-ttu-id="88b37-127">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="88b37-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="88b37-128">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="88b37-128">ConnectionString</span></span>  <br/> |<span data-ttu-id="88b37-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="88b37-129">xsd:string</span></span>  <br/> |<span data-ttu-id="88b37-130">opcional</span><span class="sxs-lookup"><span data-stu-id="88b37-130">optional</span></span>  <br/> ||<span data-ttu-id="88b37-131">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="88b37-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="88b37-132">FileName</span><span class="sxs-lookup"><span data-stu-id="88b37-132">FileName</span></span>  <br/> |<span data-ttu-id="88b37-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="88b37-133">xsd:string</span></span>  <br/> |<span data-ttu-id="88b37-134">necesario</span><span class="sxs-lookup"><span data-stu-id="88b37-134">required</span></span>  <br/> ||<span data-ttu-id="88b37-135">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="88b37-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="88b37-136">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="88b37-136">FriendlyName</span></span>  <br/> |<span data-ttu-id="88b37-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="88b37-137">xsd:string</span></span>  <br/> |<span data-ttu-id="88b37-138">opcional</span><span class="sxs-lookup"><span data-stu-id="88b37-138">optional</span></span>  <br/> ||<span data-ttu-id="88b37-139">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="88b37-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="88b37-140">ID</span><span class="sxs-lookup"><span data-stu-id="88b37-140">ID</span></span>  <br/> |<span data-ttu-id="88b37-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="88b37-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="88b37-142">necesario</span><span class="sxs-lookup"><span data-stu-id="88b37-142">required</span></span>  <br/> ||<span data-ttu-id="88b37-143">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="88b37-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="88b37-144">Timeout</span><span class="sxs-lookup"><span data-stu-id="88b37-144">Timeout</span></span>  <br/> |<span data-ttu-id="88b37-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="88b37-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="88b37-146">opcional</span><span class="sxs-lookup"><span data-stu-id="88b37-146">optional</span></span>  <br/> ||<span data-ttu-id="88b37-147">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="88b37-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

