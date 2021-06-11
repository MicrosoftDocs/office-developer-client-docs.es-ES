---
title: Elemento EventItem (EventList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Encapsula un código de evento.
ms.openlocfilehash: 0db88a175d3e0330cb648f870559d9d2bd4dc1d8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541844"
---
# <a name="eventitem-element-eventlist_type-complextype-visio-xml"></a><span data-ttu-id="9a978-103">Elemento EventItem (EventList_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9a978-103">EventItem element (EventList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="9a978-104">Encapsula un código de evento.</span><span class="sxs-lookup"><span data-stu-id="9a978-104">Encapsulates an event code.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9a978-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9a978-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9a978-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="9a978-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9a978-107">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="9a978-107">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9a978-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9a978-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9a978-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9a978-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9a978-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9a978-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9a978-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="9a978-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9a978-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="9a978-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9a978-113">Definición</span><span class="sxs-lookup"><span data-stu-id="9a978-113">Definition</span></span>

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9a978-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="9a978-114">Elements and attributes</span></span>

<span data-ttu-id="9a978-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="9a978-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9a978-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9a978-116">Parent elements</span></span>

|<span data-ttu-id="9a978-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9a978-117">**Element**</span></span>|<span data-ttu-id="9a978-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9a978-118">**Type**</span></span>|<span data-ttu-id="9a978-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9a978-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9a978-120">EventList</span><span class="sxs-lookup"><span data-stu-id="9a978-120">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9a978-121">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="9a978-121">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9a978-122">Contiene un **elemento EventItem** para cada evento al que debe responder un objeto.</span><span class="sxs-lookup"><span data-stu-id="9a978-122">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9a978-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9a978-123">Child elements</span></span>

<span data-ttu-id="9a978-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9a978-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9a978-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="9a978-125">Attributes</span></span>

|<span data-ttu-id="9a978-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="9a978-126">**Attribute**</span></span>|<span data-ttu-id="9a978-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9a978-127">**Type**</span></span>|<span data-ttu-id="9a978-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="9a978-128">**Required**</span></span>|<span data-ttu-id="9a978-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9a978-129">**Description**</span></span>|<span data-ttu-id="9a978-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="9a978-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9a978-131">Acción</span><span class="sxs-lookup"><span data-stu-id="9a978-131">Action</span></span>  <br/> |<span data-ttu-id="9a978-132">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="9a978-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="9a978-133">necesario</span><span class="sxs-lookup"><span data-stu-id="9a978-133">required</span></span>  <br/> |<span data-ttu-id="9a978-134">Especifica el código de acción del elemento **primario EventItem.**</span><span class="sxs-lookup"><span data-stu-id="9a978-134">Specifies the action code of the parent **EventItem** element.</span></span>  <br/> |<span data-ttu-id="9a978-135">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="9a978-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="9a978-136">Habilitado</span><span class="sxs-lookup"><span data-stu-id="9a978-136">Enabled</span></span>  <br/> |<span data-ttu-id="9a978-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9a978-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9a978-138">opcional</span><span class="sxs-lookup"><span data-stu-id="9a978-138">optional</span></span>  <br/> |<span data-ttu-id="9a978-139">Representa una marca que indica si el evento está habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="9a978-139">Represents a flag indicating if the event is enabled or disabled.</span></span>  <br/> |<span data-ttu-id="9a978-140">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9a978-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9a978-141">EventCode</span><span class="sxs-lookup"><span data-stu-id="9a978-141">EventCode</span></span>  <br/> |<span data-ttu-id="9a978-142">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="9a978-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="9a978-143">necesario</span><span class="sxs-lookup"><span data-stu-id="9a978-143">required</span></span>  <br/> |<span data-ttu-id="9a978-144">Código que indica el evento que desencadena el complemento.</span><span class="sxs-lookup"><span data-stu-id="9a978-144">A code indicating the event that triggers the add-on.</span></span>  <br/> |<span data-ttu-id="9a978-145">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="9a978-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="9a978-146">ID</span><span class="sxs-lookup"><span data-stu-id="9a978-146">ID</span></span>  <br/> |<span data-ttu-id="9a978-147">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9a978-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9a978-148">necesario</span><span class="sxs-lookup"><span data-stu-id="9a978-148">required</span></span>  <br/> |<span data-ttu-id="9a978-149">El identificador del evento.</span><span class="sxs-lookup"><span data-stu-id="9a978-149">The ID of the event.</span></span>  <br/> |<span data-ttu-id="9a978-150">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9a978-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9a978-151">Target</span><span class="sxs-lookup"><span data-stu-id="9a978-151">Target</span></span>  <br/> |<span data-ttu-id="9a978-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9a978-152">xsd:string</span></span>  <br/> |<span data-ttu-id="9a978-153">necesario</span><span class="sxs-lookup"><span data-stu-id="9a978-153">required</span></span>  <br/> |<span data-ttu-id="9a978-154">Especifica el destino de un evento.</span><span class="sxs-lookup"><span data-stu-id="9a978-154">Specifies the target of an event.</span></span>  <br/> |<span data-ttu-id="9a978-155">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9a978-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9a978-156">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="9a978-156">TargetArgs</span></span>  <br/> |<span data-ttu-id="9a978-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9a978-157">xsd:string</span></span>  <br/> |<span data-ttu-id="9a978-158">necesario</span><span class="sxs-lookup"><span data-stu-id="9a978-158">required</span></span>  <br/> |<span data-ttu-id="9a978-159">Especifica una cadena que contiene argumentos que se enviarán al destino de un evento.</span><span class="sxs-lookup"><span data-stu-id="9a978-159">Specifies a string containing arguments to be sent to the target of an event.</span></span>  <br/> |<span data-ttu-id="9a978-160">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9a978-160">Values of the xsd:string type.</span></span>  <br/> |
   

