---
title: Elemento RefBy (Trigger_Type complexType) (XML de Visio)
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
# <a name="refby-element-trigger_type-complextype-visio-xml"></a><span data-ttu-id="c095b-103">Elemento RefBy (Trigger_Type complexType) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="c095b-103">RefBy element (Trigger_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="c095b-104">Especifica una referencia a una página del dibujo.</span><span class="sxs-lookup"><span data-stu-id="c095b-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c095b-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c095b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c095b-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="c095b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c095b-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="c095b-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c095b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c095b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c095b-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c095b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c095b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c095b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c095b-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="c095b-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="c095b-112">Definición</span><span class="sxs-lookup"><span data-stu-id="c095b-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c095b-113">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="c095b-113">Elements and attributes</span></span>

<span data-ttu-id="c095b-114">Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="c095b-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c095b-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c095b-115">Parent elements</span></span>

|<span data-ttu-id="c095b-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c095b-116">**Element**</span></span>|<span data-ttu-id="c095b-117">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c095b-117">**Type**</span></span>|<span data-ttu-id="c095b-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c095b-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c095b-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="c095b-119">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="c095b-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="c095b-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c095b-121">Proporciona instrucciones a Microsoft Visio para recalcular una relación entre elementos de documento en un archivo de Visio.</span><span class="sxs-lookup"><span data-stu-id="c095b-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |

   
### <a name="child-elements"></a><span data-ttu-id="c095b-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c095b-122">Child elements</span></span>

<span data-ttu-id="c095b-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c095b-123">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c095b-124">Atributos</span><span class="sxs-lookup"><span data-stu-id="c095b-124">Attributes</span></span>

|<span data-ttu-id="c095b-125">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c095b-125">**Attribute**</span></span>|<span data-ttu-id="c095b-126">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c095b-126">**Type**</span></span>|<span data-ttu-id="c095b-127">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="c095b-127">**Required**</span></span>|<span data-ttu-id="c095b-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c095b-128">**Description**</span></span>|<span data-ttu-id="c095b-129">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="c095b-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c095b-130">ID</span><span class="sxs-lookup"><span data-stu-id="c095b-130">ID</span></span>  <br/> |<span data-ttu-id="c095b-131">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c095b-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c095b-132">necesario</span><span class="sxs-lookup"><span data-stu-id="c095b-132">required</span></span>  <br/> |<span data-ttu-id="c095b-133">Especifica el atributo id. de una página del dibujo.</span><span class="sxs-lookup"><span data-stu-id="c095b-133">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="c095b-134">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c095b-134">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c095b-135">T</span><span class="sxs-lookup"><span data-stu-id="c095b-135">T</span></span>  <br/> |<span data-ttu-id="c095b-136">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c095b-136">xsd:string</span></span>  <br/> |<span data-ttu-id="c095b-137">necesario</span><span class="sxs-lookup"><span data-stu-id="c095b-137">required</span></span>  <br/> |<span data-ttu-id="c095b-138">Especifica el tipo de referencia.</span><span class="sxs-lookup"><span data-stu-id="c095b-138">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="c095b-139">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c095b-139">Values of the xsd:string type.</span></span>  <br/> |
   

