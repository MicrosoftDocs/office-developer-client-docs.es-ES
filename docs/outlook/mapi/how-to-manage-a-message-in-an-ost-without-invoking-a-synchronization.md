---
title: Administrar mensajes en OST sin invocar una sincronización en modo caché de Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: Contiene un ejemplo de código en C++ que muestra cómo usar IID_IMessageRaw en IMsgStore::OpenEntry para obtener una interfaz IMessage que administra un mensaje en un archivo de carpetas sin conexión (OST) sin forzar una descarga de todo el mensaje cuando el cliente está en modo caché de Exchange.
ms.openlocfilehash: e50637b496ff43daedad2df27d027d8a6d0dc743
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418760"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a><span data-ttu-id="2fd94-103">Administrar mensajes en OST sin invocar una sincronización en modo caché de Exchange</span><span class="sxs-lookup"><span data-stu-id="2fd94-103">Manage messages in OST without invoking a synchronization in Cached Exchange mode</span></span>

<span data-ttu-id="2fd94-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2fd94-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2fd94-105">Este tema contiene un ejemplo de código en C++ que muestra cómo usar en `IID_IMessageRaw` **[IMsgStore::OpenEntry](imsgstore-openentry.md)** para obtener una interfaz **[IMessage](imessageimapiprop.md)** que administra un mensaje en un archivo de carpetas sin conexión (OST) sin forzar una descarga de todo el mensaje cuando el cliente está en modo caché de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2fd94-105">This topic contains a code sample in C++ that shows how to use `IID_IMessageRaw` in **[IMsgStore::OpenEntry](imsgstore-openentry.md)** to obtain an **[IMessage](imessageimapiprop.md)** interface that manages a message in an offline folders file (OST) without forcing a download of the whole message when the client is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="2fd94-106">Cuando un cliente está en modo caché de Exchange, los mensajes del OST pueden estar en uno de estos dos estados:</span><span class="sxs-lookup"><span data-stu-id="2fd94-106">When a client is in Cached Exchange Mode, messages in the OST can be in one of two states:</span></span>
  
- <span data-ttu-id="2fd94-107">Se descarga el mensaje completo que contiene el encabezado y el cuerpo.</span><span class="sxs-lookup"><span data-stu-id="2fd94-107">The whole message that contains the header and the body is downloaded.</span></span>
    
- <span data-ttu-id="2fd94-108">Se descarga el mensaje con solo su encabezado.</span><span class="sxs-lookup"><span data-stu-id="2fd94-108">The message with only its header is downloaded.</span></span>
    
<span data-ttu-id="2fd94-109">Cuando solicite una interfaz **IMessage** para un mensaje en un OST y el cliente esté en modo caché de Exchange, use  `IID_IMessageRaw` .</span><span class="sxs-lookup"><span data-stu-id="2fd94-109">When you request an **IMessage** interface for a message in an OST and the client is in Cached Exchange Mode, use  `IID_IMessageRaw`.</span></span> <span data-ttu-id="2fd94-110">Si usa para solicitar una interfaz IMessage y si el mensaje solo tiene su encabezado descargado en ost, invoca una sincronización que intenta descargar `IID_IMessage` todo el mensaje. </span><span class="sxs-lookup"><span data-stu-id="2fd94-110">If you use  `IID_IMessage` to request an **IMessage** interface, and if the message has only its header downloaded in the OST, you invoke a synchronization that attempts to download the whole message.</span></span> 
  
<span data-ttu-id="2fd94-111">Si usa o  `IID_IMessageRaw` solicita una interfaz  `IID_IMessage` **IMessage,** las interfaces que se devuelven son idénticas en uso.</span><span class="sxs-lookup"><span data-stu-id="2fd94-111">If you use  `IID_IMessageRaw` or  `IID_IMessage` to request an **IMessage** interface, the interfaces that are returned are identical in use.</span></span> <span data-ttu-id="2fd94-112">La **interfaz IMessage** que se solicitó mediante el uso devuelve un mensaje de correo electrónico tal como existe en el OST, y la sincronización  `IID_IMessageRaw` no es forzada.</span><span class="sxs-lookup"><span data-stu-id="2fd94-112">The **IMessage** interface that was requested by using  `IID_IMessageRaw` returns an email message as it exists in the OST, and synchronization is not forced.</span></span> 
  
<span data-ttu-id="2fd94-113">En el siguiente ejemplo se muestra cómo llamar al **método OpenEntry,** pasando  `IID_IMessageRaw` en lugar de  `IID_IMessage` .</span><span class="sxs-lookup"><span data-stu-id="2fd94-113">The following example shows how to call the **OpenEntry** method, passing  `IID_IMessageRaw` instead of  `IID_IMessage`.</span></span>
  
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

<span data-ttu-id="2fd94-114">Si el **método OpenEntry** devuelve el MAPI_E_INTERFACE_NOT_SUPPORTED **de** error, indica que el almacén de mensajes no admite el acceso al mensaje en modo sin procesar.</span><span class="sxs-lookup"><span data-stu-id="2fd94-114">If the **OpenEntry** method returns the **MAPI_E_INTERFACE_NOT_SUPPORTED** error code, it indicates that the message store does not support accessing the message in raw mode.</span></span> <span data-ttu-id="2fd94-115">En esta situación, vuelva a intentar el **método OpenEntry** pasando  `IID_IMessage` .</span><span class="sxs-lookup"><span data-stu-id="2fd94-115">In this situation, try the **OpenEntry** method again by passing  `IID_IMessage`.</span></span>

> [!IMPORTANT]
>  <span data-ttu-id="2fd94-116">`IID_IMessageRaw` es posible que no se defina en el archivo de encabezado descargable que tiene actualmente.</span><span class="sxs-lookup"><span data-stu-id="2fd94-116">`IID_IMessageRaw` might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="2fd94-117">En este caso, puede agregarlo al código mediante la siguiente definición.</span><span class="sxs-lookup"><span data-stu-id="2fd94-117">In this case, you can add it to your code by using the following definition.</span></span> <span data-ttu-id="2fd94-118">Use la macro DEFINE_OLEGUID definida en el archivo de encabezado guiddef.h del Kit de desarrollo de software (SDK) de Microsoft Windows para asociar el nombre simbólico GUID con su valor.</span><span class="sxs-lookup"><span data-stu-id="2fd94-118">Use the DEFINE_OLEGUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the GUID symbolic name with its value.</span></span> >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a><span data-ttu-id="2fd94-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="2fd94-119">See also</span></span>

- [<span data-ttu-id="2fd94-120">Acerca de las adiciones de MAPI</span><span class="sxs-lookup"><span data-stu-id="2fd94-120">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="2fd94-121">Acceder a un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange</span><span class="sxs-lookup"><span data-stu-id="2fd94-121">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="2fd94-122">Abrir un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange</span><span class="sxs-lookup"><span data-stu-id="2fd94-122">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

