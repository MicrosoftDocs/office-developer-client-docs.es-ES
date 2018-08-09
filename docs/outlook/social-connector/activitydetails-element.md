---
title: Elemento activityDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: El elemento activityDetails almacena los datos sin procesar para un elemento de fuente de actividades único. Cada elemento de fuente de actividades deben tener su propio elemento activityDetails. Datos en el elemento activityDetails se hace referencia en las plantillas de actividad mediante el uso de elementos de nombre.
ms.openlocfilehash: c326017a038dff138d690b020a98972a08212690
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821087"
---
# <a name="activitydetails-element"></a><span data-ttu-id="5fec2-105">Elemento activityDetails</span><span class="sxs-lookup"><span data-stu-id="5fec2-105">activityDetails Element</span></span>

<span data-ttu-id="5fec2-106">El elemento **activityDetails** almacena los datos sin procesar para un elemento de fuente de actividades único.</span><span class="sxs-lookup"><span data-stu-id="5fec2-106">The **activityDetails** element stores the raw data for a single activity feed item.</span></span> <span data-ttu-id="5fec2-107">Cada elemento de fuente de actividades deben tener su propio elemento **activityDetails** .</span><span class="sxs-lookup"><span data-stu-id="5fec2-107">Each activity feed item must have its own **activityDetails** element.</span></span> <span data-ttu-id="5fec2-108">Datos en el elemento **activityDetails** se hace referencia en las plantillas de actividad mediante el uso de elementos de **nombre** .</span><span class="sxs-lookup"><span data-stu-id="5fec2-108">Data in the **activityDetails** element is referenced in activity templates by using **name** elements.</span></span> <span data-ttu-id="5fec2-109">Cada parte de los datos en el elemento **activityDetails** debe tener un elemento de **nombre** .</span><span class="sxs-lookup"><span data-stu-id="5fec2-109">Every piece of data in the **activityDetails** element must have a **name** element.</span></span> 
  
<span data-ttu-id="5fec2-110">En la siguiente tabla se describe los seis elementos que requiere el elemento **activityDetails** .</span><span class="sxs-lookup"><span data-stu-id="5fec2-110">The following table describes the six elements that the **activityDetails** element requires.</span></span> 
  
|<span data-ttu-id="5fec2-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="5fec2-111">**Element**</span></span>|<span data-ttu-id="5fec2-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5fec2-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5fec2-113">**ownerID**</span><span class="sxs-lookup"><span data-stu-id="5fec2-113">**ownerID**</span></span> <br/> |<span data-ttu-id="5fec2-114">El identificador del usuario en la red social que generó esta actividad de fuente de elemento.</span><span class="sxs-lookup"><span data-stu-id="5fec2-114">The ID of the user on the social network who generated this activity feed item.</span></span>  <br/> |
|<span data-ttu-id="5fec2-115">**objectID**</span><span class="sxs-lookup"><span data-stu-id="5fec2-115">**objectID**</span></span> <br/> |<span data-ttu-id="5fec2-116">Una cadena única para la actividad de fuente elemento para detectar los elementos de fuente duplicado.</span><span class="sxs-lookup"><span data-stu-id="5fec2-116">A unique string for the activity feed item to detect duplicate feed items.</span></span>  <br/> |
|<span data-ttu-id="5fec2-117">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="5fec2-117">**applicationId**</span></span> <br/> |<span data-ttu-id="5fec2-118">Uno de los dos identificadores únicos que se usan para que coincida con la actividad de fuente elemento con su plantilla.</span><span class="sxs-lookup"><span data-stu-id="5fec2-118">One of two unique IDs that are used to match the activity feed item with its template.</span></span> <span data-ttu-id="5fec2-119">Si tiene varias aplicaciones u otras agrupaciones, esto se puede usar como el organizador de una plantilla de primer nivel.</span><span class="sxs-lookup"><span data-stu-id="5fec2-119">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="5fec2-120">**templateId**</span><span class="sxs-lookup"><span data-stu-id="5fec2-120">**templateId**</span></span> <br/> |<span data-ttu-id="5fec2-121">El segundo identificador único que se utiliza para que coincida con la actividad de fuente elemento con su plantilla.</span><span class="sxs-lookup"><span data-stu-id="5fec2-121">The second unique ID that is used to match the activity feed item with its template.</span></span> <span data-ttu-id="5fec2-122">Esto se puede usar como el organizador de una plantilla de segundo nivel.</span><span class="sxs-lookup"><span data-stu-id="5fec2-122">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="5fec2-123">**fecha de publicación**</span><span class="sxs-lookup"><span data-stu-id="5fec2-123">**publishDate**</span></span> <br/> |<span data-ttu-id="5fec2-124">La fecha y hora en que la actividad fuente elemento se publicó.</span><span class="sxs-lookup"><span data-stu-id="5fec2-124">The date and time that the activity feed item was published.</span></span>  <br/> |
|<span data-ttu-id="5fec2-125">**templateVariables**</span><span class="sxs-lookup"><span data-stu-id="5fec2-125">**templateVariables**</span></span> <br/> |<span data-ttu-id="5fec2-126">Los datos que se usará en los tokens para la plantilla de elemento de la fuente de actividad.</span><span class="sxs-lookup"><span data-stu-id="5fec2-126">The data to be used in the tokens for the activity feed item template.</span></span>  <br/> |
   
<span data-ttu-id="5fec2-127">Para obtener un ejemplo de la actividad de fuente XML, vea [Ejemplo de XML de fuente de actividad](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="5fec2-127">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5fec2-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="5fec2-128">See also</span></span>

- [<span data-ttu-id="5fec2-129">Elemento de la fuente de información general de XML de una actividad</span><span class="sxs-lookup"><span data-stu-id="5fec2-129">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="5fec2-130">Elemento activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="5fec2-130">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="5fec2-131">Variables de plantilla</span><span class="sxs-lookup"><span data-stu-id="5fec2-131">Template Variables</span></span>](template-variables.md) 
- [<span data-ttu-id="5fec2-132">Instrucciones para mostrar correctamente las actividades</span><span class="sxs-lookup"><span data-stu-id="5fec2-132">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="5fec2-133">XML de actividades</span><span class="sxs-lookup"><span data-stu-id="5fec2-133">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="5fec2-134">Esquema XML de proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="5fec2-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="5fec2-135">Desarrollar un proveedor con el esquema XML de OSC</span><span class="sxs-lookup"><span data-stu-id="5fec2-135">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

