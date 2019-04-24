---
title: Depurar un proveedor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Hay varias formas en las que puede depurar un proveedor de Outlook Social Connector (OSC):'
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281072"
---
# <a name="debugging-a-provider"></a>Depurar un proveedor

Hay varias formas en las que puede depurar un proveedor de Outlook Social Connector (OSC): 
  
- Mediante comandos de depuración en el componente de la cinta de la interfaz de usuario de Office Fluent en Outlook o la aplicación cliente de Office auxiliar para hacer que el OSC lleve a cabo diversas acciones.
    
- Mediante el uso de Fiddler para realizar un seguimiento de las llamadas a la API y el XML enviado entre una red social y su proveedor de OSC
    
## <a name="debug-buttons"></a>Botones de dePuración

La extensibilidad del proveedor de OSC proporciona la capacidad de depurar un proveedor de OSC. Para depurar un proveedor, `DebugProviders` cree un valor de tipo DWORD en el registro de `SocialConnector` Windows en la clave (como se muestra en la siguiente línea) `DebugProviders` y establezca el valor en 1. 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
De forma predeterminada, la depuración del proveedor está desactivada. Si el `DebugProviders` valor no está presente, o está presente y se establece en un valor de 0, la depuración del proveedor se desactiva. 
  
Si está activada la depuración del proveedor, OSC muestra un cuadro de diálogo de alerta con información de error detallada cuando se produce un error y valida cualquier XML del proveedor OSC con el esquema XML del proveedor de OSC. Basándose en el espacio de nombres especificado para una cadena XML, un proveedor OSC desarrollado con OSC 1,0 se valida con el archivo de esquema OSC 1,0, OutlookSocialProvider. xsd. Un proveedor OSC desarrollado con OSC 1,1 o posterior se valida con el archivo de esquema, OutlookSocialProvider_ 1.1. xsd. Cuando se usa el `DebugProviders` valor, la alerta de depuración aparece para todos los proveedores cargados en lugar de un proveedor específico. 
  
Para mostrar los botones de depuración que pueden ayudarle a depurar un proveedor, cree un `ShowDebugButtons` valor de tipo `SocialConnector` DWORD en el registro de `ShowDebugButtons` Windows bajo la clave y establezca el valor en 1. Para ocultar los botones de la barra de comandos de `ShowDebugButtons` depuración, establezca el valor en 0. 
  
Para Outlook 2010 y aplicaciones cliente desde Office 2013, los botones de depuración **** aparecen en la ficha complementos de la cinta de la Explorer. Para Outlook 2007 y Outlook 2003, los botones de depuración aparecen en la barra de comandos estándar de la ventana del explorador de Outlook. 
  
En la tabla siguiente se describen los botones de depuración.
  
|**Botón dePurar**|**Función**|
|:-----|:-----|
|Sincronizar contactos  <br/> |Hace que el OSC pregunte sólo a los contactos almacenados en caché al proveedor de OSC.  <br/> |
|Sincronización de GAL  <br/> |Hace que OSC rellene los datos de la lista global de direcciones de Exchange a los contactos de Outlook.  <br/> |
|Caché de la categoría invalidar  <br/> |Hace que OSC vuelva a cargar la lista de categorías de cada almacén cuando se actualiza la fuente de actividades.  <br/> |
   
## <a name="fiddler"></a>Fiddler

Fiddler es una herramienta de depuración en el cable para comprobar las llamadas a la API enviadas desde el proveedor a la red social y el XML enviado por la red social a su proveedor. Fiddler está disponible para su descarga en el proxy de dePuración [Web de Fiddler](https://www.fiddler2.com/fiddler2/version.asp).
  
## <a name="see-also"></a>Vea también

- [Pasos rápidos para aprender a desarrollar un proveedor](quick-steps-for-learning-to-develop-a-provider.md)  
- [Sincronización de amigos y actividades](synchronizing-friends-and-activities.md) 
- [Procedimientos recomendados para desarrollar un proveedor](best-practices-for-developing-a-provider.md)
- [Secuencias de llamada típicas de OSC](osc-typical-calling-sequences.md)  
- [Desarrollo de un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)  
- [Preparación para la publicación de un proveedor OSC](getting-ready-to-release-an-osc-provider.md)

