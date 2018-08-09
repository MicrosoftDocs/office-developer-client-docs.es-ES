---
title: Ejemplo de XML de fuentes de actividades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa50ca36-8d01-4770-9d9c-30a5baa146ff
description: El ejemplo de XML de este tema es que una actividad fuente cadena XML devuelta a Outlook Social Connector (OSC) después de que llama al método ISocialSession2::GetActivitiesEx para una red social.
ms.openlocfilehash: ab27ddfad5044994a19bb32759994a0e98c39ae6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821078"
---
# <a name="activity-feed-xml-example"></a><span data-ttu-id="7e0f6-103">Ejemplo de XML de fuentes de actividades</span><span class="sxs-lookup"><span data-stu-id="7e0f6-103">Activity Feed XML Example</span></span>

<span data-ttu-id="7e0f6-104">El ejemplo de XML de este tema es una cadena XML devuelta a Outlook Social Connector (OSC) después de que llama al método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) para una red social de fuente de actividades.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-104">The XML example in this topic is an activity feed XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method for a social network.</span></span> 
  
<span data-ttu-id="7e0f6-105">En el ejemplo se muestra el XML que contiene las siguientes cuatro actividades **activityFeed** , cada uno de ellos delimitado por el elemento **activityDetails** y que coincidan con una plantilla para mostrar con fines:</span><span class="sxs-lookup"><span data-stu-id="7e0f6-105">The example shows the **activityFeed** XML that contains the following four activities, each delimited by the **activityDetails** element and matching a template for display purposes:</span></span> 
  
- <span data-ttu-id="7e0f6-106">Para actualizar una imagen de perfil, Melissa Macbeth, cuyo **ownerID** en la red social es 4667647.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-106">A profile picture update by Melissa Macbeth, whose **ownerID** on the social network is 4667647.</span></span> <span data-ttu-id="7e0f6-107">Esta actividad especifica tres variables de plantilla de tipo **publisherVariable**, **listVariable**y **pictureVariable** (que está delimitado por **listVariable**).</span><span class="sxs-lookup"><span data-stu-id="7e0f6-107">This activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable** (which is enclosed in **listVariable**).</span></span> <span data-ttu-id="7e0f6-108">Estas variables especifican a la persona que publicó la actividad fuente elemento y la información de la imagen que se van a actualizar (mediante el uso de los elementos secundarios de **nombre**, **valor**, **altText**y **href** de **pictureVariable**).</span><span class="sxs-lookup"><span data-stu-id="7e0f6-108">These variables specify the person who published the activity feed item, and information for the picture to be updated (by using the **name**, **value**, **altText**, and **href** child elements of **pictureVariable**).</span></span>
    
- <span data-ttu-id="7e0f6-109">Para actualizar una imagen de perfil, Michael Affronti cuyo **ownerID** en la red social es 5015012.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-109">A profile picture update by Michael Affronti whose **ownerID** on the social network is 5015012.</span></span> <span data-ttu-id="7e0f6-110">Al igual que la última actividad, esta actividad especifica tres variables de plantilla de tipo **publisherVariable**, **listVariable**y **pictureVariable**.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-110">Similar to the last activity, this activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable**.</span></span> <span data-ttu-id="7e0f6-111">Estas variables especifican a la persona que publicó la actividad fuente de elemento y la información de la imagen que se van a actualizar.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-111">These variables specify the person who published the activity feed item and information for the picture to be updated.</span></span>
    
- <span data-ttu-id="7e0f6-112">Una actualización de estado por Michael Affronti, que muestra el mismo **ownerID** de 5015012 como la última actividad.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-112">A status update by Michael Affronti, showing the same **ownerID** of 5015012 as the last activity.</span></span> <span data-ttu-id="7e0f6-113">Esta actividad especifica dos variables de plantilla de tipo **publisherVariable** y **textVariable**.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-113">This activity specifies two template variables of type **publisherVariable** and **textVariable**.</span></span> <span data-ttu-id="7e0f6-114">**publisherVariable** especifica a la persona que publicó el elemento de fuente de actividades y **textVariable** incluye un **valor** de la línea de estado`is hiking on Mount Rainier this weekend!`</span><span class="sxs-lookup"><span data-stu-id="7e0f6-114">**publisherVariable** specifies the person who published the activity feed item, and **textVariable** includes a **value** of the status line  `is hiking on Mount Rainier this weekend!`</span></span>
    
- <span data-ttu-id="7e0f6-115">Una entrada de blog por Michael Affronti, que muestra el mismo **ownerID** de 5015012 como las actividades de dos por última vez.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-115">A blog post by Michael Affronti, showing the same **ownerID** of 5015012 as the last two activities.</span></span> <span data-ttu-id="7e0f6-116">Esta actividad especifica dos variables de plantilla de tipo **publisherVariable** y **linkVariable**.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-116">This activity specifies two template variables of type **publisherVariable** and **linkVariable**.</span></span> <span data-ttu-id="7e0f6-117">**publisherVariable** especifica el elemento de fuente de la persona que publicó la actividad y **linkVariable** incluye más información (especificada por los elementos secundarios de **nombre**, el **texto**y el **valor** de **linkVariable**) acerca de la entrada de blog.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-117">**publisherVariable** specifies the person who published the activity feed item, and **linkVariable** includes further information (specified by the **name**, **text**, and **value** child elements of **linkVariable**) about the blog post.</span></span>
    
<span data-ttu-id="7e0f6-118">Cada una de las actividades de cuatro especifica un valor de **identificador de plantilla** , que coincide con una de las tres plantillas especificadas por el elemento de **plantillas** .</span><span class="sxs-lookup"><span data-stu-id="7e0f6-118">Each of the four activities specifies a **templateID** value, which matches one of the three templates specified by the **templates** element.</span></span> <span data-ttu-id="7e0f6-119">Cada plantilla está en su propio elemento **activityTemplateContainer** , identificado por un valor de **identificador de plantilla** que también se usa para mostrar una actividad que tiene el mismo valor de **identificador de plantilla** .</span><span class="sxs-lookup"><span data-stu-id="7e0f6-119">Each template is in its own **activityTemplateContainer** element, identified by a **templateID** value that is also used to display an activity that has the same **templateID** value.</span></span> 
  
<span data-ttu-id="7e0f6-120">Para obtener una descripción detallada de los elementos XML utilizados en el ejemplo, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="7e0f6-120">For a detailed description of the XML elements used in the example, see the following topics:</span></span> 
  
- [<span data-ttu-id="7e0f6-121">Elemento de la fuente de información general de XML de una actividad</span><span class="sxs-lookup"><span data-stu-id="7e0f6-121">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)
    
- [<span data-ttu-id="7e0f6-122">Elemento activityDetails</span><span class="sxs-lookup"><span data-stu-id="7e0f6-122">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="7e0f6-123">Elemento activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="7e0f6-123">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="7e0f6-124">Variables de plantilla</span><span class="sxs-lookup"><span data-stu-id="7e0f6-124">Template Variables</span></span>](template-variables.md)
    
## <a name="xml-example"></a><span data-ttu-id="7e0f6-125">Ejemplo de XML</span><span class="sxs-lookup"><span data-stu-id="7e0f6-125">XML example</span></span>

<span data-ttu-id="7e0f6-126">En el ejemplo siguiente se muestra el XML de cuatro actividades **activityFeed** : dos perfiles actualizaciones de imagen, una actualización de estado y una entrada de blog.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-126">The following example shows the **activityFeed** XML of four activities: two profile picture updates, a status update, and a blog post.</span></span> <span data-ttu-id="7e0f6-127">El código XML también especifica tres plantillas para mostrar de actividad para mostrar las actividades correspondientes.</span><span class="sxs-lookup"><span data-stu-id="7e0f6-127">The XML also specifies three activity display templates for displaying the corresponding activities.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<activityFeed xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
  <network>Contoso</network>
  <activities>
    <activityDetails>
      <ownerID>4667647</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a31</objectID>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <publishDate>2010-03-05T17:19:57</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>4667647</id>
          <nameHint>Melissa Macbeth</nameHint>
          <profileUrl>http://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</value>
              <altText>Melissa Macbeth</altText>
              <href>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</href>
            </simpleTemplateVariable>
          </listItems>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a32</objectID>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <publishDate>2010-03-08T17:19:57</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>http://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</value>
              <altText>Michael Affronti</altText>
              <href>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</href>
            </simpleTemplateVariable>
          </listItems>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a38</objectID>
      <applicationID>2</applicationID>
      <templateID>2</templateID>
      <publishDate>2010-03-08T18:30:00</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>http://www.contoso.com</profileUrl>
        </templateVariable>
        <templateVariable type="textVariable">
          <name>statusText</name>
          <value>is hiking on Mount Rainier this weekend!</value>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a39</objectID>
      <applicationID>2</applicationID>
      <templateID>3</templateID>
      <publishDate>2010-03-04T15:00:00</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>http://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="linkVariable">
          <name>blogPost</name>
          <text>Connect your Inbox to Facebook and Windows Live with the Outlook Social Connector</text>
          <value>http://blogs.office.com/b/office_blog/archive/2010/07/13/connect-to-facebook-and-windows-live-with-the-outlook-social-connector.aspx</value>
        </templateVariable>
      </templateVariables>
    </activityDetails>
  </activities>
  <templates>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <activityTemplate>
        <type>Photo</type>
        <title>{publisher:Publisher} has a new profile photo: </title>
        <data>{list:ProfilePhoto({picture:Photo})}</data>
        <icon>http://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>2</templateID>
      <activityTemplate>
        <type>Status Update</type>
        <title>{publisher:Publisher}: {text:statusText}</title>
                <data></data>
        <icon>http://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>3</templateID>
      <activityTemplate>
        <type>Other</type>
        <title>{publisher:Publisher} wrote a new blog post {link:blogPost}</title>
                <data></data>
        <icon>http://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
  </templates>
</activityFeed>

```

## <a name="see-also"></a><span data-ttu-id="7e0f6-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e0f6-128">See also</span></span>

- [<span data-ttu-id="7e0f6-129">Ejemplos XML de proveedor OSC</span><span class="sxs-lookup"><span data-stu-id="7e0f6-129">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="7e0f6-130">XML de actividades</span><span class="sxs-lookup"><span data-stu-id="7e0f6-130">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="7e0f6-131">Ejemplo de XML de capacidades</span><span class="sxs-lookup"><span data-stu-id="7e0f6-131">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="7e0f6-132">Ejemplo de XML de amigos</span><span class="sxs-lookup"><span data-stu-id="7e0f6-132">Friends XML Example</span></span>](friends-xml-example.md)
- [<span data-ttu-id="7e0f6-133">Esquema XML de proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="7e0f6-133">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

