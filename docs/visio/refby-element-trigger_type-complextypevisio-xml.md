---
title: Elemento de RefBy (Trigger_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Especifica una referencia a una página en el dibujo.
ms.openlocfilehash: 57ac63c4488b68d3af3c6e4a75417e2c7937723c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822914"
---
# <a name="refby-element-triggertype-complextype-visio-xml"></a><span data-ttu-id="7caaf-103">Elemento de RefBy (Trigger_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="7caaf-103">RefBy element (Trigger_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="7caaf-104">Especifica una referencia a una página en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="7caaf-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7caaf-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7caaf-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7caaf-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="7caaf-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7caaf-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="7caaf-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7caaf-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7caaf-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7caaf-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7caaf-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7caaf-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7caaf-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7caaf-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="7caaf-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="7caaf-112">Definición</span><span class="sxs-lookup"><span data-stu-id="7caaf-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7caaf-113">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="7caaf-113">Elements and attributes</span></span>

<span data-ttu-id="7caaf-114">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="7caaf-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7caaf-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7caaf-115">Parent elements</span></span>

|<span data-ttu-id="7caaf-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="7caaf-116">**Element**</span></span>|<span data-ttu-id="7caaf-117">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7caaf-117">**Type**</span></span>|<span data-ttu-id="7caaf-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7caaf-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7caaf-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="7caaf-119">Trigger</span></span>](http://msdn.microsoft.com/library/6dbd2c66-3b29-03f6-648f-723d359ded0d%28Office.15%29.aspx) <br/> |[<span data-ttu-id="7caaf-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="7caaf-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7caaf-121">Proporciona instrucciones para Microsoft Visio para volver a calcular una relación entre los elementos de documento en un archivo de Visio.</span><span class="sxs-lookup"><span data-stu-id="7caaf-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |
|[<span data-ttu-id="7caaf-122">Trigger</span><span class="sxs-lookup"><span data-stu-id="7caaf-122">Trigger</span></span>](http://msdn.microsoft.com/library/e4eeb238-f6d0-fb23-db1c-01d55b0a8d88%28Office.15%29.aspx) <br/> |[<span data-ttu-id="7caaf-123">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="7caaf-123">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7caaf-124">Proporciona instrucciones para Microsoft Visio para volver a calcular una relación entre los elementos de documento en un archivo de Visio.</span><span class="sxs-lookup"><span data-stu-id="7caaf-124">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |
|[<span data-ttu-id="7caaf-125">Trigger</span><span class="sxs-lookup"><span data-stu-id="7caaf-125">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="7caaf-126">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="7caaf-126">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7caaf-127">Proporciona instrucciones para Microsoft Visio para volver a calcular una relación entre los elementos de documento en un archivo de Visio.</span><span class="sxs-lookup"><span data-stu-id="7caaf-127">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7caaf-128">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7caaf-128">Child elements</span></span>

<span data-ttu-id="7caaf-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7caaf-129">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7caaf-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="7caaf-130">Attributes</span></span>

|<span data-ttu-id="7caaf-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="7caaf-131">**Attribute**</span></span>|<span data-ttu-id="7caaf-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7caaf-132">**Type**</span></span>|<span data-ttu-id="7caaf-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="7caaf-133">**Required**</span></span>|<span data-ttu-id="7caaf-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7caaf-134">**Description**</span></span>|<span data-ttu-id="7caaf-135">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="7caaf-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7caaf-136">id.</span><span class="sxs-lookup"><span data-stu-id="7caaf-136">ID</span></span>  <br/> |<span data-ttu-id="7caaf-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7caaf-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7caaf-138">necesario</span><span class="sxs-lookup"><span data-stu-id="7caaf-138">required</span></span>  <br/> |<span data-ttu-id="7caaf-139">Especifica el atributo de identificador de una página en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="7caaf-139">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="7caaf-140">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7caaf-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7caaf-141">T</span><span class="sxs-lookup"><span data-stu-id="7caaf-141">T</span></span>  <br/> |<span data-ttu-id="7caaf-142">xsd: String</span><span class="sxs-lookup"><span data-stu-id="7caaf-142">xsd:string</span></span>  <br/> |<span data-ttu-id="7caaf-143">necesario</span><span class="sxs-lookup"><span data-stu-id="7caaf-143">required</span></span>  <br/> |<span data-ttu-id="7caaf-144">Especifica el tipo de referencia.</span><span class="sxs-lookup"><span data-stu-id="7caaf-144">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="7caaf-145">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="7caaf-145">Values of the xsd:string type.</span></span>  <br/> |
   

