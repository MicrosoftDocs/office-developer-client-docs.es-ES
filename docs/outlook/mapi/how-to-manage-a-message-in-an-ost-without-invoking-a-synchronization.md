---
title: Administrar mensajes en OST sin invocar una sincronización en el modo caché de Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: 'Contiene un ejemplo de código en C++ que muestra cómo usar IID_IMessageRaw en IMsgStore:: OpenEntry para obtener una interfaz IMessage que administra un mensaje en un archivo de carpetas sin conexión (OST) sin forzar la descarga de todo el mensaje cuando el cliente está en caché de Exchange Modo.'
ms.openlocfilehash: e50637b496ff43daedad2df27d027d8a6d0dc743
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316397"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a><span data-ttu-id="e20d7-103">Administrar mensajes en OST sin invocar una sincronización en el modo caché de Exchange</span><span class="sxs-lookup"><span data-stu-id="e20d7-103">Manage messages in OST without invoking a synchronization in Cached Exchange mode</span></span>

<span data-ttu-id="e20d7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e20d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e20d7-105">Este tema contiene un ejemplo de código en C++ que muestra cómo usar `IID_IMessageRaw` en **[IMsgStore:: OpenEntry](imsgstore-openentry.md)** para obtener una interfaz **[IMessage](imessageimapiprop.md)** que administra un mensaje en un archivo de carpetas sin conexión (OST) sin forzar la descarga de todo el mensaje cuando el cliente está en modo caché de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e20d7-105">This topic contains a code sample in C++ that shows how to use `IID_IMessageRaw` in **[IMsgStore::OpenEntry](imsgstore-openentry.md)** to obtain an **[IMessage](imessageimapiprop.md)** interface that manages a message in an offline folders file (OST) without forcing a download of the whole message when the client is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="e20d7-106">Cuando un cliente está en modo de intercambio en caché, los mensajes del OST pueden estar en uno de estos dos Estados:</span><span class="sxs-lookup"><span data-stu-id="e20d7-106">When a client is in Cached Exchange Mode, messages in the OST can be in one of two states:</span></span>
  
- <span data-ttu-id="e20d7-107">Se descarga el mensaje completo que contiene el encabezado y el cuerpo.</span><span class="sxs-lookup"><span data-stu-id="e20d7-107">The whole message that contains the header and the body is downloaded.</span></span>
    
- <span data-ttu-id="e20d7-108">Se descarga el mensaje que solo tiene su encabezado.</span><span class="sxs-lookup"><span data-stu-id="e20d7-108">The message with only its header is downloaded.</span></span>
    
<span data-ttu-id="e20d7-109">Cuando se solicita una interfaz **IMessage** para un mensaje en un Ost y el cliente está en modo de intercambio en caché, `IID_IMessageRaw`use.</span><span class="sxs-lookup"><span data-stu-id="e20d7-109">When you request an **IMessage** interface for a message in an OST and the client is in Cached Exchange Mode, use  `IID_IMessageRaw`.</span></span> <span data-ttu-id="e20d7-110">Si se usa `IID_IMessage` para solicitar una interfaz **IMessage** y si el mensaje solo tiene su encabezado descargado en Ost, se invoca una sincronización que intenta descargar el mensaje completo.</span><span class="sxs-lookup"><span data-stu-id="e20d7-110">If you use  `IID_IMessage` to request an **IMessage** interface, and if the message has only its header downloaded in the OST, you invoke a synchronization that attempts to download the whole message.</span></span> 
  
<span data-ttu-id="e20d7-111">Si usa `IID_IMessageRaw` o `IID_IMessage` para solicitar una interfaz **IMessage** , las interfaces que se devuelven son idénticas en uso.</span><span class="sxs-lookup"><span data-stu-id="e20d7-111">If you use  `IID_IMessageRaw` or  `IID_IMessage` to request an **IMessage** interface, the interfaces that are returned are identical in use.</span></span> <span data-ttu-id="e20d7-112">La interfaz **IMessage** que se solicitó mediante `IID_IMessageRaw` la devolución de un mensaje de correo electrónico como existe en el Ost y la sincronización no se ha forzado.</span><span class="sxs-lookup"><span data-stu-id="e20d7-112">The **IMessage** interface that was requested by using  `IID_IMessageRaw` returns an email message as it exists in the OST, and synchronization is not forced.</span></span> 
  
<span data-ttu-id="e20d7-113">En el ejemplo siguiente se muestra cómo llamar al método **OpenEntry** , `IID_IMessageRaw` pasando en lugar `IID_IMessage`de.</span><span class="sxs-lookup"><span data-stu-id="e20d7-113">The following example shows how to call the **OpenEntry** method, passing  `IID_IMessageRaw` instead of  `IID_IMessage`.</span></span>
  
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

<span data-ttu-id="e20d7-114">Si el método **OpenEntry** devuelve el código de error **MAPI_E_INTERFACE_NOT_SUPPORTED** , indica que el almacén de mensajes no admite el acceso al mensaje en modo sin procesar.</span><span class="sxs-lookup"><span data-stu-id="e20d7-114">If the **OpenEntry** method returns the **MAPI_E_INTERFACE_NOT_SUPPORTED** error code, it indicates that the message store does not support accessing the message in raw mode.</span></span> <span data-ttu-id="e20d7-115">En esta situación, pruebe el método **OpenEntry** de nuevo pasando `IID_IMessage`.</span><span class="sxs-lookup"><span data-stu-id="e20d7-115">In this situation, try the **OpenEntry** method again by passing  `IID_IMessage`.</span></span>

> [!IMPORTANT]
>  <span data-ttu-id="e20d7-116">`IID_IMessageRaw`puede que no esté definida en el archivo de encabezado descargable que tiene actualmente.</span><span class="sxs-lookup"><span data-stu-id="e20d7-116">`IID_IMessageRaw` might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="e20d7-117">En este caso, puede agregarlo al código con la siguiente definición.</span><span class="sxs-lookup"><span data-stu-id="e20d7-117">In this case, you can add it to your code by using the following definition.</span></span> <span data-ttu-id="e20d7-118">Use la macro DEFINE_OLEGUID definida en el archivo de encabezado guiddef. h del kit de desarrollo de software (SDK) de Microsoft Windows para asociar el nombre simbólico GUID con su valor.</span><span class="sxs-lookup"><span data-stu-id="e20d7-118">Use the DEFINE_OLEGUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the GUID symbolic name with its value.</span></span> >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a><span data-ttu-id="e20d7-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="e20d7-119">See also</span></span>

- [<span data-ttu-id="e20d7-120">Acerca de las adiciones de MAPI</span><span class="sxs-lookup"><span data-stu-id="e20d7-120">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="e20d7-121">Acceder a un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange</span><span class="sxs-lookup"><span data-stu-id="e20d7-121">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="e20d7-122">Abrir un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange</span><span class="sxs-lookup"><span data-stu-id="e20d7-122">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

