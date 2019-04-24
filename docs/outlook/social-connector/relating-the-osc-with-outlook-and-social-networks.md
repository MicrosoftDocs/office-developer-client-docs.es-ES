---
title: Información relativa a la OSC con Outlook y las redes sociales
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: Outlook Social Connector (OSC) puede mostrar en la tarjeta de contacto de Office y en las actividades, el estado o las actualizaciones de las fotos del panel de personas de Outlook para un compañero de trabajo, amigo o cualquier persona con la que esté asociado.
ms.openlocfilehash: 0ee9451e64f12e8ba371c1ba91a1379cff257313
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329263"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a>Información relativa a la OSC con Outlook y las redes sociales

Outlook Social Connector (OSC) puede mostrar en la tarjeta de contacto de Office y en las actividades, el estado o las actualizaciones de las fotos del panel de personas de Outlook para un compañero de trabajo, amigo o cualquier persona con la que esté asociado. De forma predeterminada, el OSC muestra los correos electrónicos de Outlook, los datos adjuntos y las convocatorias de reunión recibidas de una persona seleccionada. Si la persona seleccionada y el usuario de Office colaboran en un sitio de SharePoint, el OSC también muestra actualizaciones de documentos y otras actividades de sitio de ese sitio de SharePoint. Según los contextos de asociación en los que esté interesado el usuario de Office, el usuario de Office puede instalar los proveedores de OSC para las aplicaciones de línea de negocio, los sitios web corporativos internos o una variedad de sitios de red profesionales y sociales, como LinkedIn, Facebook y Windows Live.
  
Para permitir el uso compartido de la funcionalidad en las aplicaciones cliente de Office, el motor del núcleo OSC se implementa como parte de un componente compartido de Office y el panel de personas se implementa como un complemento de Outlook. Para usar el OSC, un usuario de Office debe tener instalado Outlook en ese equipo cliente y haber configurado Outlook con un perfil, de modo que el OSC pueda almacenar en caché los contactos de una carpeta de contactos. 
  
Un proveedor OSC es un archivo DLL del modelo de objetos componentes (COM) que permite al OSC tener acceso a los datos de la red social de manera independiente de las API de cada red social. Una DLL de proveedor de OSC debe instalarse localmente en un equipo cliente. El proveedor OSC de una red social conecta el OSC, que forma parte de Outlook, con la red social en Internet.
  
Un proveedor OSC debe implementar un conjunto de interfaces, definidas como parte de la extensibilidad del proveedor OSC, para comunicarse con el OSC. La extensibilidad de proveedores de OSC está disponible como una plataforma abierta.
  
La arquitectura de proveedor del OSC permite que varios proveedores trabajen con el motor del núcleo OSC y agreguen información social como amigos y actividades. La figura 1 ilustra la arquitectura del proveedor de OSC.
  
**Figura 1. Arquitectura de proveedor de Outlook Social Connector**

![Redes sociales, proveedores de OSC, OSC y Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a>Terminología

En esta referencia de proveedor de Outlook Social Connector, una red social se usa para hacer referencia a los siguientes tipos de sitios: 
  
- Sitios de colaboración, como SharePoint.
    
- Sitios de redes sociales, como Facebook y Windows Live.
    
- Sitios de red profesionales como LinkedIn.
    
- Otras aplicaciones de línea de negocio o sitios Web internos corporativos usados para la red.
    
El término amigo suele usarse para incluir amigos, familia, compañeros, conexiones y cualquier otra persona a la que se asocie un usuario de Office en un contexto de colaboración, como SharePoint, o que se haya agregado a la cuenta de red social del usuario. Los usuarios que no son amigos son a los que se hace referencia en las actualizaciones de actividad de los amigos, pero no son amigos que se han agregado a la cuenta de red social del usuario de Office. Los contactos son personas en una carpeta de contactos de Outlook. 
  
## <a name="see-also"></a>Vea también

- [Introducción al desarrollo de un proveedor de Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

