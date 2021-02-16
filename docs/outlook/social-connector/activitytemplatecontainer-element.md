---
title: Elemento activityTemplateContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: Un elemento activityTemplateContainer es una plantilla que te permite dar formato a los elementos de fuente de actividades y reutilizar XML que especifica un diseño.
ms.openlocfilehash: c2540b1d871e440e8f8f343a1788194c32d7dcc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413720"
---
# <a name="activitytemplatecontainer-element"></a><span data-ttu-id="2a9fd-103">Elemento activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="2a9fd-103">activityTemplateContainer Element</span></span>

<span data-ttu-id="2a9fd-104">Un **elemento activityTemplateContainer** es una plantilla que te permite dar formato a los elementos de la fuente de actividades y reutilizar xml que especifica un diseño.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-104">An **activityTemplateContainer** element is a template that allows you to format your activity feed items and reuse XML that specifies a layout.</span></span> <span data-ttu-id="2a9fd-105">Usa id. (**applicationID** y **templateID**) para hacer coincidir un elemento de fuente (**activityDetails**) con una plantilla (**activityTemplateContainer**).</span><span class="sxs-lookup"><span data-stu-id="2a9fd-105">Use IDs (**applicationID** and **templateID**) to match a feed item (**activityDetails**) to a template (**activityTemplateContainer**).</span></span> <span data-ttu-id="2a9fd-106">Almacena los datos de diseño como parte del **elemento activityTemplate.**</span><span class="sxs-lookup"><span data-stu-id="2a9fd-106">Store the layout data as part of the **activityTemplate** element.</span></span> <span data-ttu-id="2a9fd-107">Para hacer referencia a datos que se extrajo del elemento de fuente de actividad individual, use variables de plantilla como marcadores de posición para información como personas, vínculos y texto.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-107">To reference data that is pulled from the individual activity feed item, use template variables as placeholders for information such as people, links, and text.</span></span> 
  
<span data-ttu-id="2a9fd-108">En la tabla siguiente se describen los tres elementos que requiere **el elemento activityTemplateContainer.**</span><span class="sxs-lookup"><span data-stu-id="2a9fd-108">The following table describes the three elements that the **activityTemplateContainer** element requires.</span></span> 
  
|<span data-ttu-id="2a9fd-109">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2a9fd-109">**Element**</span></span>|<span data-ttu-id="2a9fd-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2a9fd-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2a9fd-111">**applicationID**</span><span class="sxs-lookup"><span data-stu-id="2a9fd-111">**applicationID**</span></span> <br/> |<span data-ttu-id="2a9fd-112">Uno de los dos identificadores únicos que se usan para hacer coincidir el elemento de fuente con su plantilla.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-112">One of two unique IDs that are used to match the feed item with its template.</span></span> <span data-ttu-id="2a9fd-113">Si tiene varias aplicaciones u otras agrupaciones, puede usarse como organizador de plantillas de primer nivel.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-113">If you have multiple applications or other groupings, this can be used as a first-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="2a9fd-114">**templateID**</span><span class="sxs-lookup"><span data-stu-id="2a9fd-114">**templateID**</span></span> <br/> |<span data-ttu-id="2a9fd-115">El segundo identificador único que se usa para hacer coincidir el elemento de fuente con su plantilla.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-115">The second unique ID that is used to match the feed item with its template.</span></span> <span data-ttu-id="2a9fd-116">Puede usarse como organizador de plantillas de segundo nivel.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-116">This can be used as a second-tier template organizer.</span></span>  <br/> |
|<span data-ttu-id="2a9fd-117">**activityTemplate**</span><span class="sxs-lookup"><span data-stu-id="2a9fd-117">**activityTemplate**</span></span> <br/> |<span data-ttu-id="2a9fd-118">El diseño de la plantilla **(icono,** **título** y elementos **de** datos) y el tipo de actividad **(elemento de** tipo).</span><span class="sxs-lookup"><span data-stu-id="2a9fd-118">The layout of the template (**icon**, **title**, and **data** elements), and the type of activity (**type** element).</span></span>  <br/> |
   
<span data-ttu-id="2a9fd-119">En la tabla siguiente se describen los elementos secundarios de **activityTemplate**, que describen el diseño y el tipo de una plantilla.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-119">The following table describes the child elements of **activityTemplate**, which describe the layout and the type of a template.</span></span>
  
|<span data-ttu-id="2a9fd-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2a9fd-120">**Element**</span></span>|<span data-ttu-id="2a9fd-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2a9fd-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2a9fd-122">**icon**</span><span class="sxs-lookup"><span data-stu-id="2a9fd-122">**icon**</span></span> <br/> |<span data-ttu-id="2a9fd-123">Un token de vínculo, que hace referencia a la dirección URL del icono de ese elemento de fuente.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-123">A link token, which references the URL for the icon for that feed item.</span></span>  <br/> |
|<span data-ttu-id="2a9fd-124">**title**</span><span class="sxs-lookup"><span data-stu-id="2a9fd-124">**title**</span></span> <br/> |<span data-ttu-id="2a9fd-125">La información necesaria para el elemento de fuente.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-125">The required information for the feed item.</span></span>  <br/> |
|<span data-ttu-id="2a9fd-126">**tipo**</span><span class="sxs-lookup"><span data-stu-id="2a9fd-126">**type**</span></span> <br/> |<span data-ttu-id="2a9fd-127">El tipo de actividad, como una actualización de estado, foto o documento.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-127">The type of activity, such as an update of status, photo, or document.</span></span>  <br/> |
|<span data-ttu-id="2a9fd-128">**data**</span><span class="sxs-lookup"><span data-stu-id="2a9fd-128">**data**</span></span> <br/> |<span data-ttu-id="2a9fd-129">Cualquier información adicional para el elemento de fuente, como imágenes, texto o vínculos.</span><span class="sxs-lookup"><span data-stu-id="2a9fd-129">Any additional information for the feed item, such as pictures, text, or links.</span></span>  <br/> |
   
<span data-ttu-id="2a9fd-130">Para obtener un ejemplo de XML de fuente de actividades, vea [el ejemplo XML de fuente de actividades](activity-feed-xml-example.md)</span><span class="sxs-lookup"><span data-stu-id="2a9fd-130">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2a9fd-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2a9fd-131">See also</span></span>

- [<span data-ttu-id="2a9fd-132">Información general sobre XML para un elemento de fuente de actividades</span><span class="sxs-lookup"><span data-stu-id="2a9fd-132">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="2a9fd-133">Elemento activityDetails</span><span class="sxs-lookup"><span data-stu-id="2a9fd-133">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="2a9fd-134">Variables de plantilla</span><span class="sxs-lookup"><span data-stu-id="2a9fd-134">Template Variables</span></span>](template-variables.md)  
- [<span data-ttu-id="2a9fd-135">Directrices para mostrar actividades correctamente</span><span class="sxs-lookup"><span data-stu-id="2a9fd-135">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="2a9fd-136">XML para actividades</span><span class="sxs-lookup"><span data-stu-id="2a9fd-136">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="2a9fd-137">Esquema XML del proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="2a9fd-137">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="2a9fd-138">Desarrollo de un proveedor con el esquema XML de OSC</span><span class="sxs-lookup"><span data-stu-id="2a9fd-138">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

