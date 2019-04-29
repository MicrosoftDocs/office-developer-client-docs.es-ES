---
title: Elemento activityDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: El elemento activityDetails almacena los datos sin procesar de un único elemento de fuente de actividades. Cada elemento de fuente de actividad debe tener su propio elemento activityDetails. Se hace referencia a los datos del elemento activityDetails en las plantillas de actividad mediante elementos de nombre.
ms.openlocfilehash: fd9c2136e8e2b687fa281ecda71039809848f63c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434875"
---
# <a name="activitydetails-element"></a><span data-ttu-id="3ca39-105">Elemento activityDetails</span><span class="sxs-lookup"><span data-stu-id="3ca39-105">activityDetails Element</span></span>

<span data-ttu-id="3ca39-106">El elemento **activityDetails** almacena los datos sin procesar de un único elemento de fuente de actividades.</span><span class="sxs-lookup"><span data-stu-id="3ca39-106">The **activityDetails** element stores the raw data for a single activity feed item.</span></span> <span data-ttu-id="3ca39-107">Cada elemento de fuente de actividad debe tener su propio elemento **activityDetails** .</span><span class="sxs-lookup"><span data-stu-id="3ca39-107">Each activity feed item must have its own **activityDetails** element.</span></span> <span data-ttu-id="3ca39-108">Se hace referencia a los datos del elemento **activityDetails** en las plantillas de actividad mediante elementos de **nombre** .</span><span class="sxs-lookup"><span data-stu-id="3ca39-108">Data in the **activityDetails** element is referenced in activity templates by using **name** elements.</span></span> <span data-ttu-id="3ca39-109">Cada dato en el elemento **activityDetails** debe tener un elemento **Name** .</span><span class="sxs-lookup"><span data-stu-id="3ca39-109">Every piece of data in the **activityDetails** element must have a **name** element.</span></span> 
  
<span data-ttu-id="3ca39-110">En la tabla siguiente se describen los seis elementos que requiere el elemento **activityDetails** .</span><span class="sxs-lookup"><span data-stu-id="3ca39-110">The following table describes the six elements that the **activityDetails** element requires.</span></span> 
  
|<span data-ttu-id="3ca39-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3ca39-111">**Element**</span></span>|<span data-ttu-id="3ca39-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3ca39-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3ca39-113">**ownerID**</span><span class="sxs-lookup"><span data-stu-id="3ca39-113">**ownerID**</span></span> <br/> |<span data-ttu-id="3ca39-114">El identificador del usuario en la red social que generó este elemento de la fuente de actividades.</span><span class="sxs-lookup"><span data-stu-id="3ca39-114">The ID of the user on the social network who generated this activity feed item.</span></span>  <br/> |
|<span data-ttu-id="3ca39-115">**objectID**</span><span class="sxs-lookup"><span data-stu-id="3ca39-115">**objectID**</span></span> <br/> |<span data-ttu-id="3ca39-116">Una cadena única para que el elemento de fuente de actividades detecte elementos de fuente duplicados.</span><span class="sxs-lookup"><span data-stu-id="3ca39-116">A unique string for the activity feed item to detect duplicate feed items.</span></span>  <br/> |
|<span data-ttu-id="3ca39-117">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="3ca39-117">**applicationId**</span></span> <br/> |<span data-ttu-id="3ca39-118">Uno de los dos identificadores únicos que se usan para hacer coincidir el elemento de fuente de actividad con su plantilla.</span><span class="sxs-lookup"><span data-stu-id="3ca39-118">One of two unique IDs that are used to match the activity feed item with its template.</span></span> <span data-ttu-id="3ca39-119">Si tiene varias aplicaciones u otros grupos, puede usarse como organizador de plantillas de primer nivel.</span><span class="sxs-lookup"><span data-stu-id="3ca39-119">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="3ca39-120">**templateId**</span><span class="sxs-lookup"><span data-stu-id="3ca39-120">**templateId**</span></span> <br/> |<span data-ttu-id="3ca39-121">El segundo identificador único que se usa para hacer coincidir el elemento de fuente de actividad con su plantilla.</span><span class="sxs-lookup"><span data-stu-id="3ca39-121">The second unique ID that is used to match the activity feed item with its template.</span></span> <span data-ttu-id="3ca39-122">Se puede usar como un organizador de plantillas de segundo nivel.</span><span class="sxs-lookup"><span data-stu-id="3ca39-122">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="3ca39-123">**publishDate**</span><span class="sxs-lookup"><span data-stu-id="3ca39-123">**publishDate**</span></span> <br/> |<span data-ttu-id="3ca39-124">Fecha y hora en que se publicó el elemento de fuente de actividad.</span><span class="sxs-lookup"><span data-stu-id="3ca39-124">The date and time that the activity feed item was published.</span></span>  <br/> |
|<span data-ttu-id="3ca39-125">**templateVariables**</span><span class="sxs-lookup"><span data-stu-id="3ca39-125">**templateVariables**</span></span> <br/> |<span data-ttu-id="3ca39-126">Datos que se van a usar en los tokens de la plantilla de elemento de fuente de actividades.</span><span class="sxs-lookup"><span data-stu-id="3ca39-126">The data to be used in the tokens for the activity feed item template.</span></span>  <br/> |
   
<span data-ttu-id="3ca39-127">Para obtener un ejemplo de XML de fuente de actividades, consulte [ejemplo de XML de fuente de actividades](activity-feed-xml-example.md) .</span><span class="sxs-lookup"><span data-stu-id="3ca39-127">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3ca39-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="3ca39-128">See also</span></span>

- [<span data-ttu-id="3ca39-129">Información general sobre XML para un elemento de fuente de actividades</span><span class="sxs-lookup"><span data-stu-id="3ca39-129">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="3ca39-130">Elemento activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="3ca39-130">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="3ca39-131">Variables de plantilla</span><span class="sxs-lookup"><span data-stu-id="3ca39-131">Template Variables</span></span>](template-variables.md) 
- [<span data-ttu-id="3ca39-132">Directrices para mostrar correctamente las actividades</span><span class="sxs-lookup"><span data-stu-id="3ca39-132">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="3ca39-133">XML para actividades</span><span class="sxs-lookup"><span data-stu-id="3ca39-133">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="3ca39-134">Esquema XML del proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="3ca39-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="3ca39-135">Desarrollo de un proveedor con el esquema XML de OSC</span><span class="sxs-lookup"><span data-stu-id="3ca39-135">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

