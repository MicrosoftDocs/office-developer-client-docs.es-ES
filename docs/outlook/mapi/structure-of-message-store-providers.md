---
title: Estructura de los proveedores de almacén de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 064b2fc1-e690-43e6-95d3-a61438115de5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2f78428b8067b7937e9bd2ee36934cc29a16bfb7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820801"
---
# <a name="structure-of-message-store-providers"></a>Estructura de los proveedores de almacén de mensajes
  
**Hace referencia a**: Outlook 
  
Un proveedor de almacén de mensajes, cuando se está ejecutando en la memoria, es un [IMSProvider: IUnknown](imsprovideriunknown.md) interfaz. La interfaz de **IMSProvider** permite a cliente de aplicaciones y la cola de MAPI iniciar sesión y cerrar el almacén de mensajes. Las interfaces que usan las aplicaciones cliente y la cola de MAPI para tener acceso a carpetas y mensajes en el almacén de mensajes son interfaces [IMSLogon](imslogoniunknown.md) y [IMsgStore](imsgstoreimapiprop.md) . Estas interfaces normalmente se crean cuando el almacén de mensajes en primer lugar se ha iniciado sesión en, aunque el punto de entrada [MSProviderInit](msproviderinit.md) del mensaje almacenar DLL también podría crear ellos. 
  
Debido a que las interfaces **IMSLogon** y **IMsgStore** compartan algunos métodos, puede ser más fácil crear un objeto de clase que hereda de ambas interfaces. También puede implementar estas interfaces en objetos independientes y escribir las funciones auxiliares internas del archivo DLL que implementan los métodos compartidos que, a continuación, se pueden llamar desde los métodos en las interfaces **IMSLogon** y **IMsgStore** . 
  
En la siguiente ilustración se muestra un esquema de alto nivel de la jerarquía de objetos dentro de un almacén de mensajes que se está ejecutando.
  
**Jerarquía de objetos del almacén de mensajes**
  
![Jerarquía de objetos del almacén de mensajes] (media/storeobj.gif "Jerarquía de objetos del almacén de mensajes")
  
## <a name="see-also"></a>Vea también

- [Desarrollar un proveedor de almac�n de mensajes de MAPI](developing-a-mapi-message-store-provider.md)

