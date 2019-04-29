---
title: Información general sobre XML de un elemento de fuente de actividades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: 'Una fuente de actividades consta de una o varias actividades que se producen en una red social. Cada fuente de actividades está representada por un elemento activityFeed y se caracteriza por estos tres datos de información:'
ms.openlocfilehash: 971c54cf69a65bebbe4fd04e8608e88b89145bb4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439950"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a><span data-ttu-id="61ed1-104">Información general sobre XML de un elemento de fuente de actividades</span><span class="sxs-lookup"><span data-stu-id="61ed1-104">Overview of XML for an activity feed item</span></span>

<span data-ttu-id="61ed1-105">Una fuente de actividades consta de una o varias actividades que se producen en una red social.</span><span class="sxs-lookup"><span data-stu-id="61ed1-105">An activity feed consists of one or more activities occurring on a social network.</span></span> <span data-ttu-id="61ed1-106">Cada fuente de actividades está representada por un elemento **activityFeed** y se caracteriza por estos tres datos de información:</span><span class="sxs-lookup"><span data-stu-id="61ed1-106">Each activity feed is represented by an **activityFeed** element, and is characterized by these three pieces of information:</span></span> 
  
- <span data-ttu-id="61ed1-107">**red**: nombre de la red social desde la que se originaron las actividades.</span><span class="sxs-lookup"><span data-stu-id="61ed1-107">**network**—Name of the social network from which the activities originated.</span></span>
    
- <span data-ttu-id="61ed1-108">**actividades**: contenedor para actividades que ocurren en la cuenta del usuario que ha iniciado sesión en esa red social.</span><span class="sxs-lookup"><span data-stu-id="61ed1-108">**activities**—Container for activities happening on the logged on user's account on that social network.</span></span>
    
- <span data-ttu-id="61ed1-109">**plantillas**: contenedor para plantillas que se usan para mostrar el elemento de actividad correspondiente en **actividades**.</span><span class="sxs-lookup"><span data-stu-id="61ed1-109">**templates**—Container for templates that are used to display the corresponding activity item in **activities**.</span></span>
    
<span data-ttu-id="61ed1-110">Para crear un elemento de fuente de actividad, debe cumplir con el esquema XML de extensibilidad del proveedor de Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="61ed1-110">To create an activity feed item, you must conform to the Outlook Social Connector (OSC) provider extensibility XML schema.</span></span> <span data-ttu-id="61ed1-111">En la figura 1 se muestra la estructura XML de la fuente de actividades.</span><span class="sxs-lookup"><span data-stu-id="61ed1-111">Figure 1 shows the activity feed XML structure.</span></span>
  
<span data-ttu-id="61ed1-112">**Figura 1. Estructura XML de la fuente de actividades**</span><span class="sxs-lookup"><span data-stu-id="61ed1-112">**Figure 1. Activity feed XML structure**</span></span>

![Estructura XML de la actividad](media/odc_ol14_ta_OSC_Fig06.gif)
  
<span data-ttu-id="61ed1-114">Para cada elemento de la fuente de actividades, las dos partes más importantes de este esquema son los elementos **activityDetails** y **activityTemplateContainer** :</span><span class="sxs-lookup"><span data-stu-id="61ed1-114">For each activity feed item, the two most important parts of this schema are the **activityDetails** and **activityTemplateContainer** elements:</span></span> 
  
- <span data-ttu-id="61ed1-115">El elemento **activityDetails** almacena información específica para cada elemento de la fuente de actividades, como el nombre del propietario de la actividad o la dirección URL de las imágenes que se cargan.</span><span class="sxs-lookup"><span data-stu-id="61ed1-115">The **activityDetails** element stores specific information for each activity feed item, such as the activity owner's name or the URL for the pictures uploaded.</span></span> 
    
- <span data-ttu-id="61ed1-116">El elemento **activityTemplateContainer** almacena el formato o el diseño de cada elemento de la fuente de actividades.</span><span class="sxs-lookup"><span data-stu-id="61ed1-116">The **activityTemplateContainer** element stores the format or layout for each activity feed item.</span></span> <span data-ttu-id="61ed1-117">Consta de plantillas, representadas por elementos **activityTemplate** individuales, que se pueden volver a usar para varios elementos de fuente.</span><span class="sxs-lookup"><span data-stu-id="61ed1-117">It consists of templates, represented by individual **activityTemplate** elements, that can be reused for multiple feed items.</span></span> 
    
<span data-ttu-id="61ed1-118">Para un elemento de fuente de actividad individual, el elemento **activityTemplate** especifica los cuatro datos siguientes:</span><span class="sxs-lookup"><span data-stu-id="61ed1-118">For an individual activity feed item, the **activityTemplate** element specifies the following four pieces of information:</span></span> 
  
- <span data-ttu-id="61ed1-119">**icono**: especifica la dirección URL del icono para mostrar el elemento de fuente de actividad.</span><span class="sxs-lookup"><span data-stu-id="61ed1-119">**icon**—Specifies the URL for the icon to display the activity feed item.</span></span>
    
- <span data-ttu-id="61ed1-120">**title**: describe el elemento fuente de actividades.</span><span class="sxs-lookup"><span data-stu-id="61ed1-120">**title**—Describes the activity feed item.</span></span>
    
- <span data-ttu-id="61ed1-121">**tipo**: especifica el tipo de actividad (por ejemplo, una actualización de estado, foto o documento).</span><span class="sxs-lookup"><span data-stu-id="61ed1-121">**type**—Specifies the type of activity, such as a status, photo, or document update.</span></span>
    
- <span data-ttu-id="61ed1-122">**datos**: especifica la información adicional que se muestra con el elemento de la fuente de actividades.</span><span class="sxs-lookup"><span data-stu-id="61ed1-122">**data**—Specifies any extra information displayed with activity feed item.</span></span>
    
> [!TIP]
> <span data-ttu-id="61ed1-123">El icono que se muestra en la fuente de actividades es siempre el mismo que el icono del proveedor devuelto por la propiedad **ISocialProvider:: SocialNetworkIcon** .</span><span class="sxs-lookup"><span data-stu-id="61ed1-123">The icon displayed in the activity feed is always the same as the provider icon returned by the **ISocialProvider::SocialNetworkIcon** property.</span></span> 
  
<span data-ttu-id="61ed1-124">Vea los temas siguientes para obtener más información sobre el elemento **activityDetails** , el elemento **activityTemplateContainer** , los tokens de plantilla y las variables de plantilla:</span><span class="sxs-lookup"><span data-stu-id="61ed1-124">See the following topics for more information about the **activityDetails** element, the **activityTemplateContainer** element, template tokens, and template variables:</span></span> 
  
- [<span data-ttu-id="61ed1-125">Elemento activityDetails</span><span class="sxs-lookup"><span data-stu-id="61ed1-125">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="61ed1-126">Elemento activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="61ed1-126">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="61ed1-127">Variables de plantilla</span><span class="sxs-lookup"><span data-stu-id="61ed1-127">Template Variables</span></span>](template-variables.md)
    
- [<span data-ttu-id="61ed1-128">Directrices para mostrar correctamente las actividades</span><span class="sxs-lookup"><span data-stu-id="61ed1-128">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)
    
<span data-ttu-id="61ed1-129">Para obtener un ejemplo de XML de fuente de actividades, consulte ejemplo de XML de la [fuente de actividades](activity-feed-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="61ed1-129">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="61ed1-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="61ed1-130">See also</span></span>

- [<span data-ttu-id="61ed1-131">XML para actividades</span><span class="sxs-lookup"><span data-stu-id="61ed1-131">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="61ed1-132">Esquema XML del proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="61ed1-132">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="61ed1-133">Desarrollo de un proveedor con el esquema XML de OSC</span><span class="sxs-lookup"><span data-stu-id="61ed1-133">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

