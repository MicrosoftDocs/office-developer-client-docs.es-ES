---
title: Novedades para programadores de InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- what's new [infopath 2007],developer features [InfoPath 2007],InfoPath 2007, what's new,new features [InfoPath 2007]
localization_priority: Normal
ms.assetid: d0ad3111-bd41-4f35-8a34-62c17f20fc19
description: InfoPath está diseñado para facilitar la creación de aplicaciones enriquecidas basadas en formularios en la plataforma Microsoft SharePoint Server. Microsoft InfoPath 2013, Microsoft SharePoint Server 2013 y InfoPath Forms Services disponen de numerosas funciones para desarrolladores. InfoPath Forms Services, que está disponible en SharePoint Server 2013, le permite implementar una plantilla de formulario de InfoPath en un SharePoint Server, de tal modo que aquellos usuarios que no tengan el cliente enriquecido de InfoPath puedan abrir y rellenar formularios de InfoPath en un explorador web.
ms.openlocfilehash: 5d469dfb99290054008271867f24d947a42efeee
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385154"
---
# <a name="whats-new-for-infopath-developers"></a>Novedades para programadores de InfoPath

InfoPath está diseñado para facilitar la creación de aplicaciones enriquecidas basadas en formularios en la plataforma Microsoft SharePoint Server. Microsoft InfoPath 2013, Microsoft SharePoint Server 2013 y InfoPath Forms Services disponen de numerosas funciones para desarrolladores. InfoPath Forms Services, que está disponible en SharePoint Server 2013, le permite implementar una plantilla de formulario de InfoPath en un SharePoint Server, de tal modo que aquellos usuarios que no tengan el cliente enriquecido de InfoPath puedan abrir y rellenar formularios de InfoPath en un explorador web.
  
Las plantillas de formulario creadas con InfoPath 2013 siguen admitiendo lógica empresarial escrita con relación a las clases y los miembros del espacio de nombres **Microsoft.Office.InfoPath**, que funciona de la misma forma con un formulario abierto en InfoPath Filler que con un formulario abierto en un explorador web. Usando la lógica empresarial escrita en este modelo de objetos administrados y trabajando con las funciones de comprobación de diseño de InfoPath Designer, puede crear una plantilla de formulario sencilla e implementarla en una biblioteca de documentos configurada correctamente en SharePoint Server 2013, que se iniciará en InfoPath Filler y en un explorador web. 
  
## <a name="new-features-and-improvements"></a>Características y mejoras

En las secciones siguientes se describen brevemente las funciones y mejoras de interés para desarrolladores de InfoPath:
  
- Nueva forma de escribir y modificar código
    
- Soluciones de espacio aislado de SharePoint
    
- Publicar formularios con un solo clic
    
- Mejorar los formularios de lista de SharePoint
    
- Hospedar formularios en portales mediante el elemento web Formulario de InfoPath
    
- Formularios web más complejos
    
- Formularios de explorador compatibles con los estándares
    
- Proporcionar seguridad e integridad de la información mejoradas con firmas digitales
    
- Controles
    
## <a name="new-way-to-write-and-edit-code"></a>Nueva forma de escribir y modificar código

El IDE de Microsoft Visual Studio Tools for Applications integrado en InfoPath 2010 se ha eliminado en InfoPath 2013. Para escribir o modificar código en InfoPath 2013, ahora debe disponer de Visual Studio 2012 con el complemento [Microsoft Visual Studio Tools for Applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807) instalado. Aunque la experiencia de programación no ha cambiado en lo esencial, ahora puede aprovechar toda la experiencia de desarrollo de Visual Studio al escribir código administrado para sus formularios de InfoPath. 
  
En las siguientes secciones se describen las funciones integradas originalmente en InfoPath 2010 y SharePoint Server 2010 y que continúan aportando valor a los desarrolladores que usan InfoPath 2013 y SharePoint Server 2013.
  
## <a name="sharepoint-server-sandboxed-solutions"></a>Soluciones de espacio aislado de SharePoint Server

Con InfoPath, implementar formularios con código en SharePoint Server 2013 es más fácil que nunca. En Office InfoPath 2007, era necesario que un administrador de granja de servidores de SharePoint aprobara y cargara todos los formularios con código. La compatibilidad con soluciones de espacio aislado en SharePoint Server 2013 permite ahora a los diseñadores de formularios con permisos de administración de colecciones de sitios publicar la mayoría de los formularios con código, directamente en sus sitios de SharePoint. Un parámetro de cuota de recursos permite limitar el uso excesivo de recursos en el servidor. El administrador de la colección de sitios mantiene el control de la solución y puede tomar decisiones de confianza relacionadas con ella. El administrador de la granja de servidores puede no intervenir. Para más información sobre cómo publicar plantillas de formulario de InfoPath como soluciones de espacio aislado, vea [Publicar formularios con código](publishing-forms-with-code.md).
  
## <a name="publish-forms-with-one-click"></a>Publicar formularios con un solo clic

InfoPath está diseñado para que le resulte más sencillo que nunca publicar actualizaciones en sus formularios. Después de publicar una plantilla de formulario por primera vez, en lugar de tener que pasar por varios cuadros de diálogo, puede llevar a cabo esta tarea con un solo clic en el nuevo botón **Publicación rápida**, que está disponible en la **Barra de herramientas de acceso rápido**, y en la nueva Microsoft Office Backstage, disponible al hacer clic en la pestaña **Archivo**. 
  
## <a name="enhance-sharepoint-list-forms"></a>Mejorar formularios de lista de SharePoint

Con InfoPath, ahora puede ampliar y mejorar los formularios usados para crear, modificar y ver elementos en una lista de SharePoint. Al abrir una lista y hacer clic en la pestaña **Lista** de **Herramientas de listas** y, después, en **Personalizar formulario**, puede generar automáticamente un formulario de InfoPath similar al formulario de lista de SharePoint predeterminado que viene incluido. Después, puede personalizar y mejorar este formulario modificando el diseño, creando vistas adicionales y agregando reglas y validación de datos en InfoPath. Cuando termine de modificar el formulario de lista mejorado, puede publicarlo en SharePoint con la nueva función de publicación con un solo clic de InfoPath.
  
## <a name="host-forms-on-portal-pages-using-the-infopath-form-web-part"></a>Hospedar formularios en portales mediante el elemento web Formulario de InfoPath

En SharePoint Server 2013, resulta más fácil que nunca hospedar los formularios en páginas web con el nuevo **Elemento web Formulario de Infopath**. En Microsoft Office SharePoint Server 2007, los usuarios que deseen hospedar los formularios de InfoPath en páginas web deben escribir el código de Visual Studio. Ahora, sin tener que escribir una sola línea de código, puede agregar el **elemento web Formulario de InfoPath** a una página de elementos web y apuntarla al formulario publicado. Puede usar el **elemento web Formulario de InfoPath** para hospedar cualquier formulario explorador de InfoPath que se publique en una biblioteca de formularios o lista de SharePoint. También puede conectarse a otros elementos web en la página para enviar o recibir datos. Para obtener más información sobre cómo usar el **elemento web Formulario de InfoPath**, vea [Trabajar con el elemento web Formulario de InfoPath](https://msdn.microsoft.com/library/bb87e126-1a07-45aa-af36-b294df3a2576%28Office.15%29.aspx) en el SDK de SharePoint 2010. 
  
## <a name="richer-web-forms"></a>Formularios web más complejos

La diferencia en las características entre formularios de cliente y explorador se ha reducido, generando una experiencia de rellenado de formularios más uniforme para todos los usuarios. Los controles y funcionalidades que se admiten actualmente en los formularios de explorador incluyen:
  
- Listas con viñetas, numeradas y simples
    
- Cuadros de lista de selección múltiple
    
- Cuadros combinados
    
- Botones de imagen
    
- Capacidades de hipervínculo
    
- Sección y grupo de opciones 
    
- Controles de fecha y hora
    
- Selector de personas o grupos
    
- Funcionalidad de filtrado
    
## <a name="standards-compliant-browser-forms"></a>Formularios de explorador compatibles con los estándares

Ahora los formularios de explorador de InfoPath cumplen las Instrucciones de accesibilidad a contenido web 2.0 (WCAG 2.0) AA, lo que permite a los diseñadores crear formularios que puedan estar disponibles para usuarios con discapacidades.
  
## <a name="provide-enhanced-information-security-and-integrity-with-digital-signatures"></a>Proporcionar seguridad e integridad de la información mejoradas con firmas digitales

InfoPath admite contenido firmado digitalmente de Cryptography Next Generation (CNG). Para asegurar la integridad de la información que contienen los formularios, el cliente de InfoPath y SharePoint Server 2013 proporcionan los controles necesarios para habilitar escenarios de firma única, cofirma y contrafirma de todo el formulario o secciones del mismo. Los formularios se pueden firmar en Internet Explorer con el control ActiveX de línea de firma. Los formularios firmados se pueden ver en cualquier explorador compatible con SharePoint Server 2013.
  
## <a name="new-controls"></a>Controles

InfoPath proporciona un conjunto de controles más completo que se puede agregar a sus formularios. En la lista siguiente se describen de manera breve algunos de los nuevos controles disponibles:
  
- **Botón de imagen**: en lugar de un rectángulo gris, use cualquier imagen como botón en el formulario. 
    
- **Hipervínculo**: permita que los usuarios escriban sus propios hipervínculos cuando rellenan formularios. 
    
- **Selector de personas o grupos**: permita que los usuarios comprueben y consulten nombres de cuenta y grupos cuando rellenan formularios. 
    
- **Selector de entidad**: permita que los usuarios seleccionen valores desde listas externas en un servidor que inicia SharePoint Server 2013. 
    
- **Línea de firma**: proporcione a los usuarios una línea de firma o imagen de sello, por ejemplo, un sello inkan o hanko, cuando firmen digitalmente formularios. 
    
## <a name="see-also"></a>Vea también



[Desarrollo de plantillas de formulario de InfoPath con código](developing-infopath-form-templates-with-code.md)
  
[Programar plantillas de formulario con código mediante el modelo de objetos de InfoPath 2003](developing-form-templates-using-the-infopath-2003-object-model.md)

