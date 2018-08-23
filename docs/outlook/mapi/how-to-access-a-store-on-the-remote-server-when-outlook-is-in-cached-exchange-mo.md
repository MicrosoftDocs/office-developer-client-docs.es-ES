---
title: Tener acceso a un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: 'Última modificación: 02 de julio de 2012'
ms.openlocfilehash: c7994366000e323cc7d14a9c3a02b5229c5f08e7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573316"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Tener acceso a un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Este tema contiene un ejemplo de código en C++ que se muestra cómo usar el indicador **MAPI_NO_CACHE** para abrir una carpeta o un mensaje en un almacén de mensajes en el servidor remoto cuando Microsoft Office Outlook está en modo caché de Exchange. 
  
El modo de intercambio en caché permite que Outlook para utilizar una copia local del buzón de un usuario mientras Outlook mantiene una conexión en línea a una copia remota de buzón de correo del usuario en el servidor de Exchange remoto. Cuando Outlook se ejecuta en modo caché de Exchange, de forma predeterminada, las soluciones MAPI que inicie sesión en la misma sesión también están conectadas en el almacén de mensajes almacenados en caché. Los datos que se tiene acceso y los cambios que se realizan se realizan con la copia local del buzón.
  
Un proveedor de servicio o cliente puede invalidar la conexión con el almacén de mensajes local y abrir un mensaje o una carpeta en el almacén remoto estableciendo el bit de **MAPI_NO_CACHE** en el parámetro *ulFlags* al llamar a **[IMsgStore::OpenEntry](imsgstore-openentry.md)**. 
  
El ejemplo de código siguiente muestra cómo llamar a **IMsgStore::OpenEntry** con el indicador **MAPI_NO_CACHE** establecido en el parámetro *ulFlags* para abrir la carpeta raíz en el almacén de mensajes remoto. 
  
```cpp
HRESULT HrOpenRootFolder ( 
    LPMDB lpMDB, 
    LPMESSAGE* lpRootFolder) 
{ 
    ULONG ulObjType = NULL; 
    HRESULT hRes = lpMDB-&gt;OpenEntry( 
        0,// size of entry ID       
        NULL,                                   // Pointer to entry ID 
        NULL,                                   // Use default interface (IMAPIFolder) 
        MAPI_BEST_ACCESS | MAPI_NO_CACHE,       // Flags 
        &amp;ulObjType,
// Output parameter indicates the type of object returned 
        (LPUNKNOWN *) lpRootFolder));           // Pointer to put the opened folder in 
    return hRes; 
 
}
```

Si se abre el almacén de mensajes con el indicador **MDB_ONLINE** en el servidor remoto, no es necesario usar el indicador **MAPI_NO_CACHE** . 
  
## <a name="see-also"></a>Recursos adicionales

- [Información sobre las adiciones de MAPI](about-mapi-additions.md) 
- [Abrir un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Administrar un mensaje en un OST sin invocar una sincronización en el modo de intercambio en caché](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

