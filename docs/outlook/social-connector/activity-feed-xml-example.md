---
title: Ejemplo XML de fuente de actividad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa50ca36-8d01-4770-9d9c-30a5baa146ff
description: El ejemplo XML de este tema es una cadena XML de fuente de actividad devuelta al conector social (OSC) de Outlook después de llamar al método ISocialSession2::GetActivitiesEx para una red social.
ms.openlocfilehash: bb8af45f25d8ee2897a3a01e2863466aeacec4e8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538329"
---
# <a name="activity-feed-xml-example"></a>Ejemplo XML de fuente de actividad

El ejemplo XML de este tema es una cadena XML de fuente de actividad devuelta al conector social (OSC) de Outlook después de llamar al método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) para una red social. 
  
En el ejemplo se muestra el xml **activityFeed** que contiene las cuatro actividades siguientes, cada una delimitada por el **elemento activityDetails** y que coincide con una plantilla para mostrar: 
  
- Una actualización de imagen de perfil de Melissa Macbeth, cuyo **ownerID** en la red social es 4667647. Esta actividad especifica tres variables de plantilla de tipo **publisherVariable**, **listVariable** y **pictureVariable** (que se incluye en **listVariable**). Estas variables especifican la persona que publicó el elemento de fuente de actividad y la información de la imagen que se va a actualizar (mediante el uso del nombre **,** **valor**, **altText** y elementos secundarios **href** de **pictureVariable**).
    
- Una actualización de imagen de perfil de Michael Affronti cuyo **ownerID** en la red social es 5015012. Similar a la última actividad, esta actividad especifica tres variables de plantilla de tipo **publisherVariable**, **listVariable** y **pictureVariable**. Estas variables especifican la persona que publicó el elemento de fuente de actividad y la información de la imagen que se va a actualizar.
    
- Una actualización de estado de Michael Affronti que muestra el mismo **ownerID** de 5015012 que la última actividad. Esta actividad especifica dos variables de plantilla de tipo **publisherVariable** y **textVariable**. **publisherVariable** especifica la persona que publicó el elemento de fuente de actividad y **textVariable** incluye un **valor de** la línea de estado  `is hiking on Mount Rainier this weekend!`
    
- Una entrada de blog de Michael Affronti que muestra el mismo **ownerID** de 5015012 que las dos últimas actividades. Esta actividad especifica dos variables de plantilla de tipo **publisherVariable** y **linkVariable**. **publisherVariable** especifica la persona que publicó el elemento de fuente de actividades y  **linkVariable** incluye más información (especificada por el **nombre,** el texto y los elementos secundarios de valor de **linkVariable**) sobre la entrada de blog. 
    
Cada una de las cuatro actividades especifica un **valor templateID,** que coincide con una de las tres plantillas especificadas por el **elemento templates.** Cada plantilla está en su propio **elemento activityTemplateContainer,** identificado por un **valor templateID** que también se usa para mostrar una actividad que tiene el mismo **valor templateID.** 
  
Para obtener una descripción detallada de los elementos XML usados en el ejemplo, vea los siguientes temas: 
  
- [Información general sobre XML para un elemento de fuente de actividad](overview-of-xml-for-an-activity-feed-item.md)
    
- [elemento activityDetails](activitydetails-element.md)
    
- [elemento activityTemplateContainer](activitytemplatecontainer-element.md)
    
- [Variables de plantilla](template-variables.md)
    
## <a name="xml-example"></a>Ejemplo XML

En el siguiente ejemplo se muestra **el xml activityFeed** de cuatro actividades: dos actualizaciones de imágenes de perfil, una actualización de estado y una entrada de blog. El XML también especifica tres plantillas de presentación de actividad para mostrar las actividades correspondientes. 
  
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

## <a name="see-also"></a>Vea también

- [Ejemplos XML del proveedor de OSC](osc-provider-xml-examples.md)  
- [XML para actividades](xml-for-activities.md) 
- [Ejemplo XML de funcionalidades](capabilities-xml-example.md)  
- [Ejemplo de XML de amigos](friends-xml-example.md)
- [Outlook Esquema XML del proveedor de Social Connector](outlook-social-connector-provider-xml-schema.md)

