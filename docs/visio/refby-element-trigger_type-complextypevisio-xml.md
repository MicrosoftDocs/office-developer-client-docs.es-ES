---
title: Elemento RefBy (Trigger_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Especifica una referencia a una página del dibujo.
ms.openlocfilehash: 6d081ad1bf9e089a16820db33cec92694db7ac98
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538294"
---
# <a name="refby-element-trigger_type-complextype-visio-xml"></a><span data-ttu-id="64563-103">Elemento RefBy (Trigger_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="64563-103">RefBy element (Trigger_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="64563-104">Especifica una referencia a una página del dibujo.</span><span class="sxs-lookup"><span data-stu-id="64563-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="64563-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="64563-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="64563-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="64563-106">**Element type**</span></span> <br/> |[<span data-ttu-id="64563-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="64563-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="64563-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="64563-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="64563-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="64563-109">**Schema file**</span></span> <br/> |<span data-ttu-id="64563-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="64563-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="64563-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="64563-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="64563-112">Definición</span><span class="sxs-lookup"><span data-stu-id="64563-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="64563-113">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="64563-113">Elements and attributes</span></span>

<span data-ttu-id="64563-114">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="64563-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="64563-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="64563-115">Parent elements</span></span>

|<span data-ttu-id="64563-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="64563-116">**Element**</span></span>|<span data-ttu-id="64563-117">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="64563-117">**Type**</span></span>|<span data-ttu-id="64563-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="64563-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="64563-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="64563-119">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="64563-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="64563-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="64563-121">Proporciona instrucciones a Microsoft Visio para volver a calcular una relación entre elementos de documento en un Visio archivo.</span><span class="sxs-lookup"><span data-stu-id="64563-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |

   
### <a name="child-elements"></a><span data-ttu-id="64563-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="64563-122">Child elements</span></span>

<span data-ttu-id="64563-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="64563-123">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="64563-124">Atributos</span><span class="sxs-lookup"><span data-stu-id="64563-124">Attributes</span></span>

|<span data-ttu-id="64563-125">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="64563-125">**Attribute**</span></span>|<span data-ttu-id="64563-126">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="64563-126">**Type**</span></span>|<span data-ttu-id="64563-127">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="64563-127">**Required**</span></span>|<span data-ttu-id="64563-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="64563-128">**Description**</span></span>|<span data-ttu-id="64563-129">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="64563-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="64563-130">ID</span><span class="sxs-lookup"><span data-stu-id="64563-130">ID</span></span>  <br/> |<span data-ttu-id="64563-131">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="64563-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="64563-132">necesario</span><span class="sxs-lookup"><span data-stu-id="64563-132">required</span></span>  <br/> |<span data-ttu-id="64563-133">Especifica el atributo ID de una página en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="64563-133">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="64563-134">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="64563-134">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="64563-135">T</span><span class="sxs-lookup"><span data-stu-id="64563-135">T</span></span>  <br/> |<span data-ttu-id="64563-136">xsd:string</span><span class="sxs-lookup"><span data-stu-id="64563-136">xsd:string</span></span>  <br/> |<span data-ttu-id="64563-137">necesario</span><span class="sxs-lookup"><span data-stu-id="64563-137">required</span></span>  <br/> |<span data-ttu-id="64563-138">Especifica el tipo de referencia.</span><span class="sxs-lookup"><span data-stu-id="64563-138">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="64563-139">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="64563-139">Values of the xsd:string type.</span></span>  <br/> |
   

