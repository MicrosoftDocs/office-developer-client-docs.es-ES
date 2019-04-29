---
title: Estructura de los proveedores de almacenamiento de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 064b2fc1-e690-43e6-95d3-a61438115de5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: eda62a4cd31e0de695d52391a6717e7a0f5ea581
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426425"
---
# <a name="structure-of-message-store-providers"></a>Estructura de los proveedores de almacenamiento de mensajes
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un proveedor de almacenamiento de mensajes, cuando se está ejecutando en la memoria, es una interfaz [IMSProvider: IUnknown](imsprovideriunknown.md) . La interfaz **IMSProvider** permite a las aplicaciones cliente y a la cola MAPI iniciar y cerrar sesión en el almacén de mensajes. Las interfaces que utilizan las aplicaciones cliente y la cola MAPI para tener acceso a las carpetas y los mensajes del almacén de mensajes son [IMSLogon](imslogoniunknown.md) y [IMsgStore](imsgstoreimapiprop.md) . Estas interfaces se crean normalmente cuando el almacén de mensajes inicia sesión por primera vez en, aunque el punto de entrada [MSProviderInit](msproviderinit.md) de la dll del almacén de mensajes también podría crearlas. 
  
Como las interfaces **IMSLogon** y **IMsgStore** comparten algunos métodos, es posible que sea más fácil crear un objeto de clase que herede de ambas interfaces. También puede implementar estas interfaces en objetos independientes y escribir funciones auxiliares internas a la DLL que implementan los métodos compartidos a los que se puede llamar desde los métodos de las interfaces **IMSLogon** y **IMsgStore** . 
  
En la siguiente ilustración se muestra un esquema de alto nivel de la jerarquía de objetos dentro de un almacén de mensajes en ejecución.
  
**Jerarquía de objetos del almacén de mensajes**
  
![Jerarquía de objetos del almacén de mensajes] (media/storeobj.gif "Jerarquía de objetos del almacén de mensajes")
  
## <a name="see-also"></a>Vea también

- [Desarrollar un proveedor de almacén de mensajes MAPI](developing-a-mapi-message-store-provider.md)

