---
title: Elemento Connect (Connects_Type complexType) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: Representa una conexión entre dos formas de un dibujo, como una línea y un cuadro en un organigrama.
ms.openlocfilehash: 3450a07e042fc633b9cd4952d9b3ad6b8190ed1e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541999"
---
# <a name="connect-element-connects_type-complextype-visio-xml"></a><span data-ttu-id="cc375-103">Elemento Connect (Connects_Type complexType) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="cc375-103">Connect element (Connects_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="cc375-104">Representa una conexión entre dos formas de un dibujo, como una línea y un cuadro en un organigrama.</span><span class="sxs-lookup"><span data-stu-id="cc375-104">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cc375-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cc375-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cc375-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="cc375-106">**Element type**</span></span> <br/> |[<span data-ttu-id="cc375-107">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="cc375-107">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="cc375-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cc375-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="cc375-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="cc375-109">**Schema file**</span></span> <br/> |<span data-ttu-id="cc375-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="cc375-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="cc375-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="cc375-111">**Document parts**</span></span> <br/> |<span data-ttu-id="cc375-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="cc375-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cc375-113">Definición</span><span class="sxs-lookup"><span data-stu-id="cc375-113">Definition</span></span>

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cc375-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="cc375-114">Elements and attributes</span></span>

<span data-ttu-id="cc375-115">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="cc375-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="cc375-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cc375-116">Parent elements</span></span>

|<span data-ttu-id="cc375-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cc375-117">**Element**</span></span>|<span data-ttu-id="cc375-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cc375-118">**Type**</span></span>|<span data-ttu-id="cc375-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cc375-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cc375-120">Connects</span><span class="sxs-lookup"><span data-stu-id="cc375-120">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cc375-121">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="cc375-121">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cc375-122">Contiene un **elemento Connect** para cada conexión entre dos formas de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="cc375-122">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cc375-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cc375-123">Child elements</span></span>

<span data-ttu-id="cc375-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cc375-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cc375-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="cc375-125">Attributes</span></span>

|<span data-ttu-id="cc375-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="cc375-126">**Attribute**</span></span>|<span data-ttu-id="cc375-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cc375-127">**Type**</span></span>|<span data-ttu-id="cc375-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="cc375-128">**Required**</span></span>|<span data-ttu-id="cc375-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cc375-129">**Description**</span></span>|<span data-ttu-id="cc375-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="cc375-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cc375-131">FromCell</span><span class="sxs-lookup"><span data-stu-id="cc375-131">FromCell</span></span>  <br/> |<span data-ttu-id="cc375-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="cc375-132">xsd:string</span></span>  <br/> |<span data-ttu-id="cc375-133">opcional</span><span class="sxs-lookup"><span data-stu-id="cc375-133">optional</span></span>  <br/> |<span data-ttu-id="cc375-134">Celda desde la que se origina una conexión.</span><span class="sxs-lookup"><span data-stu-id="cc375-134">The cell from which a connection originates.</span></span>  <br/> |<span data-ttu-id="cc375-135">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="cc375-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cc375-136">FromPart</span><span class="sxs-lookup"><span data-stu-id="cc375-136">FromPart</span></span>  <br/> |<span data-ttu-id="cc375-137">xsd:int</span><span class="sxs-lookup"><span data-stu-id="cc375-137">xsd:int</span></span>  <br/> |<span data-ttu-id="cc375-138">opcional</span><span class="sxs-lookup"><span data-stu-id="cc375-138">optional</span></span>  <br/> |<span data-ttu-id="cc375-139">Parte de una forma desde la que se origina una conexión.</span><span class="sxs-lookup"><span data-stu-id="cc375-139">The part of a shape from which a connection originates.</span></span>  <br/> |<span data-ttu-id="cc375-140">Valores del tipo xsd:int.</span><span class="sxs-lookup"><span data-stu-id="cc375-140">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="cc375-141">FromSheet</span><span class="sxs-lookup"><span data-stu-id="cc375-141">FromSheet</span></span>  <br/> |<span data-ttu-id="cc375-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cc375-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cc375-143">necesario</span><span class="sxs-lookup"><span data-stu-id="cc375-143">required</span></span>  <br/> |<span data-ttu-id="cc375-144">Identificador de la forma desde la que se origina una conexión o conexiones.</span><span class="sxs-lookup"><span data-stu-id="cc375-144">The ID of the shape from which a connection or connections originate.</span></span>  <br/> |<span data-ttu-id="cc375-145">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cc375-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cc375-146">ToCell</span><span class="sxs-lookup"><span data-stu-id="cc375-146">ToCell</span></span>  <br/> |<span data-ttu-id="cc375-147">xsd:string</span><span class="sxs-lookup"><span data-stu-id="cc375-147">xsd:string</span></span>  <br/> |<span data-ttu-id="cc375-148">opcional</span><span class="sxs-lookup"><span data-stu-id="cc375-148">optional</span></span>  <br/> |<span data-ttu-id="cc375-149">Celda a la que se realiza una conexión.</span><span class="sxs-lookup"><span data-stu-id="cc375-149">The cell to which a connection is made.</span></span>  <br/> |<span data-ttu-id="cc375-150">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="cc375-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cc375-151">ToPart</span><span class="sxs-lookup"><span data-stu-id="cc375-151">ToPart</span></span>  <br/> |<span data-ttu-id="cc375-152">xsd:int</span><span class="sxs-lookup"><span data-stu-id="cc375-152">xsd:int</span></span>  <br/> |<span data-ttu-id="cc375-153">opcional</span><span class="sxs-lookup"><span data-stu-id="cc375-153">optional</span></span>  <br/> |<span data-ttu-id="cc375-154">La parte de una forma a la que se realiza una conexión.</span><span class="sxs-lookup"><span data-stu-id="cc375-154">The part of a shape to which a connection is made.</span></span>  <br/> |<span data-ttu-id="cc375-155">Valores del tipo xsd:Int.</span><span class="sxs-lookup"><span data-stu-id="cc375-155">Values of the xsd:Int type.</span></span>  <br/> |
|<span data-ttu-id="cc375-156">ToSheet</span><span class="sxs-lookup"><span data-stu-id="cc375-156">ToSheet</span></span>  <br/> |<span data-ttu-id="cc375-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cc375-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cc375-158">necesario</span><span class="sxs-lookup"><span data-stu-id="cc375-158">required</span></span>  <br/> |<span data-ttu-id="cc375-159">Identificador de la forma a la que se realizan una o más conexiones.</span><span class="sxs-lookup"><span data-stu-id="cc375-159">The ID of the shape to which one or more connections are made.</span></span>  <br/> |<span data-ttu-id="cc375-160">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cc375-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

