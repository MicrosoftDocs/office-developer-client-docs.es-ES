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
ms.openlocfilehash: 6370b559c5160bfa48d32afa77715e9a7c126aab
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390467"
---
# <a name="activity-feed-xml-example"></a>Ejemplo de XML de fuentes de actividades

El ejemplo de XML de este tema es una cadena XML devuelta a Outlook Social Connector (OSC) después de que llama al método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) para una red social de fuente de actividades. 
  
En el ejemplo se muestra el XML que contiene las siguientes cuatro actividades **activityFeed** , cada uno de ellos delimitado por el elemento **activityDetails** y que coincidan con una plantilla para mostrar con fines: 
  
- Para actualizar una imagen de perfil, Melissa Macbeth, cuyo **ownerID** en la red social es 4667647. Esta actividad especifica tres variables de plantilla de tipo **publisherVariable**, **listVariable**y **pictureVariable** (que está delimitado por **listVariable**). Estas variables especifican a la persona que publicó la actividad fuente elemento y la información de la imagen que se van a actualizar (mediante el uso de los elementos secundarios de **nombre**, **valor**, **altText**y **href** de **pictureVariable**).
    
- Para actualizar una imagen de perfil, Michael Affronti cuyo **ownerID** en la red social es 5015012. Al igual que la última actividad, esta actividad especifica tres variables de plantilla de tipo **publisherVariable**, **listVariable**y **pictureVariable**. Estas variables especifican a la persona que publicó la actividad fuente de elemento y la información de la imagen que se van a actualizar.
    
- Una actualización de estado por Michael Affronti, que muestra el mismo **ownerID** de 5015012 como la última actividad. Esta actividad especifica dos variables de plantilla de tipo **publisherVariable** y **textVariable**. **publisherVariable** especifica a la persona que publicó el elemento de fuente de actividades y **textVariable** incluye un **valor** de la línea de estado`is hiking on Mount Rainier this weekend!`
    
- Una entrada de blog por Michael Affronti, que muestra el mismo **ownerID** de 5015012 como las actividades de dos por última vez. Esta actividad especifica dos variables de plantilla de tipo **publisherVariable** y **linkVariable**. **publisherVariable** especifica el elemento de fuente de la persona que publicó la actividad y **linkVariable** incluye más información (especificada por los elementos secundarios de **nombre**, el **texto**y el **valor** de **linkVariable**) acerca de la entrada de blog.
    
Cada una de las actividades de cuatro especifica un valor de **identificador de plantilla** , que coincide con una de las tres plantillas especificadas por el elemento de **plantillas** . Cada plantilla está en su propio elemento **activityTemplateContainer** , identificado por un valor de **identificador de plantilla** que también se usa para mostrar una actividad que tiene el mismo valor de **identificador de plantilla** . 
  
Para obtener una descripción detallada de los elementos XML utilizados en el ejemplo, vea los temas siguientes: 
  
- [Elemento de la fuente de información general de XML de una actividad](overview-of-xml-for-an-activity-feed-item.md)
    
- [Elemento activityDetails](activitydetails-element.md)
    
- [Elemento activityTemplateContainer](activitytemplatecontainer-element.md)
    
- [Variables de plantilla](template-variables.md)
    
## <a name="xml-example"></a>Ejemplo de XML

En el ejemplo siguiente se muestra el XML de cuatro actividades **activityFeed** : dos perfiles actualizaciones de imagen, una actualización de estado y una entrada de blog. El código XML también especifica tres plantillas para mostrar de actividad para mostrar las actividades correspondientes. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<activityFeed xmlns="https://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
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

- [Ejemplos XML de proveedor OSC](osc-provider-xml-examples.md)  
- [XML de actividades](xml-for-activities.md) 
- [Ejemplo de XML de capacidades](capabilities-xml-example.md)  
- [Ejemplo de XML de amigos](friends-xml-example.md)
- [Esquema XML de proveedor de Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)

