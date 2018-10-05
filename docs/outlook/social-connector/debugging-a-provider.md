---
title: Depurar un proveedor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Hay varias maneras puede depurar un proveedor de Outlook Social Connector (OSC):'
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386855"
---
# <a name="debugging-a-provider"></a>Depurar un proveedor

Hay varias maneras puede depurar un proveedor de Outlook Social Connector (OSC): 
  
- Mediante el uso de comandos de depuración en el componente de la cinta de opciones de la interfaz de usuario Office Fluent en Outlook o en la aplicación de cliente de Office auxiliar para hacer que el OSC para realizar diversas acciones.
    
- Mediante el uso de Fiddler para las llamadas de API de seguimiento y XML enviados entre una red social y su proveedor de OSC
    
## <a name="debug-buttons"></a>Depurar los botones

La extensibilidad del proveedor OSC proporciona la capacidad de depuración de un proveedor de OSC. Para depurar un proveedor, cree un `DebugProviders` el valor de tipo DWORD en el registro de Windows en el `SocialConnector` clave (como se muestra en la siguiente línea) y establecer el `DebugProviders` valor a 1. 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
De forma predeterminada, el proveedor de depuración está desactivada. Si el `DebugProviders` valor no está presente, o está presente y establecido en un valor de 0, el proveedor de depuración está desactivada. 
  
Si el proveedor de depuración está activado, el OSC muestra un cuadro de diálogo de alerta con información detallada del error cuando se produce un error y valida cualquier proveedor de OSC XML con el esquema XML de proveedor OSC. Según el espacio de nombres especificado para una cadena XML, un proveedor de OSC desarrollado mediante el uso de OSC 1.0 se valida con el archivo de esquema de OSC 1.0, OutlookSocialProvider.xsd. Un proveedor de OSC desarrollado mediante el uso de OSC 1.1 o posterior se valida con el archivo de esquema, OutlookSocialProvider_1.1.xsd. Cuando se utiliza la `DebugProviders` de valor, aparece la alerta de depuración para cargados todos los proveedores en lugar de un proveedor específico. 
  
Para mostrar los botones de depuración que pueden ayudar a depurar un proveedor, cree un `ShowDebugButtons` el valor de tipo DWORD en el registro de Windows en el `SocialConnector` clave y establecer el `ShowDebugButtons` valor a 1. Para ocultar los botones de barra de comandos de depuración, establecer el `ShowDebugButtons` valor en 0. 
  
Para Outlook 2010 y las aplicaciones de cliente con respecto a Office 2013, los botones de depuración aparecen en la ficha **complementos** de la cinta de opciones del explorador. Para Outlook 2007 y Outlook 2003, los botones de depuración aparecen en la barra de comandos estándar de la ventana del explorador de Outlook. 
  
En la siguiente tabla se describe los botones de depuración.
  
|**Botón de depuración**|**Función**|
|:-----|:-----|
|Sincronizar contactos  <br/> |Hace que el OSC para solicitar al proveedor de OSC sólo los contactos almacenados en caché.  <br/> |
|Sincronización de GAL  <br/> |Hace que el OSC rellenar los datos desde la lista Global de direcciones de Exchange para los contactos de Outlook.  <br/> |
|Invalidar la memoria caché de categoría  <br/> |Hace que el OSC volver a cargar la lista de categorías para cada almacén cuando se actualiza la fuente de actividades.  <br/> |
   
## <a name="fiddler"></a>Fiddler

Fiddler es una herramienta de depuración sobre el cable para comprobar el llamadas a la API enviados desde su proveedor a la red social y XML que se envían por la red social a su proveedor. Fiddler está disponible para su descarga en el [Proxy de depuración de Web de Fiddler](https://www.fiddler2.com/fiddler2/version.asp).
  
## <a name="see-also"></a>Vea también

- [Pasos rápidos para aprender a desarrollar un proveedor](quick-steps-for-learning-to-develop-a-provider.md)  
- [Sincronización de amigos y actividades](synchronizing-friends-and-activities.md) 
- [Prácticas recomendadas para desarrollar un proveedor](best-practices-for-developing-a-provider.md)
- [Secuencias de llamada típicas de OSC](osc-typical-calling-sequences.md)  
- [Desarrollar un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)  
- [Prepararse liberar un proveedor de OSC](getting-ready-to-release-an-osc-provider.md)

