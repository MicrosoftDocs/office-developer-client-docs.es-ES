---
title: Procedimientos recomendados para el desarrollo de un proveedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: 'Debe cumplir los siguientes procedimientos al desarrollar un proveedor Outlook Social Connector 2013 (OSC):'
ms.openlocfilehash: 6a48a56d8065fb9a176ca6527340c99551cdb52a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425921"
---
# <a name="best-practices-for-developing-a-provider"></a>Procedimientos recomendados para el desarrollo de un proveedor

Debe cumplir los siguientes procedimientos al desarrollar un proveedor Outlook Social Connector 2013 (OSC):
  
- Por motivos de seguridad, los proveedores que se comunican con servidores a través de Internet deben usar el protocolo HTTPS (Protocolo de transferencia de hipertexto (HTTP) con capa de socket seguro (SSL).. De lo contrario, existe el riesgo de que las direcciones de correo electrónico, las actividades de la red social y otros datos de usuario se puedan interceptar o exponer durante el tránsito.
    
- Si está desarrollando un proveedor de OSC para una red social de terceros, su proveedor debe cumplir los términos de servicio de la red social.
    
- Para minimizar el tamaño del paquete de descarga del proveedor, cree el proveedor mediante un compilador nativo como C++ o cualquier otra herramienta que pueda crear un componente COM.
    
- En el proveedor, cree un agente de usuario único que se envíe a la red social para realizar un seguimiento de las llamadas realizadas por el proveedor a la red social.
    
- El [método ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) no debe basarse en llamar a la red social a través de Internet para obtener las capacidades del proveedor. Por ejemplo, los usuarios pueden iniciar Outlook sin conexión; si el OSC llama **a GetCapabilities** y no hay conexión de red, la llamada **GetCapabilities** no devolverá XML de **capacidades válidas.** El procedimiento recomendado es almacenar xml **de capacidades** como recurso en el proveedor. 
    
- El proveedor de OSC puede generar un volumen significativo de llamadas a una red social. En función de los términos de servicio de la red social, considere la posibilidad de almacenar en caché amigos en una carpeta Outlook para reducir el número de llamadas del OSC a su proveedor y, a su vez, de su proveedor a la red social.
    
- Office 2013 está disponible en versiones de 32 y 64 bits. Las versiones Office anteriores a Office 2010 solo están disponibles en una versión de 32 bits. La instalación predeterminada de Office 2013 en un Windows de 64 bits es de 32 bits. Si tiene la intención de admitir la versión de 64 bits del OSC que se instala con Office 64 bits de 2013, también debe liberar una versión de 64 bits del proveedor. 
    
## <a name="see-also"></a>Vea también

- [Secuencias de llamadas típicas de OSC](osc-typical-calling-sequences.md)  
- [Desarrollo de un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)  
- [Implementación de un proveedor](deploying-a-provider.md)  
- [Introducción al desarrollo de un Outlook social connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

