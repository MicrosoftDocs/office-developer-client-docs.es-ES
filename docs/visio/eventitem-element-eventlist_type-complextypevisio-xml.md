---
title: Elemento EventItem (complexType EventList_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Encapsula un código de evento.
ms.openlocfilehash: 6ed539bd6cb4524b2498b636295442bed917c72a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337201"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a><span data-ttu-id="8b9dc-103">Elemento EventItem (complexType EventList_Type) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="8b9dc-103">EventItem element (EventList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="8b9dc-104">Encapsula un código de evento.</span><span class="sxs-lookup"><span data-stu-id="8b9dc-104">Encapsulates an event code.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8b9dc-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8b9dc-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8b9dc-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="8b9dc-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8b9dc-107">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="8b9dc-107">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8b9dc-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8b9dc-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8b9dc-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="8b9dc-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8b9dc-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="8b9dc-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8b9dc-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="8b9dc-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8b9dc-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="8b9dc-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8b9dc-113">Definición</span><span class="sxs-lookup"><span data-stu-id="8b9dc-113">Definition</span></span>

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8b9dc-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="8b9dc-114">Elements and attributes</span></span>

<span data-ttu-id="8b9dc-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="8b9dc-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8b9dc-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8b9dc-116">Parent elements</span></span>

|<span data-ttu-id="8b9dc-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8b9dc-117">**Element**</span></span>|<span data-ttu-id="8b9dc-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8b9dc-118">**Type**</span></span>|<span data-ttu-id="8b9dc-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8b9dc-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8b9dc-120">EventList</span><span class="sxs-lookup"><span data-stu-id="8b9dc-120">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8b9dc-121">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="8b9dc-121">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8b9dc-122">Contiene un elemento **EventItem** por cada evento al que debe responder un objeto.</span><span class="sxs-lookup"><span data-stu-id="8b9dc-122">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8b9dc-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8b9dc-123">Child elements</span></span>

<span data-ttu-id="8b9dc-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8b9dc-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8b9dc-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="8b9dc-125">Attributes</span></span>

|<span data-ttu-id="8b9dc-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="8b9dc-126">**Attribute**</span></span>|<span data-ttu-id="8b9dc-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8b9dc-127">**Type**</span></span>|<span data-ttu-id="8b9dc-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="8b9dc-128">**Required**</span></span>|<span data-ttu-id="8b9dc-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8b9dc-129">**Description**</span></span>|<span data-ttu-id="8b9dc-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="8b9dc-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8b9dc-131">Acción</span><span class="sxs-lookup"><span data-stu-id="8b9dc-131">Action</span></span>  <br/> |<span data-ttu-id="8b9dc-132">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="8b9dc-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="8b9dc-133">necesario</span><span class="sxs-lookup"><span data-stu-id="8b9dc-133">required</span></span>  <br/> |<span data-ttu-id="8b9dc-134">Especifica el código de acción del elemento **EventItem** primario.</span><span class="sxs-lookup"><span data-stu-id="8b9dc-134">Specifies the action code of the parent **EventItem** element.</span></span>  <br/> |<span data-ttu-id="8b9dc-135">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="8b9dc-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="8b9dc-136">Habilitado</span><span class="sxs-lookup"><span data-stu-id="8b9dc-136">Enabled</span></span>  <br/> |<span data-ttu-id="8b9dc-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="8b9dc-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8b9dc-138">opcional</span><span class="sxs-lookup"><span data-stu-id="8b9dc-138">optional</span></span>  <br/> |<span data-ttu-id="8b9dc-139">Representa una marca que indica si el evento está habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="8b9dc-139">Represents a flag indicating if the event is enabled or disabled.</span></span>  <br/> |<span data-ttu-id="8b9dc-140">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="8b9dc-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8b9dc-141">EventCode</span><span class="sxs-lookup"><span data-stu-id="8b9dc-141">EventCode</span></span>  <br/> |<span data-ttu-id="8b9dc-142">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="8b9dc-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="8b9dc-143">necesario</span><span class="sxs-lookup"><span data-stu-id="8b9dc-143">required</span></span>  <br/> |<span data-ttu-id="8b9dc-144">Un código que indica el evento que desencadena el complemento.</span><span class="sxs-lookup"><span data-stu-id="8b9dc-144">A code indicating the event that triggers the add-on.</span></span>  <br/> |<span data-ttu-id="8b9dc-145">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="8b9dc-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="8b9dc-146">ID</span><span class="sxs-lookup"><span data-stu-id="8b9dc-146">ID</span></span>  <br/> |<span data-ttu-id="8b9dc-147">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8b9dc-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8b9dc-148">necesario</span><span class="sxs-lookup"><span data-stu-id="8b9dc-148">required</span></span>  <br/> |<span data-ttu-id="8b9dc-149">IDENTIFICADOR del evento.</span><span class="sxs-lookup"><span data-stu-id="8b9dc-149">The ID of the event.</span></span>  <br/> |<span data-ttu-id="8b9dc-150">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8b9dc-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8b9dc-151">Target</span><span class="sxs-lookup"><span data-stu-id="8b9dc-151">Target</span></span>  <br/> |<span data-ttu-id="8b9dc-152">xsd: String</span><span class="sxs-lookup"><span data-stu-id="8b9dc-152">xsd:string</span></span>  <br/> |<span data-ttu-id="8b9dc-153">necesario</span><span class="sxs-lookup"><span data-stu-id="8b9dc-153">required</span></span>  <br/> |<span data-ttu-id="8b9dc-154">Especifica el destino de un evento.</span><span class="sxs-lookup"><span data-stu-id="8b9dc-154">Specifies the target of an event.</span></span>  <br/> |<span data-ttu-id="8b9dc-155">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="8b9dc-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8b9dc-156">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="8b9dc-156">TargetArgs</span></span>  <br/> |<span data-ttu-id="8b9dc-157">xsd: String</span><span class="sxs-lookup"><span data-stu-id="8b9dc-157">xsd:string</span></span>  <br/> |<span data-ttu-id="8b9dc-158">necesario</span><span class="sxs-lookup"><span data-stu-id="8b9dc-158">required</span></span>  <br/> |<span data-ttu-id="8b9dc-159">Especifica una cadena que contiene los argumentos que se enviarán al destino de un evento.</span><span class="sxs-lookup"><span data-stu-id="8b9dc-159">Specifies a string containing arguments to be sent to the target of an event.</span></span>  <br/> |<span data-ttu-id="8b9dc-160">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="8b9dc-160">Values of the xsd:string type.</span></span>  <br/> |
   

