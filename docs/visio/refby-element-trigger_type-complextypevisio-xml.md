---
title: Elemento de RefBy (Trigger_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Especifica una referencia a una página en el dibujo.
ms.openlocfilehash: e4726a8fe49a7492cd2f7833bbcf5e6810bae18d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572434"
---
# <a name="refby-element-triggertype-complextype-visio-xml"></a><span data-ttu-id="a93d8-103">Elemento de RefBy (Trigger_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="a93d8-103">RefBy element (Trigger_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a93d8-104">Especifica una referencia a una página en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="a93d8-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a93d8-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a93d8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a93d8-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="a93d8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a93d8-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="a93d8-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a93d8-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a93d8-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a93d8-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a93d8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a93d8-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a93d8-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a93d8-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="a93d8-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="a93d8-112">Definición</span><span class="sxs-lookup"><span data-stu-id="a93d8-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a93d8-113">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="a93d8-113">Elements and attributes</span></span>

<span data-ttu-id="a93d8-114">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="a93d8-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a93d8-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a93d8-115">Parent elements</span></span>

|<span data-ttu-id="a93d8-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="a93d8-116">**Element**</span></span>|<span data-ttu-id="a93d8-117">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a93d8-117">**Type**</span></span>|<span data-ttu-id="a93d8-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a93d8-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a93d8-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="a93d8-119">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="a93d8-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="a93d8-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a93d8-121">Proporciona instrucciones para Microsoft Visio para volver a calcular una relación entre los elementos de documento en un archivo de Visio.</span><span class="sxs-lookup"><span data-stu-id="a93d8-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |

   
### <a name="child-elements"></a><span data-ttu-id="a93d8-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a93d8-122">Child elements</span></span>

<span data-ttu-id="a93d8-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a93d8-123">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a93d8-124">Atributos</span><span class="sxs-lookup"><span data-stu-id="a93d8-124">Attributes</span></span>

|<span data-ttu-id="a93d8-125">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="a93d8-125">**Attribute**</span></span>|<span data-ttu-id="a93d8-126">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a93d8-126">**Type**</span></span>|<span data-ttu-id="a93d8-127">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="a93d8-127">**Required**</span></span>|<span data-ttu-id="a93d8-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a93d8-128">**Description**</span></span>|<span data-ttu-id="a93d8-129">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="a93d8-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a93d8-130">ID</span><span class="sxs-lookup"><span data-stu-id="a93d8-130">ID</span></span>  <br/> |<span data-ttu-id="a93d8-131">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a93d8-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a93d8-132">necesario</span><span class="sxs-lookup"><span data-stu-id="a93d8-132">required</span></span>  <br/> |<span data-ttu-id="a93d8-133">Especifica el atributo de identificador de una página en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="a93d8-133">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="a93d8-134">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a93d8-134">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a93d8-135">T</span><span class="sxs-lookup"><span data-stu-id="a93d8-135">T</span></span>  <br/> |<span data-ttu-id="a93d8-136">xsd: String</span><span class="sxs-lookup"><span data-stu-id="a93d8-136">xsd:string</span></span>  <br/> |<span data-ttu-id="a93d8-137">necesario</span><span class="sxs-lookup"><span data-stu-id="a93d8-137">required</span></span>  <br/> |<span data-ttu-id="a93d8-138">Especifica el tipo de referencia.</span><span class="sxs-lookup"><span data-stu-id="a93d8-138">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="a93d8-139">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="a93d8-139">Values of the xsd:string type.</span></span>  <br/> |
   

