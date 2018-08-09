---
title: Procedimientos recomendados para el desarrollo de un proveedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: 'Debe cumplir las siguientes prácticas al desarrollar un proveedor de Outlook Social Connector 2013 (OSC):'
ms.openlocfilehash: a6ee9d54f33bbc855d178aba844a8f65ec92f964
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821081"
---
# <a name="best-practices-for-developing-a-provider"></a>Procedimientos recomendados para el desarrollo de un proveedor

Debe cumplir las siguientes prácticas al desarrollar un proveedor de Outlook Social Connector 2013 (OSC):
  
- Por motivos de seguridad, los proveedores que se comunican con servidores a través de Internet deben usar el protocolo HTTPS (transferencia de hipertexto protocolo (HTTP) con la capa de sockets seguros (SSL)). De lo contrario, hay un riesgo de que las direcciones de correo electrónico, las actividades de redes sociales y otro usuario datos podrían ser interceptados o expuestos mientras están en tránsito.
    
- Si está desarrollando un proveedor de OSC para una red social de otro fabricante, su proveedor debe cumplir los términos de la red social de servicio.
    
- Para reducir el tamaño del paquete de descarga del proveedor, crear el proveedor mediante un compilador como C++ o cualquier otra herramienta que puede generar un componente COM nativo.
    
- En su proveedor, cree a un agente de usuario único que se envía a la red social para realizar un seguimiento de las llamadas realizadas por el proveedor para la red social.
    
- El método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) no debe confiar en una llamada a la red social a través de Internet para obtener las capacidades del proveedor. Por ejemplo, los usuarios pueden iniciar Outlook sin conexión; Si el OSC llama a **GetCapabilities** y no hay ninguna conexión de red, la llamada **GetCapabilities** no devolverá válido XML de las **capacidades** . El procedimiento recomendado es almacenar **capacidades** XML como un recurso en su proveedor. 
    
- Su proveedor de OSC puede generar un volumen significativo de las llamadas a una red social. Según los términos del servicio para la red social, considere la posibilidad de almacenamiento en caché de amigos a una carpeta de Outlook para reducir el número de llamadas desde el OSC a su proveedor y, a su vez, desde su proveedor de la red social.
    
- Office 2013 está disponible en versiones de 32 bits y 64 bits. Las versiones de Office anteriores a Office 2010 sólo están disponibles en una versión de 32 bits. La instalación predeterminada de Office 2013 en Windows de 64 bits es de 32 bits. Si piensa admitir la versión de 64 bits de la OSC que se instala con Office 2013 de 64 bits, también debe liberar una versión de 64 bits de su proveedor. 
    
## <a name="see-also"></a>Vea también

- [Secuencias de llamada típicas de OSC](osc-typical-calling-sequences.md)  
- [Desarrollar un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)  
- [Implementación de un proveedor](deploying-a-provider.md)  
- [Introducción al desarrollo de un proveedor de Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

