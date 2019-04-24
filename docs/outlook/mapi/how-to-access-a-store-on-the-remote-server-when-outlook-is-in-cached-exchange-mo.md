---
title: Obtener acceso a un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: 'Última modificación: 2012 de julio de 2002'
ms.openlocfilehash: cfc20c1a9ca4510ffec86bf16666f1fc50822321
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299443"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Obtener acceso a un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Este tema contiene un ejemplo de código en C++ que muestra cómo usar la marca **MAPI_NO_CACHE** para abrir una carpeta o un mensaje en un almacén de mensajes en el servidor remoto cuando Microsoft Office Outlook está en modo caché de Exchange. 
  
El modo caché de Exchange permite a Outlook usar una copia local del buzón de un usuario mientras Outlook mantiene una conexión en línea a una copia remota del buzón del usuario en el servidor remoto de Exchange. Cuando Outlook se ejecuta en modo caché de Exchange, de forma predeterminada, todas las soluciones MAPI que inicien sesión en la misma sesión también se conectan al almacén de mensajes en caché. Los datos a los que se obtiene acceso y los cambios realizados se realizan en la copia local del buzón.
  
Un cliente o un proveedor de servicios puede invalidar la conexión al almacén de mensajes local y abrir un mensaje o una carpeta en el almacén remoto estableciendo el bit de **MAPI_NO_CACHE** en el parámetro *ulFlags* al llamar a **[IMsgStore:: OpenEntry](imsgstore-openentry.md)**. 
  
El siguiente ejemplo de código muestra cómo llamar a **IMsgStore:: OpenEntry** con la marca **MAPI_NO_CACHE** establecida en el parámetro *ulFlags* para abrir la carpeta raíz en el almacén de mensajes remotos. 
  
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

Si ha abierto el almacén de mensajes con la marca **MDB_ONLINE** en el servidor remoto, no es necesario que use la marca **MAPI_NO_CACHE** . 
  
## <a name="see-also"></a>Vea también

- [Acerca de las adiciones de MAPI](about-mapi-additions.md) 
- [Abrir un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Administrar un mensaje en un OST sin invocar una sincronización en el modo de intercambio en caché](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

