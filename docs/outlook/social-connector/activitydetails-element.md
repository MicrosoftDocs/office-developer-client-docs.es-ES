---
title: elemento activityDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: El elemento activityDetails almacena los datos sin procesar de un único elemento de fuente de actividad. Cada elemento de fuente de actividad debe tener su propio elemento activityDetails. Los datos del elemento activityDetails se hacen referencia en las plantillas de actividad mediante elementos name.
ms.openlocfilehash: fd9c2136e8e2b687fa281ecda71039809848f63c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434875"
---
# <a name="activitydetails-element"></a><span data-ttu-id="36cdc-105">elemento activityDetails</span><span class="sxs-lookup"><span data-stu-id="36cdc-105">activityDetails Element</span></span>

<span data-ttu-id="36cdc-106">El **elemento activityDetails** almacena los datos sin procesar de un único elemento de fuente de actividad.</span><span class="sxs-lookup"><span data-stu-id="36cdc-106">The **activityDetails** element stores the raw data for a single activity feed item.</span></span> <span data-ttu-id="36cdc-107">Cada elemento de fuente de actividad debe tener su **propio elemento activityDetails.**</span><span class="sxs-lookup"><span data-stu-id="36cdc-107">Each activity feed item must have its own **activityDetails** element.</span></span> <span data-ttu-id="36cdc-108">Los datos del **elemento activityDetails** se hacen referencia en las plantillas de actividad mediante **elementos name.**</span><span class="sxs-lookup"><span data-stu-id="36cdc-108">Data in the **activityDetails** element is referenced in activity templates by using **name** elements.</span></span> <span data-ttu-id="36cdc-109">Cada fragmento de datos del **elemento activityDetails** debe tener un **elemento name.**</span><span class="sxs-lookup"><span data-stu-id="36cdc-109">Every piece of data in the **activityDetails** element must have a **name** element.</span></span> 
  
<span data-ttu-id="36cdc-110">En la tabla siguiente se describen los seis elementos que requiere **el elemento activityDetails.**</span><span class="sxs-lookup"><span data-stu-id="36cdc-110">The following table describes the six elements that the **activityDetails** element requires.</span></span> 
  
|<span data-ttu-id="36cdc-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="36cdc-111">**Element**</span></span>|<span data-ttu-id="36cdc-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="36cdc-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="36cdc-113">**ownerID**</span><span class="sxs-lookup"><span data-stu-id="36cdc-113">**ownerID**</span></span> <br/> |<span data-ttu-id="36cdc-114">El identificador del usuario de la red social que generó este elemento de fuente de actividad.</span><span class="sxs-lookup"><span data-stu-id="36cdc-114">The ID of the user on the social network who generated this activity feed item.</span></span>  <br/> |
|<span data-ttu-id="36cdc-115">**objectID**</span><span class="sxs-lookup"><span data-stu-id="36cdc-115">**objectID**</span></span> <br/> |<span data-ttu-id="36cdc-116">Una cadena única para que el elemento de fuente de actividad detecte elementos de fuente duplicados.</span><span class="sxs-lookup"><span data-stu-id="36cdc-116">A unique string for the activity feed item to detect duplicate feed items.</span></span>  <br/> |
|<span data-ttu-id="36cdc-117">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="36cdc-117">**applicationId**</span></span> <br/> |<span data-ttu-id="36cdc-118">Uno de los dos identificadores únicos que se usan para hacer coincidir el elemento de fuente de actividad con su plantilla.</span><span class="sxs-lookup"><span data-stu-id="36cdc-118">One of two unique IDs that are used to match the activity feed item with its template.</span></span> <span data-ttu-id="36cdc-119">Si tiene varias aplicaciones u otras agrupaciones, puede usarse como organizador de plantillas de primer nivel.</span><span class="sxs-lookup"><span data-stu-id="36cdc-119">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="36cdc-120">**templateId**</span><span class="sxs-lookup"><span data-stu-id="36cdc-120">**templateId**</span></span> <br/> |<span data-ttu-id="36cdc-121">El segundo identificador único que se usa para hacer coincidir el elemento de fuente de actividad con su plantilla.</span><span class="sxs-lookup"><span data-stu-id="36cdc-121">The second unique ID that is used to match the activity feed item with its template.</span></span> <span data-ttu-id="36cdc-122">Se puede usar como organizador de plantillas de segundo nivel.</span><span class="sxs-lookup"><span data-stu-id="36cdc-122">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="36cdc-123">**publishDate**</span><span class="sxs-lookup"><span data-stu-id="36cdc-123">**publishDate**</span></span> <br/> |<span data-ttu-id="36cdc-124">Fecha y hora en que se publicó el elemento de fuente de actividad.</span><span class="sxs-lookup"><span data-stu-id="36cdc-124">The date and time that the activity feed item was published.</span></span>  <br/> |
|<span data-ttu-id="36cdc-125">**templateVariables**</span><span class="sxs-lookup"><span data-stu-id="36cdc-125">**templateVariables**</span></span> <br/> |<span data-ttu-id="36cdc-126">Los datos que se usarán en los tokens de la plantilla de elemento de fuente de actividad.</span><span class="sxs-lookup"><span data-stu-id="36cdc-126">The data to be used in the tokens for the activity feed item template.</span></span>  <br/> |
   
<span data-ttu-id="36cdc-127">Para obtener un ejemplo de XML de fuente de actividad, vea [Ejemplo XML de fuente de actividad](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="36cdc-127">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="36cdc-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="36cdc-128">See also</span></span>

- [<span data-ttu-id="36cdc-129">Información general sobre XML para un elemento de fuente de actividad</span><span class="sxs-lookup"><span data-stu-id="36cdc-129">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="36cdc-130">elemento activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="36cdc-130">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="36cdc-131">Variables de plantilla</span><span class="sxs-lookup"><span data-stu-id="36cdc-131">Template Variables</span></span>](template-variables.md) 
- [<span data-ttu-id="36cdc-132">Directrices para mostrar actividades correctamente</span><span class="sxs-lookup"><span data-stu-id="36cdc-132">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="36cdc-133">XML para actividades</span><span class="sxs-lookup"><span data-stu-id="36cdc-133">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="36cdc-134">Outlook Esquema XML del proveedor de Social Connector</span><span class="sxs-lookup"><span data-stu-id="36cdc-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="36cdc-135">Desarrollo de un proveedor con el esquema XML de OSC</span><span class="sxs-lookup"><span data-stu-id="36cdc-135">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

