---
title: Conectar el elemento (Connects_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: "\n			Representa una conexión entre dos formas de un dibujo, como una línea y un cuadro en un organigrama.\n"
ms.openlocfilehash: 82413f44f05f2ec6140e2b3981b7a1e8435becb0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399322"
---
# <a name="connect-element-connectstype-complextype-visio-xml"></a><span data-ttu-id="8b1bc-103">Conectar el elemento (Connects_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="8b1bc-103">Connect element (Connects_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="8b1bc-104">
			Representa una conexión entre dos formas de un dibujo, como una línea y un cuadro en un organigrama.
</span><span class="sxs-lookup"><span data-stu-id="8b1bc-104">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8b1bc-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8b1bc-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8b1bc-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="8b1bc-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8b1bc-107">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="8b1bc-107">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8b1bc-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8b1bc-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8b1bc-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="8b1bc-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8b1bc-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8b1bc-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8b1bc-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="8b1bc-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8b1bc-112">página # .xml, master # .xml</span><span class="sxs-lookup"><span data-stu-id="8b1bc-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8b1bc-113">Definición</span><span class="sxs-lookup"><span data-stu-id="8b1bc-113">Definition</span></span>

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8b1bc-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="8b1bc-114">Elements and attributes</span></span>

<span data-ttu-id="8b1bc-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="8b1bc-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8b1bc-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8b1bc-116">Parent elements</span></span>

|<span data-ttu-id="8b1bc-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="8b1bc-117">**Element**</span></span>|<span data-ttu-id="8b1bc-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8b1bc-118">**Type**</span></span>|<span data-ttu-id="8b1bc-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8b1bc-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8b1bc-120">Connects</span><span class="sxs-lookup"><span data-stu-id="8b1bc-120">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8b1bc-121">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="8b1bc-121">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8b1bc-122">Contiene un elemento **Connect** para cada conexión entre dos formas de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="8b1bc-122">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8b1bc-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8b1bc-123">Child elements</span></span>

<span data-ttu-id="8b1bc-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8b1bc-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8b1bc-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="8b1bc-125">Attributes</span></span>

|<span data-ttu-id="8b1bc-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="8b1bc-126">**Attribute**</span></span>|<span data-ttu-id="8b1bc-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8b1bc-127">**Type**</span></span>|<span data-ttu-id="8b1bc-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="8b1bc-128">**Required**</span></span>|<span data-ttu-id="8b1bc-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8b1bc-129">**Description**</span></span>|<span data-ttu-id="8b1bc-130">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="8b1bc-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8b1bc-131">FromCell</span><span class="sxs-lookup"><span data-stu-id="8b1bc-131">FromCell</span></span>  <br/> |<span data-ttu-id="8b1bc-132">xsd: String</span><span class="sxs-lookup"><span data-stu-id="8b1bc-132">xsd:string</span></span>  <br/> |<span data-ttu-id="8b1bc-133">opcional</span><span class="sxs-lookup"><span data-stu-id="8b1bc-133">optional</span></span>  <br/> |<span data-ttu-id="8b1bc-134">La celda desde la que se origina una conexión.</span><span class="sxs-lookup"><span data-stu-id="8b1bc-134">The cell from which a connection originates.</span></span>  <br/> |<span data-ttu-id="8b1bc-135">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="8b1bc-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8b1bc-136">FromPart</span><span class="sxs-lookup"><span data-stu-id="8b1bc-136">FromPart</span></span>  <br/> |<span data-ttu-id="8b1bc-137">xsd: int</span><span class="sxs-lookup"><span data-stu-id="8b1bc-137">xsd:int</span></span>  <br/> |<span data-ttu-id="8b1bc-138">opcional</span><span class="sxs-lookup"><span data-stu-id="8b1bc-138">optional</span></span>  <br/> |<span data-ttu-id="8b1bc-139">La parte de una forma desde la que se origina una conexión.</span><span class="sxs-lookup"><span data-stu-id="8b1bc-139">The part of a shape from which a connection originates.</span></span>  <br/> |<span data-ttu-id="8b1bc-140">Valores del tipo XSD: int.</span><span class="sxs-lookup"><span data-stu-id="8b1bc-140">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="8b1bc-141">FromSheet</span><span class="sxs-lookup"><span data-stu-id="8b1bc-141">FromSheet</span></span>  <br/> |<span data-ttu-id="8b1bc-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8b1bc-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8b1bc-143">necesario</span><span class="sxs-lookup"><span data-stu-id="8b1bc-143">required</span></span>  <br/> |<span data-ttu-id="8b1bc-144">El identificador de la forma desde la que se originan una conexión o conexiones.</span><span class="sxs-lookup"><span data-stu-id="8b1bc-144">The ID of the shape from which a connection or connections originate.</span></span>  <br/> |<span data-ttu-id="8b1bc-145">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8b1bc-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8b1bc-146">ToCell</span><span class="sxs-lookup"><span data-stu-id="8b1bc-146">ToCell</span></span>  <br/> |<span data-ttu-id="8b1bc-147">xsd: String</span><span class="sxs-lookup"><span data-stu-id="8b1bc-147">xsd:string</span></span>  <br/> |<span data-ttu-id="8b1bc-148">opcional</span><span class="sxs-lookup"><span data-stu-id="8b1bc-148">optional</span></span>  <br/> |<span data-ttu-id="8b1bc-149">La celda a la que se realiza una conexión.</span><span class="sxs-lookup"><span data-stu-id="8b1bc-149">The cell to which a connection is made.</span></span>  <br/> |<span data-ttu-id="8b1bc-150">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="8b1bc-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8b1bc-151">ToPart</span><span class="sxs-lookup"><span data-stu-id="8b1bc-151">ToPart</span></span>  <br/> |<span data-ttu-id="8b1bc-152">xsd: int</span><span class="sxs-lookup"><span data-stu-id="8b1bc-152">xsd:int</span></span>  <br/> |<span data-ttu-id="8b1bc-153">opcional</span><span class="sxs-lookup"><span data-stu-id="8b1bc-153">optional</span></span>  <br/> |<span data-ttu-id="8b1bc-154">La parte de una forma a la que se realiza una conexión.</span><span class="sxs-lookup"><span data-stu-id="8b1bc-154">The part of a shape to which a connection is made.</span></span>  <br/> |<span data-ttu-id="8b1bc-155">Valores del tipo XSD: int.</span><span class="sxs-lookup"><span data-stu-id="8b1bc-155">Values of the xsd:Int type.</span></span>  <br/> |
|<span data-ttu-id="8b1bc-156">ToSheet</span><span class="sxs-lookup"><span data-stu-id="8b1bc-156">ToSheet</span></span>  <br/> |<span data-ttu-id="8b1bc-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8b1bc-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8b1bc-158">necesario</span><span class="sxs-lookup"><span data-stu-id="8b1bc-158">required</span></span>  <br/> |<span data-ttu-id="8b1bc-159">El identificador de la forma a la que se realizan una o más conexiones.</span><span class="sxs-lookup"><span data-stu-id="8b1bc-159">The ID of the shape to which one or more connections are made.</span></span>  <br/> |<span data-ttu-id="8b1bc-160">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8b1bc-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

