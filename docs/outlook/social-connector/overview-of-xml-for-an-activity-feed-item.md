---
title: Información general sobre XML de un elemento de fuente de actividades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: 'Una fuente de actividades consta de una o más actividades que se producen en una red social. Cada fuente de actividades está representada por un elemento activityFeed y se caracteriza por estos tres fragmentos de información:'
ms.openlocfilehash: 318875aeb6312a3710654d129f3f48139ff7ef12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821226"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a><span data-ttu-id="6b105-104">Información general sobre XML de un elemento de fuente de actividades</span><span class="sxs-lookup"><span data-stu-id="6b105-104">Overview of XML for an activity feed item</span></span>

<span data-ttu-id="6b105-105">Una fuente de actividades consta de una o más actividades que se producen en una red social.</span><span class="sxs-lookup"><span data-stu-id="6b105-105">An activity feed consists of one or more activities occurring on a social network.</span></span> <span data-ttu-id="6b105-106">Cada fuente de actividades está representada por un elemento **activityFeed** y se caracteriza por estos tres fragmentos de información:</span><span class="sxs-lookup"><span data-stu-id="6b105-106">Each activity feed is represented by an **activityFeed** element, and is characterized by these three pieces of information:</span></span> 
  
- <span data-ttu-id="6b105-107">**red**: nombre de la red social desde el que se originaron las actividades.</span><span class="sxs-lookup"><span data-stu-id="6b105-107">**network**—Name of the social network from which the activities originated.</span></span>
    
- <span data-ttu-id="6b105-108">**actividades**: contenedor de actividades que ocurren en la cuenta del usuario ha iniciado la sesión de esa red social.</span><span class="sxs-lookup"><span data-stu-id="6b105-108">**activities**—Container for activities happening on the logged on user's account on that social network.</span></span>
    
- <span data-ttu-id="6b105-109">**plantillas**: contenedor de plantillas que se usan para mostrar el elemento correspondiente de la actividad en **las actividades**.</span><span class="sxs-lookup"><span data-stu-id="6b105-109">**templates**—Container for templates that are used to display the corresponding activity item in **activities**.</span></span>
    
<span data-ttu-id="6b105-110">Para crear un elemento de fuente de actividades, debe cumplir el esquema XML de extensibilidad de proveedor de Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="6b105-110">To create an activity feed item, you must conform to the Outlook Social Connector (OSC) provider extensibility XML schema.</span></span> <span data-ttu-id="6b105-111">La figura 1 muestra la que estructura XML de la fuente de la actividad.</span><span class="sxs-lookup"><span data-stu-id="6b105-111">Figure 1 shows the activity feed XML structure.</span></span>
  
<span data-ttu-id="6b105-112">**En la figura 1. Estructura XML de la fuente de actividades**</span><span class="sxs-lookup"><span data-stu-id="6b105-112">**Figure 1. Activity feed XML structure**</span></span>

![Estructura XML de la actividad](media/odc_ol14_ta_OSC_Fig06.gif)
  
<span data-ttu-id="6b105-114">Para cada elemento de fuente de actividades, las dos partes más importantes de este esquema son los elementos **activityDetails** y **activityTemplateContainer** :</span><span class="sxs-lookup"><span data-stu-id="6b105-114">For each activity feed item, the two most important parts of this schema are the **activityDetails** and **activityTemplateContainer** elements:</span></span> 
  
- <span data-ttu-id="6b105-115">El elemento **activityDetails** almacena información específica para cada elemento, como el nombre del propietario de la actividad o la dirección URL de las imágenes que se cargan de fuente de actividades.</span><span class="sxs-lookup"><span data-stu-id="6b105-115">The **activityDetails** element stores specific information for each activity feed item, such as the activity owner's name or the URL for the pictures uploaded.</span></span> 
    
- <span data-ttu-id="6b105-116">El elemento **activityTemplateContainer** almacena el formato o elemento de la fuente de diseño para cada actividad.</span><span class="sxs-lookup"><span data-stu-id="6b105-116">The **activityTemplateContainer** element stores the format or layout for each activity feed item.</span></span> <span data-ttu-id="6b105-117">Se compone de plantillas, representadas por elementos individuales **activityTemplate** , que se pueden reutilizar para varios elementos de la fuente.</span><span class="sxs-lookup"><span data-stu-id="6b105-117">It consists of templates, represented by individual **activityTemplate** elements, that can be reused for multiple feed items.</span></span> 
    
<span data-ttu-id="6b105-118">Para un elemento de fuente de actividades de individuales, el elemento **activityTemplate** especifica las cuatro piezas de la información siguientes:</span><span class="sxs-lookup"><span data-stu-id="6b105-118">For an individual activity feed item, the **activityTemplate** element specifies the following four pieces of information:</span></span> 
  
- <span data-ttu-id="6b105-119">**icono**— especifica el elemento de fuente de la dirección URL del icono para mostrar la actividad.</span><span class="sxs-lookup"><span data-stu-id="6b105-119">**icon**—Specifies the URL for the icon to display the activity feed item.</span></span>
    
- <span data-ttu-id="6b105-120">**título**: describe la actividad fuente item.</span><span class="sxs-lookup"><span data-stu-id="6b105-120">**title**—Describes the activity feed item.</span></span>
    
- <span data-ttu-id="6b105-121">**tipo**: especifica el tipo de actividad, como un estado, fotografía o actualización de documentos.</span><span class="sxs-lookup"><span data-stu-id="6b105-121">**type**—Specifies the type of activity, such as a status, photo, or document update.</span></span>
    
- <span data-ttu-id="6b105-122">**datos**— especifica cualquier información adicional que se muestra con el elemento de fuente de actividades.</span><span class="sxs-lookup"><span data-stu-id="6b105-122">**data**—Specifies any extra information displayed with activity feed item.</span></span>
    
> [!TIP]
> <span data-ttu-id="6b105-123">El icono que se muestra en la fuente de actividades siempre es el mismo que el icono de proveedor devuelto por la propiedad **ISocialProvider::SocialNetworkIcon** .</span><span class="sxs-lookup"><span data-stu-id="6b105-123">The icon displayed in the activity feed is always the same as the provider icon returned by the **ISocialProvider::SocialNetworkIcon** property.</span></span> 
  
<span data-ttu-id="6b105-124">Consulte los siguientes temas para obtener más información sobre el elemento **activityDetails** , el elemento **activityTemplateContainer** , los tokens de plantilla y variables de plantilla:</span><span class="sxs-lookup"><span data-stu-id="6b105-124">See the following topics for more information about the **activityDetails** element, the **activityTemplateContainer** element, template tokens, and template variables:</span></span> 
  
- [<span data-ttu-id="6b105-125">Elemento activityDetails</span><span class="sxs-lookup"><span data-stu-id="6b105-125">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="6b105-126">Elemento activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="6b105-126">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="6b105-127">Variables de plantilla</span><span class="sxs-lookup"><span data-stu-id="6b105-127">Template Variables</span></span>](template-variables.md)
    
- [<span data-ttu-id="6b105-128">Instrucciones para mostrar correctamente las actividades</span><span class="sxs-lookup"><span data-stu-id="6b105-128">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)
    
<span data-ttu-id="6b105-129">Para obtener un ejemplo de la actividad de fuente XML, vea [Ejemplo de XML de fuente de actividad](activity-feed-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="6b105-129">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6b105-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b105-130">See also</span></span>

- [<span data-ttu-id="6b105-131">XML de actividades</span><span class="sxs-lookup"><span data-stu-id="6b105-131">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="6b105-132">Esquema XML de proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="6b105-132">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="6b105-133">Desarrollar un proveedor con el esquema XML de OSC</span><span class="sxs-lookup"><span data-stu-id="6b105-133">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

