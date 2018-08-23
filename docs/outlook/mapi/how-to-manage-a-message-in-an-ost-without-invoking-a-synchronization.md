---
title: Administrar mensajes en OST sin invocar una sincronización en el modo de intercambio en caché
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: Contiene un ejemplo de código en C++ que se muestra cómo usar IID_IMessageRaw en IMsgStore::OpenEntry para obtener una interfaz que administra un mensaje en un archivo de carpetas sin conexión (OST) sin necesidad de una descarga de todo el mensaje cuando el cliente está en la caché de Exchange Modo.
ms.openlocfilehash: f094f5a7deae705ed64b912483726aeb409fb107
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568108"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a>Administrar mensajes en OST sin invocar una sincronización en el modo de intercambio en caché

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Este tema contiene un ejemplo de código en C++ que se muestra cómo usar `IID_IMessageRaw` en **[IMsgStore::OpenEntry](imsgstore-openentry.md)** para obtener **[una interfaz que administra un mensaje en un archivo de carpetas sin conexión (OST)](imessageimapiprop.md)** sin necesidad de una descarga de todo el mensaje cuando el cliente se encuentra en el modo de intercambio en caché. 
  
Cuando un cliente está en modo caché de Exchange, los mensajes en el archivo OST pueden estar en uno de los dos estados:
  
- Se descarga el mensaje entero que contiene el encabezado y el cuerpo.
    
- Se descarga el mensaje con sólo su encabezado.
    
Cuando se solicita **una interfaz para un mensaje en un OST** y el cliente está en modo caché de Exchange, utilice `IID_IMessageRaw`. Si usa `IID_IMessage` para solicitar **una interfaz,** y si el mensaje tiene solo su encabezado descargado en el archivo OST, invocar una sincronización que intenta descargar todo el mensaje. 
  
Si usa `IID_IMessageRaw` o `IID_IMessage` para solicitar **una interfaz** , las interfaces que se devuelven son idénticas en uso. **La interfaz que se solicitó mediante el uso de** `IID_IMessageRaw` devuelve un mensaje de correo electrónico tal y como existe en el archivo OST, y no se fuerza la sincronización. 
  
En el ejemplo siguiente se muestra cómo llamar al método **OpenEntry** , pasando `IID_IMessageRaw` en lugar de `IID_IMessage`.
  
```cpp
HRESULT HrOpenRawMessage ( 
    LPMDB lpMSB,  
    ULONG cbEntryID,  
    LPENTRYID lpEntryID,  
    ULONG ulFlags,  
    LPMESSAGE* lpMessage) 
{ 
    ULONG ulObjType = NULL; 
 
    HRESULT hRes = lpMDB->OpenEntry( 
        cbEntryID, 
        lpEntryID, 
        IID_IMessageRaw, 
        ulFlags, 
        &ulObjType, 
        (LPUNKNOWN*) lpMessage)); 
 
   return hRes; 
} 

```

Si el método **OpenEntry** devuelve el código de error **MAPI_E_INTERFACE_NOT_SUPPORTED** , indica que el almacén de mensajes no es compatible con el acceso a los mensajes en modo sin procesar. En esta situación, el método **OpenEntry** vuelva a intentarlo pasando `IID_IMessage`.

> [!IMPORTANT]
>  `IID_IMessageRaw`no es posible que se define en el archivo de encabezado descargables que tiene actualmente. En este caso, puede agregarlo a su código mediante el uso de la siguiente definición. Utilice la macro DEFINE_OLEGUID definida en el guiddef.h de archivo de encabezado de Kit de desarrollo de Software (SDK) de Microsoft Windows para asociar el nombre simbólico GUID su valor. >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a>Recursos adicionales

- [Información sobre las adiciones de MAPI](about-mapi-additions.md) 
- [Acceder a un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [Abrir un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

