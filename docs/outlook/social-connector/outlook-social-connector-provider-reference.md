---
title: Referencia de proveedores de Outlook Social Connector
manager: soliver
ms.date: 04/04/2016
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13661393-adf6-4870-86c4-303262317675
description: El Outlook Social Connector 2013 proporciona un centro de comunicación para comunicaciones personales y profesionales.
ms.openlocfilehash: e570fe69cbbe0e8d472e712fb3b8592c97fe43c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359839"
---
# <a name="outlook-social-connector-provider-reference"></a>Referencia de proveedores de Outlook Social Connector

El Outlook Social Connector 2013 proporciona un centro de comunicación para comunicaciones personales y profesionales. El Outlook Social Connector (OSC) funciona con SharePoint Server, SharePoint Workspace, lync client y todas las aplicaciones cliente de Office que admiten información de presencia y la tarjeta de contacto admite el OSC. 

En Outlook en particular, simplemente seleccionando un elemento de Outlook como un correo electrónico o una solicitud de reunión y haciendo clic en el remitente o un destinatario en ese elemento, sin salir de Outlook, los usuarios pueden ver en el Panel de personas actividades, fotos y actualizaciones de estado de esta persona en sus redes sociales favoritas. Los usuarios pueden ver cómodamente todos los Outlook correo electrónico, datos adjuntos y reuniones recibidas de esta persona. En un entorno organizativo, los usuarios de un sitio SharePoint también pueden ver en el panel de personas actualizaciones de documentos y otras actividades del sitio de esta persona en el SharePoint sitio.
  
Una red social puede desarrollar un proveedor para que el OSC sincronice y acote las actualizaciones de redes sociales en servidores y aplicaciones de soporte técnico. Las redes sociales populares como LinkedIn, Facebook y Windows Live ofrecen proveedores para el OSC. 
  
La Outlook de proveedor de Social Connector 2013 describe cómo desarrollar un proveedor de OSC mediante la extensibilidad del proveedor de OSC. 
  
Si no tiene experiencia en el desarrollo de soluciones para Outlook, consulte [Seleccionar una API o tecnología para desarrollar soluciones de Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) para identificar las API y tecnologías más adecuadas para sus necesidades. 
  
## <a name="in-this-section"></a>En esta sección

- Introducción al desarrollo de un proveedor de conectores sociales de [Outlook:](getting-started-with-developing-an-outlook-social-connector-provider.md)proporciona una introducción al OSC, que incluye lo siguiente: cómo un proveedor de OSC puede ser útil, pasos rápidos para aprender a desarrollar un proveedor, requisitos técnicos, procedimientos recomendados para desarrollar un proveedor y las novedades de esta versión.
    
- [Plantillas de ejemplo de OSC:](osc-sample-templates.md)describe varias Visual Studio plantillas para desarrollar un proveedor.
    
- Secuencias de llamadas típicas de [OSC:](osc-typical-calling-sequences.md)describe algunas secuencias de llamadas típicas del OSC de los miembros de las interfaces de extensibilidad del proveedor de OSC. Esto debería permitirle comprender mejor cómo implementar estas interfaces.
    
- Desarrollo de un proveedor con el esquema XML de [OSC:](developing-a-provider-with-the-osc-xml-schema.md)describe cómo las interfaces de extensibilidad del proveedor de OSC y el esquema XML de OSC están diseñados para admitir un proveedor de OSC.
    
- [Depurar un proveedor:](debugging-a-provider.md)sugiere algunas formas de ayudar a depurar un proveedor de OSC.
    
- [Implementación de un proveedor:](deploying-a-provider.md)describe los requisitos de registro para un proveedor de OSC y proporciona una lista de comprobación para instalar un proveedor.
    
- [Prepararse para liberar un proveedor de OSC:](getting-ready-to-release-an-osc-provider.md)sugiere pruebas que puede hacer antes de liberar un proveedor de OSC.
    
- Outlook de proveedor [de Social Connector:](outlook-social-connector-provider-reference-0.md)proporciona información de referencia para las interfaces de extensibilidad del proveedor OSC y el esquema XML de OSC, y enumera los posibles códigos de error.
    
## <a name="see-also"></a>Vea también

- [Outlook Aviso de copyright de referencia de proveedor de Social Connector 2013](outlook-social-connector-2013-provider-reference-copyright-notice.md) 
- [Convenciones del documento](https://msdn.microsoft.com/office/aa905365.aspx)   
- [Accesibilidad en los productos de Microsoft](https://www.microsoft.com/enable/products/default.aspx)  
- [Declaración de privacidad de Microsoft](https://privacy.microsoft.com/en-us/privacystatement)
    

