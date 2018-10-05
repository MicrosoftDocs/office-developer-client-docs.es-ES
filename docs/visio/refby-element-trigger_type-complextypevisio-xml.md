---
title: Elemento de RefBy (Trigger_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Especifica una referencia a una página en el dibujo.
ms.openlocfilehash: d987825345b64bd6e202970fc786aedaf49c6a94
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383320"
---
# <a name="refby-element-triggertype-complextype-visio-xml"></a><span data-ttu-id="6b823-103">Elemento de RefBy (Trigger_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="6b823-103">RefBy element (Trigger_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="6b823-104">Especifica una referencia a una página en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="6b823-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6b823-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6b823-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b823-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="6b823-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6b823-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="6b823-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6b823-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6b823-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6b823-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6b823-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6b823-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6b823-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6b823-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="6b823-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="6b823-112">Definición</span><span class="sxs-lookup"><span data-stu-id="6b823-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6b823-113">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="6b823-113">Elements and attributes</span></span>

<span data-ttu-id="6b823-114">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="6b823-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6b823-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6b823-115">Parent elements</span></span>

|<span data-ttu-id="6b823-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="6b823-116">**Element**</span></span>|<span data-ttu-id="6b823-117">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6b823-117">**Type**</span></span>|<span data-ttu-id="6b823-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6b823-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6b823-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="6b823-119">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="6b823-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="6b823-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6b823-121">Proporciona instrucciones para Microsoft Visio para volver a calcular una relación entre los elementos de documento en un archivo de Visio.</span><span class="sxs-lookup"><span data-stu-id="6b823-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |

   
### <a name="child-elements"></a><span data-ttu-id="6b823-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6b823-122">Child elements</span></span>

<span data-ttu-id="6b823-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6b823-123">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6b823-124">Atributos</span><span class="sxs-lookup"><span data-stu-id="6b823-124">Attributes</span></span>

|<span data-ttu-id="6b823-125">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="6b823-125">**Attribute**</span></span>|<span data-ttu-id="6b823-126">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6b823-126">**Type**</span></span>|<span data-ttu-id="6b823-127">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="6b823-127">**Required**</span></span>|<span data-ttu-id="6b823-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6b823-128">**Description**</span></span>|<span data-ttu-id="6b823-129">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="6b823-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6b823-130">ID</span><span class="sxs-lookup"><span data-stu-id="6b823-130">ID</span></span>  <br/> |<span data-ttu-id="6b823-131">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6b823-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6b823-132">necesario</span><span class="sxs-lookup"><span data-stu-id="6b823-132">required</span></span>  <br/> |<span data-ttu-id="6b823-133">Especifica el atributo de identificador de una página en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="6b823-133">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="6b823-134">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6b823-134">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6b823-135">T</span><span class="sxs-lookup"><span data-stu-id="6b823-135">T</span></span>  <br/> |<span data-ttu-id="6b823-136">xsd: String</span><span class="sxs-lookup"><span data-stu-id="6b823-136">xsd:string</span></span>  <br/> |<span data-ttu-id="6b823-137">necesario</span><span class="sxs-lookup"><span data-stu-id="6b823-137">required</span></span>  <br/> |<span data-ttu-id="6b823-138">Especifica el tipo de referencia.</span><span class="sxs-lookup"><span data-stu-id="6b823-138">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="6b823-139">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="6b823-139">Values of the xsd:string type.</span></span>  <br/> |
   

