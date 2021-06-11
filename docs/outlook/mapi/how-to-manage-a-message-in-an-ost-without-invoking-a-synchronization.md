---
title: Administrar mensajes en OST sin invocar una sincronización en modo Exchange caché
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: Contiene un ejemplo de código en C++ que muestra cómo usar IID_IMessageRaw en IMsgStore::OpenEntry para obtener una interfaz IMessage que administra un mensaje en un archivo de carpetas sin conexión (OST) sin forzar una descarga del mensaje completo cuando el cliente está en modo caché Exchange.
ms.openlocfilehash: e50637b496ff43daedad2df27d027d8a6d0dc743
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418760"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a>Administrar mensajes en OST sin invocar una sincronización en modo Exchange caché

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Este tema contiene un ejemplo de código en C++ que muestra cómo usar en `IID_IMessageRaw` **[IMsgStore::OpenEntry](imsgstore-openentry.md)** para obtener una interfaz **[IMessage](imessageimapiprop.md)** que administra un mensaje en un archivo de carpetas sin conexión (OST) sin forzar una descarga del mensaje completo cuando el cliente está en modo caché Exchange. 
  
Cuando un cliente está en modo Exchange caché, los mensajes de ost pueden estar en uno de dos estados:
  
- Se descarga el mensaje completo que contiene el encabezado y el cuerpo.
    
- Se descarga el mensaje con solo su encabezado.
    
Cuando solicite una interfaz **IMessage** para un mensaje en una OST y el cliente esté en modo Exchange caché, use `IID_IMessageRaw` . Si usa para solicitar una interfaz IMessage y si el mensaje solo tiene su encabezado descargado en ost, invocará una sincronización que intente descargar `IID_IMessage` todo el mensaje.  
  
Si usa o  `IID_IMessageRaw`  `IID_IMessage` solicita una interfaz **IMessage,** las interfaces que se devuelven son idénticas en uso. La **interfaz IMessage** que se solicitó mediante el uso devuelve un mensaje de correo electrónico tal como existe en ost y la  `IID_IMessageRaw` sincronización no es forzada. 
  
En el ejemplo siguiente se muestra cómo llamar al **método OpenEntry,** pasando  `IID_IMessageRaw` en lugar de  `IID_IMessage` .
  
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

Si el **método OpenEntry** devuelve el MAPI_E_INTERFACE_NOT_SUPPORTED **de** error, indica que el almacén de mensajes no admite el acceso al mensaje en modo sin procesar. En esta situación, vuelva a intentar **el método OpenEntry** pasando  `IID_IMessage` .

> [!IMPORTANT]
>  `IID_IMessageRaw` es posible que no se defina en el archivo de encabezado descargable que tiene actualmente. En este caso, puede agregarlo al código mediante la siguiente definición. Use la macro DEFINE_OLEGUID definida en el archivo de encabezado guiddef.h del Kit de desarrollo de software (SDK) de Microsoft Windows para asociar el nombre simbólico GUID con su valor. >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a>Vea también

- [Acerca de las adiciones de MAPI](about-mapi-additions.md) 
- [Acceder a un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [Abrir un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

