---
title: Elemento de EventItem (EventList_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Encapsula un código de evento.
ms.openlocfilehash: dcdd3aa264e8ddfb1aa6f2e908f1c43a0d470872
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822080"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a><span data-ttu-id="cf657-103">Elemento de EventItem (EventList_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="cf657-103">EventItem element (EventList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="cf657-104">Encapsula un código de evento.</span><span class="sxs-lookup"><span data-stu-id="cf657-104">Encapsulates an event code.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cf657-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cf657-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cf657-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="cf657-106">**Element type**</span></span> <br/> |[<span data-ttu-id="cf657-107">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="cf657-107">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="cf657-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cf657-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="cf657-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="cf657-109">**Schema file**</span></span> <br/> |<span data-ttu-id="cf657-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="cf657-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="cf657-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="cf657-111">**Document parts**</span></span> <br/> |<span data-ttu-id="cf657-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="cf657-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cf657-113">Definición</span><span class="sxs-lookup"><span data-stu-id="cf657-113">Definition</span></span>

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cf657-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="cf657-114">Elements and attributes</span></span>

<span data-ttu-id="cf657-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="cf657-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="cf657-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cf657-116">Parent elements</span></span>

|<span data-ttu-id="cf657-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="cf657-117">**Element**</span></span>|<span data-ttu-id="cf657-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cf657-118">**Type**</span></span>|<span data-ttu-id="cf657-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cf657-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cf657-120">EventList</span><span class="sxs-lookup"><span data-stu-id="cf657-120">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cf657-121">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="cf657-121">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cf657-122">Contiene un elemento **EventItem** para cada evento al que debe responder un objeto.</span><span class="sxs-lookup"><span data-stu-id="cf657-122">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cf657-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cf657-123">Child elements</span></span>

<span data-ttu-id="cf657-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cf657-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cf657-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="cf657-125">Attributes</span></span>

|<span data-ttu-id="cf657-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="cf657-126">**Attribute**</span></span>|<span data-ttu-id="cf657-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cf657-127">**Type**</span></span>|<span data-ttu-id="cf657-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="cf657-128">**Required**</span></span>|<span data-ttu-id="cf657-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cf657-129">**Description**</span></span>|<span data-ttu-id="cf657-130">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="cf657-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cf657-131">Acción</span><span class="sxs-lookup"><span data-stu-id="cf657-131">Action</span></span>  <br/> |<span data-ttu-id="cf657-132">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="cf657-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="cf657-133">necesario</span><span class="sxs-lookup"><span data-stu-id="cf657-133">required</span></span>  <br/> |<span data-ttu-id="cf657-134">Especifica el código de acción del elemento primario **EventItem** .</span><span class="sxs-lookup"><span data-stu-id="cf657-134">Specifies the action code of the parent **EventItem** element.</span></span>  <br/> |<span data-ttu-id="cf657-135">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="cf657-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="cf657-136">Habilitado</span><span class="sxs-lookup"><span data-stu-id="cf657-136">Enabled</span></span>  <br/> |<span data-ttu-id="cf657-137">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="cf657-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="cf657-138">opcional</span><span class="sxs-lookup"><span data-stu-id="cf657-138">optional</span></span>  <br/> |<span data-ttu-id="cf657-139">Representa una marca que indica si el evento está habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="cf657-139">Represents a flag indicating if the event is enabled or disabled.</span></span>  <br/> |<span data-ttu-id="cf657-140">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="cf657-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="cf657-141">EventCode</span><span class="sxs-lookup"><span data-stu-id="cf657-141">EventCode</span></span>  <br/> |<span data-ttu-id="cf657-142">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="cf657-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="cf657-143">necesario</span><span class="sxs-lookup"><span data-stu-id="cf657-143">required</span></span>  <br/> |<span data-ttu-id="cf657-144">Un código que indica el evento que desencadena el complemento.</span><span class="sxs-lookup"><span data-stu-id="cf657-144">A code indicating the event that triggers the add-on.</span></span>  <br/> |<span data-ttu-id="cf657-145">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="cf657-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="cf657-146">ID</span><span class="sxs-lookup"><span data-stu-id="cf657-146">ID</span></span>  <br/> |<span data-ttu-id="cf657-147">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cf657-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cf657-148">necesario</span><span class="sxs-lookup"><span data-stu-id="cf657-148">required</span></span>  <br/> |<span data-ttu-id="cf657-149">El identificador del evento.</span><span class="sxs-lookup"><span data-stu-id="cf657-149">The ID of the event.</span></span>  <br/> |<span data-ttu-id="cf657-150">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cf657-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cf657-151">Destino</span><span class="sxs-lookup"><span data-stu-id="cf657-151">Target</span></span>  <br/> |<span data-ttu-id="cf657-152">xsd: String</span><span class="sxs-lookup"><span data-stu-id="cf657-152">xsd:string</span></span>  <br/> |<span data-ttu-id="cf657-153">necesario</span><span class="sxs-lookup"><span data-stu-id="cf657-153">required</span></span>  <br/> |<span data-ttu-id="cf657-154">Especifica el destino de un evento.</span><span class="sxs-lookup"><span data-stu-id="cf657-154">Specifies the target of an event.</span></span>  <br/> |<span data-ttu-id="cf657-155">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="cf657-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cf657-156">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="cf657-156">TargetArgs</span></span>  <br/> |<span data-ttu-id="cf657-157">xsd: String</span><span class="sxs-lookup"><span data-stu-id="cf657-157">xsd:string</span></span>  <br/> |<span data-ttu-id="cf657-158">necesario</span><span class="sxs-lookup"><span data-stu-id="cf657-158">required</span></span>  <br/> |<span data-ttu-id="cf657-159">Especifica una cadena que contiene los argumentos que se envíen al destino de un evento.</span><span class="sxs-lookup"><span data-stu-id="cf657-159">Specifies a string containing arguments to be sent to the target of an event.</span></span>  <br/> |<span data-ttu-id="cf657-160">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="cf657-160">Values of the xsd:string type.</span></span>  <br/> |
   

