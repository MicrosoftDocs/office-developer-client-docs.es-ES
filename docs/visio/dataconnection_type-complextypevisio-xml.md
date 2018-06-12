---
title: DataConnection_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 3a900e22fd36c936f689081149b484bd5e7460fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821929"
---
# <a name="dataconnectiontype-complextype-visio-xml"></a><span data-ttu-id="e8bf1-102">DataConnection_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="e8bf1-102">DataConnection_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e8bf1-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="e8bf1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e8bf1-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e8bf1-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e8bf1-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="e8bf1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e8bf1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e8bf1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e8bf1-107">**Base de la extensión**</span><span class="sxs-lookup"><span data-stu-id="e8bf1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e8bf1-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e8bf1-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e8bf1-109">Definición</span><span class="sxs-lookup"><span data-stu-id="e8bf1-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="e8bf1-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="e8bf1-110">Elements and attributes</span></span>

<span data-ttu-id="e8bf1-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e8bf1-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e8bf1-112">Child elements</span></span>

<span data-ttu-id="e8bf1-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e8bf1-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="e8bf1-114">Attributes</span></span>

|<span data-ttu-id="e8bf1-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="e8bf1-115">**Attribute**</span></span>|<span data-ttu-id="e8bf1-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e8bf1-116">**Type**</span></span>|<span data-ttu-id="e8bf1-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="e8bf1-117">**Required**</span></span>|<span data-ttu-id="e8bf1-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e8bf1-118">**Description**</span></span>|<span data-ttu-id="e8bf1-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="e8bf1-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e8bf1-120">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="e8bf1-120">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="e8bf1-121">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="e8bf1-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e8bf1-122">opcional</span><span class="sxs-lookup"><span data-stu-id="e8bf1-122">optional</span></span>  <br/> ||<span data-ttu-id="e8bf1-123">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e8bf1-124">Comando</span><span class="sxs-lookup"><span data-stu-id="e8bf1-124">Command</span></span>  <br/> |<span data-ttu-id="e8bf1-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="e8bf1-125">xsd:string</span></span>  <br/> |<span data-ttu-id="e8bf1-126">opcional</span><span class="sxs-lookup"><span data-stu-id="e8bf1-126">optional</span></span>  <br/> ||<span data-ttu-id="e8bf1-127">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e8bf1-128">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="e8bf1-128">ConnectionString</span></span>  <br/> |<span data-ttu-id="e8bf1-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="e8bf1-129">xsd:string</span></span>  <br/> |<span data-ttu-id="e8bf1-130">opcional</span><span class="sxs-lookup"><span data-stu-id="e8bf1-130">optional</span></span>  <br/> ||<span data-ttu-id="e8bf1-131">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e8bf1-132">FileName</span><span class="sxs-lookup"><span data-stu-id="e8bf1-132">FileName</span></span>  <br/> |<span data-ttu-id="e8bf1-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="e8bf1-133">xsd:string</span></span>  <br/> |<span data-ttu-id="e8bf1-134">necesario</span><span class="sxs-lookup"><span data-stu-id="e8bf1-134">required</span></span>  <br/> ||<span data-ttu-id="e8bf1-135">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e8bf1-136">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e8bf1-136">FriendlyName</span></span>  <br/> |<span data-ttu-id="e8bf1-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="e8bf1-137">xsd:string</span></span>  <br/> |<span data-ttu-id="e8bf1-138">opcional</span><span class="sxs-lookup"><span data-stu-id="e8bf1-138">optional</span></span>  <br/> ||<span data-ttu-id="e8bf1-139">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e8bf1-140">id.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-140">ID</span></span>  <br/> |<span data-ttu-id="e8bf1-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e8bf1-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e8bf1-142">necesario</span><span class="sxs-lookup"><span data-stu-id="e8bf1-142">required</span></span>  <br/> ||<span data-ttu-id="e8bf1-143">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e8bf1-144">Timeout</span><span class="sxs-lookup"><span data-stu-id="e8bf1-144">Timeout</span></span>  <br/> |<span data-ttu-id="e8bf1-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e8bf1-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e8bf1-146">opcional</span><span class="sxs-lookup"><span data-stu-id="e8bf1-146">optional</span></span>  <br/> ||<span data-ttu-id="e8bf1-147">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

