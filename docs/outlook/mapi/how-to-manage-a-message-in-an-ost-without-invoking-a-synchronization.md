---
title: Administrar mensajes en OST sin invocar una sincronización en el modo caché de Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: 'Contiene un ejemplo de código en C++ que muestra cómo usar IID_IMessageRaw en IMsgStore:: OpenEntry para obtener una interfaz IMessage que administra un mensaje en un archivo de carpetas sin conexión (OST) sin forzar la descarga de todo el mensaje cuando el cliente está en caché de Exchange Modo.'
ms.openlocfilehash: e50637b496ff43daedad2df27d027d8a6d0dc743
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418760"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a>Administrar mensajes en OST sin invocar una sincronización en el modo caché de Exchange

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Este tema contiene un ejemplo de código en C++ que muestra cómo usar `IID_IMessageRaw` en **[IMsgStore:: OpenEntry](imsgstore-openentry.md)** para obtener una interfaz **[IMessage](imessageimapiprop.md)** que administra un mensaje en un archivo de carpetas sin conexión (OST) sin forzar la descarga de todo el mensaje cuando el cliente está en modo caché de Exchange. 
  
Cuando un cliente está en modo de intercambio en caché, los mensajes del OST pueden estar en uno de estos dos Estados:
  
- Se descarga el mensaje completo que contiene el encabezado y el cuerpo.
    
- Se descarga el mensaje que solo tiene su encabezado.
    
Cuando se solicita una interfaz **IMessage** para un mensaje en un Ost y el cliente está en modo de intercambio en caché, `IID_IMessageRaw`use. Si se usa `IID_IMessage` para solicitar una interfaz **IMessage** y si el mensaje solo tiene su encabezado descargado en Ost, se invoca una sincronización que intenta descargar el mensaje completo. 
  
Si usa `IID_IMessageRaw` o `IID_IMessage` para solicitar una interfaz **IMessage** , las interfaces que se devuelven son idénticas en uso. La interfaz **IMessage** que se solicitó mediante `IID_IMessageRaw` la devolución de un mensaje de correo electrónico como existe en el Ost y la sincronización no se ha forzado. 
  
En el ejemplo siguiente se muestra cómo llamar al método **OpenEntry** , `IID_IMessageRaw` pasando en lugar `IID_IMessage`de.
  
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

Si el método **OpenEntry** devuelve el código de error **MAPI_E_INTERFACE_NOT_SUPPORTED** , indica que el almacén de mensajes no admite el acceso al mensaje en modo sin procesar. En esta situación, pruebe el método **OpenEntry** de nuevo pasando `IID_IMessage`.

> [!IMPORTANT]
>  `IID_IMessageRaw`puede que no esté definida en el archivo de encabezado descargable que tiene actualmente. En este caso, puede agregarlo al código con la siguiente definición. Use la macro DEFINE_OLEGUID definida en el archivo de encabezado guiddef. h del kit de desarrollo de software (SDK) de Microsoft Windows para asociar el nombre simbólico GUID con su valor. >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a>Vea también

- [Acerca de las adiciones de MAPI](about-mapi-additions.md) 
- [Acceder a un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [Abrir un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

