---
title: Ejemplo xml de fuente de actividades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa50ca36-8d01-4770-9d9c-30a5baa146ff
description: El ejemplo XML de este tema es una cadena XML de fuente de actividades devuelta al conector social de Outlook (OSC) después de llamar al método ISocialSession2::GetActivitiesEx para una red social.
ms.openlocfilehash: bb8af45f25d8ee2897a3a01e2863466aeacec4e8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538329"
---
# <a name="activity-feed-xml-example"></a><span data-ttu-id="172ee-103">Ejemplo xml de fuente de actividades</span><span class="sxs-lookup"><span data-stu-id="172ee-103">Activity Feed XML Example</span></span>

<span data-ttu-id="172ee-104">El ejemplo XML de este tema es una cadena XML de fuente de actividades devuelta al conector social de Outlook (OSC) después de llamar al [método ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) para una red social.</span><span class="sxs-lookup"><span data-stu-id="172ee-104">The XML example in this topic is an activity feed XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method for a social network.</span></span> 
  
<span data-ttu-id="172ee-105">En el ejemplo se muestra el xml **activityFeed** que contiene las cuatro actividades siguientes, cada una delimitada por el elemento **activityDetails** y la coincidencia de una plantilla para mostrar:</span><span class="sxs-lookup"><span data-stu-id="172ee-105">The example shows the **activityFeed** XML that contains the following four activities, each delimited by the **activityDetails** element and matching a template for display purposes:</span></span> 
  
- <span data-ttu-id="172ee-106">Una actualización de imagen de perfil de Melissa Macbeth, cuyo **ownerID** en la red social es 4667647.</span><span class="sxs-lookup"><span data-stu-id="172ee-106">A profile picture update by Melissa Macbeth, whose **ownerID** on the social network is 4667647.</span></span> <span data-ttu-id="172ee-107">Esta actividad especifica tres variables de plantilla de tipo **publisherVariable**, **listVariable** e **pictureVariable** (que se incluye en **listVariable**).</span><span class="sxs-lookup"><span data-stu-id="172ee-107">This activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable** (which is enclosed in **listVariable**).</span></span> <span data-ttu-id="172ee-108">Estas variables especifican la persona que publicó el elemento de fuente de actividades y la información de la imagen que se va a actualizar (con el nombre **,** **el** valor , **altText** y los elementos secundarios **href** de **pictureVariable**).</span><span class="sxs-lookup"><span data-stu-id="172ee-108">These variables specify the person who published the activity feed item, and information for the picture to be updated (by using the **name**, **value**, **altText**, and **href** child elements of **pictureVariable**).</span></span>
    
- <span data-ttu-id="172ee-109">Una actualización de imagen de perfil de Michael Affronti cuyo **ownerID** en la red social es 5015012.</span><span class="sxs-lookup"><span data-stu-id="172ee-109">A profile picture update by Michael Affronti whose **ownerID** on the social network is 5015012.</span></span> <span data-ttu-id="172ee-110">Similar a la última actividad, esta actividad especifica tres variables de plantilla de tipo **publisherVariable**, **listVariable** y **pictureVariable**.</span><span class="sxs-lookup"><span data-stu-id="172ee-110">Similar to the last activity, this activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable**.</span></span> <span data-ttu-id="172ee-111">Estas variables especifican la persona que publicó el elemento de fuente de actividades y la información de la imagen que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="172ee-111">These variables specify the person who published the activity feed item and information for the picture to be updated.</span></span>
    
- <span data-ttu-id="172ee-112">Una actualización de estado de Michael Affronti, que muestra el mismo **ownerID** de 5015012 que la última actividad.</span><span class="sxs-lookup"><span data-stu-id="172ee-112">A status update by Michael Affronti, showing the same **ownerID** of 5015012 as the last activity.</span></span> <span data-ttu-id="172ee-113">Esta actividad especifica dos variables de plantilla de tipo **publisherVariable** y **textVariable**.</span><span class="sxs-lookup"><span data-stu-id="172ee-113">This activity specifies two template variables of type **publisherVariable** and **textVariable**.</span></span> <span data-ttu-id="172ee-114">**publisherVariable** especifica la persona que publicó el elemento de fuente de actividades y **textVariable** incluye un **valor** de la línea de estado.  `is hiking on Mount Rainier this weekend!`</span><span class="sxs-lookup"><span data-stu-id="172ee-114">**publisherVariable** specifies the person who published the activity feed item, and **textVariable** includes a **value** of the status line  `is hiking on Mount Rainier this weekend!`</span></span>
    
- <span data-ttu-id="172ee-115">Una entrada de blog de Michael Affronti que muestra el mismo **ownerID** de 5015012 que las dos últimas actividades.</span><span class="sxs-lookup"><span data-stu-id="172ee-115">A blog post by Michael Affronti, showing the same **ownerID** of 5015012 as the last two activities.</span></span> <span data-ttu-id="172ee-116">Esta actividad especifica dos variables de plantilla de tipo **publisherVariable** y **linkVariable**.</span><span class="sxs-lookup"><span data-stu-id="172ee-116">This activity specifies two template variables of type **publisherVariable** and **linkVariable**.</span></span> <span data-ttu-id="172ee-117">**publisherVariable** especifica la persona que publicó el elemento de fuente de actividades y  **linkVariable** incluye más información (especificada por el **nombre,** el texto y los elementos secundarios de valor de **linkVariable**) sobre la entrada de blog. </span><span class="sxs-lookup"><span data-stu-id="172ee-117">**publisherVariable** specifies the person who published the activity feed item, and **linkVariable** includes further information (specified by the **name**, **text**, and **value** child elements of **linkVariable**) about the blog post.</span></span>
    
<span data-ttu-id="172ee-118">Cada una de las cuatro actividades especifica un **valor templateID,** que coincide con una de las tres plantillas especificadas por el **elemento templates.**</span><span class="sxs-lookup"><span data-stu-id="172ee-118">Each of the four activities specifies a **templateID** value, which matches one of the three templates specified by the **templates** element.</span></span> <span data-ttu-id="172ee-119">Cada plantilla está en su propio **elemento activityTemplateContainer,** identificado por un valor **templateID** que también se usa para mostrar una actividad que tiene el mismo **valor templateID.**</span><span class="sxs-lookup"><span data-stu-id="172ee-119">Each template is in its own **activityTemplateContainer** element, identified by a **templateID** value that is also used to display an activity that has the same **templateID** value.</span></span> 
  
<span data-ttu-id="172ee-120">Para obtener una descripción detallada de los elementos XML usados en el ejemplo, vea los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="172ee-120">For a detailed description of the XML elements used in the example, see the following topics:</span></span> 
  
- [<span data-ttu-id="172ee-121">Información general sobre XML para un elemento de fuente de actividades</span><span class="sxs-lookup"><span data-stu-id="172ee-121">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)
    
- [<span data-ttu-id="172ee-122">Elemento activityDetails</span><span class="sxs-lookup"><span data-stu-id="172ee-122">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="172ee-123">Elemento activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="172ee-123">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="172ee-124">Variables de plantilla</span><span class="sxs-lookup"><span data-stu-id="172ee-124">Template Variables</span></span>](template-variables.md)
    
## <a name="xml-example"></a><span data-ttu-id="172ee-125">Ejemplo de XML</span><span class="sxs-lookup"><span data-stu-id="172ee-125">XML example</span></span>

<span data-ttu-id="172ee-126">En el siguiente ejemplo se muestra el XML **activityFeed** de cuatro actividades: dos actualizaciones de imágenes de perfil, una actualización de estado y una entrada de blog.</span><span class="sxs-lookup"><span data-stu-id="172ee-126">The following example shows the **activityFeed** XML of four activities: two profile picture updates, a status update, and a blog post.</span></span> <span data-ttu-id="172ee-127">El XML también especifica tres plantillas para mostrar actividades para mostrar las actividades correspondientes.</span><span class="sxs-lookup"><span data-stu-id="172ee-127">The XML also specifies three activity display templates for displaying the corresponding activities.</span></span> 
  
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
          <profileUrl>https://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</value>
              <altText>Melissa Macbeth</altText>
              <href>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</href>
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
          <profileUrl>https://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</value>
              <altText>Michael Affronti</altText>
              <href>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</href>
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
          <profileUrl>https://www.contoso.com</profileUrl>
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
          <profileUrl>https://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="linkVariable">
          <name>blogPost</name>
          <text>Connect your Inbox to Facebook and Windows Live with the Outlook Social Connector</text>
          <value>https://blogs.office.com/b/office_blog/archive/2010/07/13/connect-to-facebook-and-windows-live-with-the-outlook-social-connector.aspx</value>
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
        <icon>https://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>2</templateID>
      <activityTemplate>
        <type>Status Update</type>
        <title>{publisher:Publisher}: {text:statusText}</title>
                <data></data>
        <icon>https://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>3</templateID>
      <activityTemplate>
        <type>Other</type>
        <title>{publisher:Publisher} wrote a new blog post {link:blogPost}</title>
                <data></data>
        <icon>https://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
  </templates>
</activityFeed>

```

## <a name="see-also"></a><span data-ttu-id="172ee-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="172ee-128">See also</span></span>

- [<span data-ttu-id="172ee-129">Ejemplos xml del proveedor de OSC</span><span class="sxs-lookup"><span data-stu-id="172ee-129">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="172ee-130">XML para actividades</span><span class="sxs-lookup"><span data-stu-id="172ee-130">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="172ee-131">Ejemplo xml de funcionalidades</span><span class="sxs-lookup"><span data-stu-id="172ee-131">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="172ee-132">Ejemplo xml de amigos</span><span class="sxs-lookup"><span data-stu-id="172ee-132">Friends XML Example</span></span>](friends-xml-example.md)
- [<span data-ttu-id="172ee-133">Esquema XML del proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="172ee-133">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

