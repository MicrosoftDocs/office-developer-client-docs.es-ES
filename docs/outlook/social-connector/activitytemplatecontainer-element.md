---
title: Elemento activityTemplateContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: Un elemento activityTemplateContainer es una plantilla que le permite dar formato a los elementos de la fuente de actividades y volver a usar XML que especifica un diseño.
ms.openlocfilehash: e744bb1bdb828003cdda7086468533b32b4bf20f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821090"
---
# <a name="activitytemplatecontainer-element"></a><span data-ttu-id="6e0c4-103">Elemento activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="6e0c4-103">activityTemplateContainer Element</span></span>

<span data-ttu-id="6e0c4-104">Un elemento **activityTemplateContainer** es una plantilla que le permite dar formato a los elementos de la fuente de actividades y volver a usar XML que especifica un diseño.</span><span class="sxs-lookup"><span data-stu-id="6e0c4-104">An **activityTemplateContainer** element is a template that allows you to format your activity feed items and reuse XML that specifies a layout.</span></span> <span data-ttu-id="6e0c4-105">Utilice los identificadores (**applicationID** y **templateID**) para que coincida con un elemento de la fuente (**activityDetails**) a una plantilla (**activityTemplateContainer**).</span><span class="sxs-lookup"><span data-stu-id="6e0c4-105">Use IDs (**applicationID** and **templateID**) to match a feed item (**activityDetails**) to a template (**activityTemplateContainer**).</span></span> <span data-ttu-id="6e0c4-106">Almacenar los datos de diseño como parte del elemento **activityTemplate** .</span><span class="sxs-lookup"><span data-stu-id="6e0c4-106">Store the layout data as part of the **activityTemplate** element.</span></span> <span data-ttu-id="6e0c4-107">Para hacer referencia a datos que se extraen desde el elemento de fuente de actividades individuales, use las variables de plantilla como marcadores de posición para información como personas, vínculos y texto.</span><span class="sxs-lookup"><span data-stu-id="6e0c4-107">To reference data that is pulled from the individual activity feed item, use template variables as placeholders for information such as people, links, and text.</span></span> 
  
<span data-ttu-id="6e0c4-108">En la siguiente tabla se describe los tres elementos que requiere el elemento **activityTemplateContainer** .</span><span class="sxs-lookup"><span data-stu-id="6e0c4-108">The following table describes the three elements that the **activityTemplateContainer** element requires.</span></span> 
  
|<span data-ttu-id="6e0c4-109">**Element**</span><span class="sxs-lookup"><span data-stu-id="6e0c4-109">**Element**</span></span>|<span data-ttu-id="6e0c4-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6e0c4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6e0c4-111">**applicationID**</span><span class="sxs-lookup"><span data-stu-id="6e0c4-111">**applicationID**</span></span> <br/> |<span data-ttu-id="6e0c4-112">Uno de los dos identificadores únicos que se usan para que coincida con el elemento de la fuente con su plantilla.</span><span class="sxs-lookup"><span data-stu-id="6e0c4-112">One of two unique IDs that are used to match the feed item with its template.</span></span> <span data-ttu-id="6e0c4-113">Si tiene varias aplicaciones u otras agrupaciones, esto se puede usar como el organizador de una plantilla de primer nivel.</span><span class="sxs-lookup"><span data-stu-id="6e0c4-113">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="6e0c4-114">**identificador de plantilla**</span><span class="sxs-lookup"><span data-stu-id="6e0c4-114">**templateID**</span></span> <br/> |<span data-ttu-id="6e0c4-115">El segundo identificador único que se utiliza para que coincida con el elemento de la fuente con su plantilla.</span><span class="sxs-lookup"><span data-stu-id="6e0c4-115">The second unique ID that is used to match the feed item with its template.</span></span> <span data-ttu-id="6e0c4-116">Esto se puede usar como el organizador de una plantilla de segundo nivel.</span><span class="sxs-lookup"><span data-stu-id="6e0c4-116">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="6e0c4-117">**activityTemplate**</span><span class="sxs-lookup"><span data-stu-id="6e0c4-117">**activityTemplate**</span></span> <br/> |<span data-ttu-id="6e0c4-118">El diseño de la plantilla (elementos de**icono**, **título**y **datos** ) y el tipo de actividad (**tipo de** elemento).</span><span class="sxs-lookup"><span data-stu-id="6e0c4-118">The layout of the template (**icon**, **title**, and **data** elements), and the type of activity (**type** element).</span></span>  <br/> |
   
<span data-ttu-id="6e0c4-119">En la siguiente tabla se describe los elementos secundarios de **activityTemplate**, que se describe el diseño y el tipo de una plantilla.</span><span class="sxs-lookup"><span data-stu-id="6e0c4-119">The following table describes the child elements of **activityTemplate**, which describe the layout and the type of a template.</span></span>
  
|<span data-ttu-id="6e0c4-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="6e0c4-120">**Element**</span></span>|<span data-ttu-id="6e0c4-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6e0c4-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6e0c4-122">**icon**</span><span class="sxs-lookup"><span data-stu-id="6e0c4-122">**icon**</span></span> <br/> |<span data-ttu-id="6e0c4-123">Un token de vínculo, que hace referencia a la dirección URL del icono para ese elemento de la fuente.</span><span class="sxs-lookup"><span data-stu-id="6e0c4-123">A link token, which references the URL for the icon for that feed item.</span></span>  <br/> |
|<span data-ttu-id="6e0c4-124">**title**</span><span class="sxs-lookup"><span data-stu-id="6e0c4-124">**title**</span></span> <br/> |<span data-ttu-id="6e0c4-125">La información necesaria para el elemento de la fuente.</span><span class="sxs-lookup"><span data-stu-id="6e0c4-125">The required information for the feed item.</span></span>  <br/> |
|<span data-ttu-id="6e0c4-126">**type**</span><span class="sxs-lookup"><span data-stu-id="6e0c4-126">**type**</span></span> <br/> |<span data-ttu-id="6e0c4-127">El tipo de actividad, como una actualización de estado, la foto o el documento.</span><span class="sxs-lookup"><span data-stu-id="6e0c4-127">The type of activity, such as an update of status, photo, or document.</span></span>  <br/> |
|<span data-ttu-id="6e0c4-128">**data**</span><span class="sxs-lookup"><span data-stu-id="6e0c4-128">**data**</span></span> <br/> |<span data-ttu-id="6e0c4-129">Información adicional para el elemento de la fuente, como imágenes, texto o vínculos.</span><span class="sxs-lookup"><span data-stu-id="6e0c4-129">Any additional information for the feed item, such as pictures, text, or links.</span></span>  <br/> |
   
<span data-ttu-id="6e0c4-130">Para obtener un ejemplo de la actividad de fuente XML, vea [Ejemplo de XML de fuente de actividad](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="6e0c4-130">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6e0c4-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e0c4-131">See also</span></span>

- [<span data-ttu-id="6e0c4-132">Elemento de la fuente de información general de XML de una actividad</span><span class="sxs-lookup"><span data-stu-id="6e0c4-132">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="6e0c4-133">Elemento activityDetails</span><span class="sxs-lookup"><span data-stu-id="6e0c4-133">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="6e0c4-134">Variables de plantilla</span><span class="sxs-lookup"><span data-stu-id="6e0c4-134">Template Variables</span></span>](template-variables.md)  
- [<span data-ttu-id="6e0c4-135">Instrucciones para mostrar correctamente las actividades</span><span class="sxs-lookup"><span data-stu-id="6e0c4-135">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="6e0c4-136">XML de actividades</span><span class="sxs-lookup"><span data-stu-id="6e0c4-136">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="6e0c4-137">Esquema XML de proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="6e0c4-137">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="6e0c4-138">Desarrollar un proveedor con el esquema XML de OSC</span><span class="sxs-lookup"><span data-stu-id="6e0c4-138">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

