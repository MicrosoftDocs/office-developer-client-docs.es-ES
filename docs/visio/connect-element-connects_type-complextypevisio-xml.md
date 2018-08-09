---
title: Conectar el elemento (Connects_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: "\n			Representa una conexión entre dos formas de un dibujo, como una línea y un cuadro en un organigrama.\n"
ms.openlocfilehash: 1bd3e1f006afe8d5bbb698e0b3a2179b74728315
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821844"
---
# <a name="connect-element-connectstype-complextype-visio-xml"></a><span data-ttu-id="b5446-103">Conectar el elemento (Connects_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="b5446-103">Connect element (Connects_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b5446-104">
			Representa una conexión entre dos formas de un dibujo, como una línea y un cuadro en un organigrama.
</span><span class="sxs-lookup"><span data-stu-id="b5446-104">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b5446-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b5446-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5446-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="b5446-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b5446-107">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="b5446-107">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b5446-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b5446-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b5446-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b5446-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b5446-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b5446-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b5446-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="b5446-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b5446-112">página # .xml, master # .xml</span><span class="sxs-lookup"><span data-stu-id="b5446-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b5446-113">Definición</span><span class="sxs-lookup"><span data-stu-id="b5446-113">Definition</span></span>

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b5446-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="b5446-114">Elements and attributes</span></span>

<span data-ttu-id="b5446-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="b5446-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b5446-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b5446-116">Parent elements</span></span>

|<span data-ttu-id="b5446-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="b5446-117">**Element**</span></span>|<span data-ttu-id="b5446-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b5446-118">**Type**</span></span>|<span data-ttu-id="b5446-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b5446-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b5446-120">Connects</span><span class="sxs-lookup"><span data-stu-id="b5446-120">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b5446-121">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="b5446-121">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b5446-122">Contiene un elemento **Connect** para cada conexión entre dos formas de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="b5446-122">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b5446-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b5446-123">Child elements</span></span>

<span data-ttu-id="b5446-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b5446-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b5446-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="b5446-125">Attributes</span></span>

|<span data-ttu-id="b5446-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="b5446-126">**Attribute**</span></span>|<span data-ttu-id="b5446-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b5446-127">**Type**</span></span>|<span data-ttu-id="b5446-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="b5446-128">**Required**</span></span>|<span data-ttu-id="b5446-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b5446-129">**Description**</span></span>|<span data-ttu-id="b5446-130">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="b5446-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b5446-131">FromCell</span><span class="sxs-lookup"><span data-stu-id="b5446-131">FromCell</span></span>  <br/> |<span data-ttu-id="b5446-132">xsd: String</span><span class="sxs-lookup"><span data-stu-id="b5446-132">xsd:string</span></span>  <br/> |<span data-ttu-id="b5446-133">opcional</span><span class="sxs-lookup"><span data-stu-id="b5446-133">optional</span></span>  <br/> |<span data-ttu-id="b5446-134">La celda desde la que se origina una conexión.</span><span class="sxs-lookup"><span data-stu-id="b5446-134">The cell from which a connection originates.</span></span>  <br/> |<span data-ttu-id="b5446-135">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="b5446-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b5446-136">FromPart</span><span class="sxs-lookup"><span data-stu-id="b5446-136">FromPart</span></span>  <br/> |<span data-ttu-id="b5446-137">xsd: int</span><span class="sxs-lookup"><span data-stu-id="b5446-137">xsd:int</span></span>  <br/> |<span data-ttu-id="b5446-138">opcional</span><span class="sxs-lookup"><span data-stu-id="b5446-138">optional</span></span>  <br/> |<span data-ttu-id="b5446-139">La parte de una forma desde la que se origina una conexión.</span><span class="sxs-lookup"><span data-stu-id="b5446-139">The part of a shape from which a connection originates.</span></span>  <br/> |<span data-ttu-id="b5446-140">Valores del tipo XSD: int.</span><span class="sxs-lookup"><span data-stu-id="b5446-140">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="b5446-141">FromSheet</span><span class="sxs-lookup"><span data-stu-id="b5446-141">FromSheet</span></span>  <br/> |<span data-ttu-id="b5446-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b5446-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b5446-143">necesario</span><span class="sxs-lookup"><span data-stu-id="b5446-143">required</span></span>  <br/> |<span data-ttu-id="b5446-144">El identificador de la forma desde la que se originan una conexión o conexiones.</span><span class="sxs-lookup"><span data-stu-id="b5446-144">The ID of the shape from which a connection or connections originate.</span></span>  <br/> |<span data-ttu-id="b5446-145">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b5446-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b5446-146">ToCell</span><span class="sxs-lookup"><span data-stu-id="b5446-146">ToCell</span></span>  <br/> |<span data-ttu-id="b5446-147">xsd: String</span><span class="sxs-lookup"><span data-stu-id="b5446-147">xsd:string</span></span>  <br/> |<span data-ttu-id="b5446-148">opcional</span><span class="sxs-lookup"><span data-stu-id="b5446-148">optional</span></span>  <br/> |<span data-ttu-id="b5446-149">La celda a la que se realiza una conexión.</span><span class="sxs-lookup"><span data-stu-id="b5446-149">The cell to which a connection is made.</span></span>  <br/> |<span data-ttu-id="b5446-150">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="b5446-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b5446-151">ToPart</span><span class="sxs-lookup"><span data-stu-id="b5446-151">ToPart</span></span>  <br/> |<span data-ttu-id="b5446-152">xsd: int</span><span class="sxs-lookup"><span data-stu-id="b5446-152">xsd:int</span></span>  <br/> |<span data-ttu-id="b5446-153">opcional</span><span class="sxs-lookup"><span data-stu-id="b5446-153">optional</span></span>  <br/> |<span data-ttu-id="b5446-154">La parte de una forma a la que se realiza una conexión.</span><span class="sxs-lookup"><span data-stu-id="b5446-154">The part of a shape to which a connection is made.</span></span>  <br/> |<span data-ttu-id="b5446-155">Valores del tipo XSD: int.</span><span class="sxs-lookup"><span data-stu-id="b5446-155">Values of the xsd:Int type.</span></span>  <br/> |
|<span data-ttu-id="b5446-156">ToSheet</span><span class="sxs-lookup"><span data-stu-id="b5446-156">ToSheet</span></span>  <br/> |<span data-ttu-id="b5446-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b5446-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b5446-158">necesario</span><span class="sxs-lookup"><span data-stu-id="b5446-158">required</span></span>  <br/> |<span data-ttu-id="b5446-159">El identificador de la forma a la que se realizan una o más conexiones.</span><span class="sxs-lookup"><span data-stu-id="b5446-159">The ID of the shape to which one or more connections are made.</span></span>  <br/> |<span data-ttu-id="b5446-160">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b5446-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

