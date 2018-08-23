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
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a><span data-ttu-id="9c4b9-103">Administrar mensajes en OST sin invocar una sincronización en el modo de intercambio en caché</span><span class="sxs-lookup"><span data-stu-id="9c4b9-103">Manage messages in OST without invoking a synchronization in Cached Exchange mode</span></span>

<span data-ttu-id="9c4b9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c4b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c4b9-105">Este tema contiene un ejemplo de código en C++ que se muestra cómo usar `IID_IMessageRaw` en **[IMsgStore::OpenEntry](imsgstore-openentry.md)** para obtener **[una interfaz que administra un mensaje en un archivo de carpetas sin conexión (OST)](imessageimapiprop.md)** sin necesidad de una descarga de todo el mensaje cuando el cliente se encuentra en el modo de intercambio en caché.</span><span class="sxs-lookup"><span data-stu-id="9c4b9-105">This topic contains a code sample in C++ that shows how to use `IID_IMessageRaw` in **[IMsgStore::OpenEntry](imsgstore-openentry.md)** to obtain an **[IMessage](imessageimapiprop.md)** interface that manages a message in an offline folders file (OST) without forcing a download of the whole message when the client is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="9c4b9-106">Cuando un cliente está en modo caché de Exchange, los mensajes en el archivo OST pueden estar en uno de los dos estados:</span><span class="sxs-lookup"><span data-stu-id="9c4b9-106">When a client is in Cached Exchange Mode, messages in the OST can be in one of two states:</span></span>
  
- <span data-ttu-id="9c4b9-107">Se descarga el mensaje entero que contiene el encabezado y el cuerpo.</span><span class="sxs-lookup"><span data-stu-id="9c4b9-107">The whole message that contains the header and the body is downloaded.</span></span>
    
- <span data-ttu-id="9c4b9-108">Se descarga el mensaje con sólo su encabezado.</span><span class="sxs-lookup"><span data-stu-id="9c4b9-108">The message with only its header is downloaded.</span></span>
    
<span data-ttu-id="9c4b9-109">Cuando se solicita **una interfaz para un mensaje en un OST** y el cliente está en modo caché de Exchange, utilice `IID_IMessageRaw`.</span><span class="sxs-lookup"><span data-stu-id="9c4b9-109">When you request an **IMessage** interface for a message in an OST and the client is in Cached Exchange Mode, use  `IID_IMessageRaw`.</span></span> <span data-ttu-id="9c4b9-110">Si usa `IID_IMessage` para solicitar **una interfaz,** y si el mensaje tiene solo su encabezado descargado en el archivo OST, invocar una sincronización que intenta descargar todo el mensaje.</span><span class="sxs-lookup"><span data-stu-id="9c4b9-110">If you use  `IID_IMessage` to request an **IMessage** interface, and if the message has only its header downloaded in the OST, you invoke a synchronization that attempts to download the whole message.</span></span> 
  
<span data-ttu-id="9c4b9-111">Si usa `IID_IMessageRaw` o `IID_IMessage` para solicitar **una interfaz** , las interfaces que se devuelven son idénticas en uso.</span><span class="sxs-lookup"><span data-stu-id="9c4b9-111">If you use  `IID_IMessageRaw` or  `IID_IMessage` to request an **IMessage** interface, the interfaces that are returned are identical in use.</span></span> <span data-ttu-id="9c4b9-112">**La interfaz que se solicitó mediante el uso de** `IID_IMessageRaw` devuelve un mensaje de correo electrónico tal y como existe en el archivo OST, y no se fuerza la sincronización.</span><span class="sxs-lookup"><span data-stu-id="9c4b9-112">The **IMessage** interface that was requested by using  `IID_IMessageRaw` returns an email message as it exists in the OST, and synchronization is not forced.</span></span> 
  
<span data-ttu-id="9c4b9-113">En el ejemplo siguiente se muestra cómo llamar al método **OpenEntry** , pasando `IID_IMessageRaw` en lugar de `IID_IMessage`.</span><span class="sxs-lookup"><span data-stu-id="9c4b9-113">The following example shows how to call the **OpenEntry** method, passing  `IID_IMessageRaw` instead of  `IID_IMessage`.</span></span>
  
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

<span data-ttu-id="9c4b9-114">Si el método **OpenEntry** devuelve el código de error **MAPI_E_INTERFACE_NOT_SUPPORTED** , indica que el almacén de mensajes no es compatible con el acceso a los mensajes en modo sin procesar.</span><span class="sxs-lookup"><span data-stu-id="9c4b9-114">If the **OpenEntry** method returns the **MAPI_E_INTERFACE_NOT_SUPPORTED** error code, it indicates that the message store does not support accessing the message in raw mode.</span></span> <span data-ttu-id="9c4b9-115">En esta situación, el método **OpenEntry** vuelva a intentarlo pasando `IID_IMessage`.</span><span class="sxs-lookup"><span data-stu-id="9c4b9-115">In this situation, try the **OpenEntry** method again by passing  `IID_IMessage`.</span></span>

> [!IMPORTANT]
>  <span data-ttu-id="9c4b9-116">`IID_IMessageRaw`no es posible que se define en el archivo de encabezado descargables que tiene actualmente.</span><span class="sxs-lookup"><span data-stu-id="9c4b9-116">`IID_IMessageRaw` might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="9c4b9-117">En este caso, puede agregarlo a su código mediante el uso de la siguiente definición.</span><span class="sxs-lookup"><span data-stu-id="9c4b9-117">In this case, you can add it to your code by using the following definition.</span></span> <span data-ttu-id="9c4b9-118">Utilice la macro DEFINE_OLEGUID definida en el guiddef.h de archivo de encabezado de Kit de desarrollo de Software (SDK) de Microsoft Windows para asociar el nombre simbólico GUID su valor.</span><span class="sxs-lookup"><span data-stu-id="9c4b9-118">Use the DEFINE_OLEGUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the GUID symbolic name with its value.</span></span> >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a><span data-ttu-id="9c4b9-119">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="9c4b9-119">See also</span></span>

- [<span data-ttu-id="9c4b9-120">Información sobre las adiciones de MAPI</span><span class="sxs-lookup"><span data-stu-id="9c4b9-120">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="9c4b9-121">Acceder a un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange</span><span class="sxs-lookup"><span data-stu-id="9c4b9-121">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="9c4b9-122">Abrir un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange</span><span class="sxs-lookup"><span data-stu-id="9c4b9-122">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

