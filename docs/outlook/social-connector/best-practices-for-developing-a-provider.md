---
title: Procedimientos recomendados para el desarrollo de un proveedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: 'Debe seguir los siguientes procedimientos al desarrollar un proveedor de Outlook Social Connector 2013 (OSC):'
ms.openlocfilehash: 6a48a56d8065fb9a176ca6527340c99551cdb52a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425921"
---
# <a name="best-practices-for-developing-a-provider"></a>Procedimientos recomendados para el desarrollo de un proveedor

Debe seguir los siguientes procedimientos al desarrollar un proveedor de Outlook Social Connector 2013 (OSC):
  
- Por motivos de seguridad, los proveedores que se comunican con servidores a través de Internet deben usar el protocolo HTTPS (Protocolo de transferencia de hipertexto (HTTP) con Capa de sockets seguros (SSL).. De lo contrario, existe el riesgo de que las direcciones de correo electrónico, las actividades de redes sociales y otros datos de usuario se puedan interceptar o exponer durante el tránsito.
    
- Si está desarrollando un proveedor de OSC para una red social de terceros, el proveedor debe cumplir los términos de servicio de la red social.
    
- Para minimizar el tamaño del paquete de descarga del proveedor, compila el proveedor mediante un compilador nativo como C++ o cualquier otra herramienta que pueda crear un componente COM.
    
- En su proveedor, cree un agente de usuario único que se envíe a la red social para realizar un seguimiento de las llamadas realizadas por el proveedor a la red social.
    
- El [método ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) no debe confiar en llamar a la red social a través de Internet para obtener las capacidades del proveedor. Por ejemplo, los usuarios pueden iniciar Outlook sin conexión; si el OSC llama **a GetCapabilities** y no hay conexión de red, la llamada **GetCapabilities** no devolverá xml de **funcionalidades válidas.** El procedimiento recomendado es almacenar **xml de funcionalidades** como recurso en el proveedor. 
    
- El proveedor de OSC puede generar un volumen significativo de llamadas a una red social. Según los términos de servicio de la red social, considere la posibilidad de almacenar en caché a amigos en una carpeta de Outlook para reducir el número de llamadas desde el sistema operativo a su proveedor y, a su vez, desde su proveedor a la red social.
    
- Office 2013 está disponible en versiones de 32 y 64 bits. Las versiones de Office anteriores a Office 2010 solo están disponibles en una versión de 32 bits. La instalación predeterminada de Office 2013 en Windows de 64 bits es de 32 bits. Si desea admitir la versión de 64 bits del OSC que se instala con Office 2013 de 64 bits, también debe publicar una versión de 64 bits de su proveedor. 
    
## <a name="see-also"></a>Consulte también

- [Secuencias de llamada típicas de OSC](osc-typical-calling-sequences.md)  
- [Desarrollo de un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)  
- [Implementación de un proveedor](deploying-a-provider.md)  
- [Introducción al desarrollo de un proveedor de Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

