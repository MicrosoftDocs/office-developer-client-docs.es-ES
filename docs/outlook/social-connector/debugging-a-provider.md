---
title: Depurar un proveedor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Hay varias formas de depurar un proveedor Outlook Social Connector (OSC):'
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281072"
---
# <a name="debugging-a-provider"></a>Depurar un proveedor

Hay varias formas de depurar un proveedor Outlook Social Connector (OSC): 
  
- Mediante el uso de comandos de depuración en el componente de la cinta de opciones de la interfaz de usuario de Office Fluent en Outlook o la aplicación cliente Office compatible para hacer que el OSC lleve Office cabo varias acciones.
    
- Mediante el uso de Fiddler para rastrear llamadas API y XML enviados entre una red social y su proveedor de OSC
    
## <a name="debug-buttons"></a>Botones de depuración

La extensibilidad del proveedor de OSC proporciona la capacidad de depurar un proveedor de OSC. Para depurar un proveedor, cree un valor de tipo DWORD en el registro Windows debajo de la clave (como se muestra en la siguiente línea) y establezca el valor `DebugProviders` `SocialConnector` en `DebugProviders` 1. 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
De forma predeterminada, la depuración del proveedor está desactivada. Si el valor no está presente o está presente y se establece en un valor de 0, la depuración  `DebugProviders` del proveedor se desactivará. 
  
Si la depuración del proveedor está activada, el OSC muestra un cuadro de diálogo de alerta con información de error detallada cuando se produce un error y valida cualquier XML del proveedor de OSC con el esquema XML del proveedor de OSC. En función del espacio de nombres especificado para una cadena XML, un proveedor de OSC desarrollado mediante OSC 1.0 se valida con el archivo de esquema de OSC 1.0, OutlookSocialProvider.xsd. Un proveedor de OSC desarrollado mediante OSC 1.1 o posterior se valida en el archivo de esquema, OutlookSocialProvider_1.1.xsd. Cuando se usa el  `DebugProviders` valor, aparece la alerta de depuración para todos los proveedores cargados en lugar de un proveedor específico. 
  
Para mostrar botones de depuración que pueden ayudarle a depurar un proveedor, cree un valor de tipo DWORD en el registro de Windows debajo de la clave y establezca el valor en `ShowDebugButtons` `SocialConnector` `ShowDebugButtons` 1. Para ocultar los botones de la barra de comandos de depuración, establezca  `ShowDebugButtons` el valor en 0. 
  
Para Outlook 2010 y aplicaciones cliente desde Office 2013, los **botones** de depuración aparecen en la pestaña Complementos de la cinta de opciones del explorador. Para Outlook 2007 y Outlook 2003, los botones de depuración aparecen en la barra de comandos estándar de la ventana Outlook explorador. 
  
En la tabla siguiente se describen los botones de depuración.
  
|**Botón Depurar**|**Función**|
|:-----|:-----|
|Sincronizar contactos  <br/> |Hace que el OSC pida al proveedor de OSC solo contactos almacenados en caché.  <br/> |
|Sincronización gal  <br/> |Hace que el OSC rellene los datos de la Exchange global de direcciones para Outlook contactos.  <br/> |
|Invalidar caché de categorías  <br/> |Hace que el OSC vuelva a cargar la lista de categorías de cada almacén cuando se actualiza la fuente de actividad.  <br/> |
   
## <a name="fiddler"></a>Fiddler

Fiddler es una herramienta de depuración por cable para comprobar las llamadas API enviadas desde el proveedor a la red social y el XML enviado por la red social a su proveedor. Fiddler está disponible para su descarga en [Fiddler Web Debugging Proxy](https://www.fiddler2.com/fiddler2/version.asp).
  
## <a name="see-also"></a>Vea también

- [Pasos rápidos para aprender a desarrollar un proveedor](quick-steps-for-learning-to-develop-a-provider.md)  
- [Sincronizar amigos y actividades](synchronizing-friends-and-activities.md) 
- [Procedimientos recomendados para desarrollar un proveedor](best-practices-for-developing-a-provider.md)
- [Secuencias de llamadas típicas de OSC](osc-typical-calling-sequences.md)  
- [Desarrollo de un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)  
- [Prepararse para liberar un proveedor de OSC](getting-ready-to-release-an-osc-provider.md)

