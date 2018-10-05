---
title: Obtener acceso a un mensaje en un almacén IMAP sin descargar el mensaje completo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2a93ab3e-798f-5741-d5e0-bba8c6b437c7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 194131148cc36dfff791b4cfae01862e8bbef5cb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398447"
---
# <a name="access-a-message-on-an-imap-store-without-downloading-the-entire-message"></a><span data-ttu-id="99801-103">Obtener acceso a un mensaje en un almacén IMAP sin descargar el mensaje completo</span><span class="sxs-lookup"><span data-stu-id="99801-103">Access a message on an IMAP store without downloading the entire message</span></span>

<span data-ttu-id="99801-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99801-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99801-105">En este tema se muestra un ejemplo de código en C++ que las consultas de un almacén de mensajes para la interfaz de **[IProxyStoreObject](iproxystoreobject.md)** y usa el puntero devuelto y la función **[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md)** para obtener un puntero a un objeto de almacén IMAP que ha sido los secretos de.</span><span class="sxs-lookup"><span data-stu-id="99801-105">This topic shows a code sample in C++ that queries a message store for the **[IProxyStoreObject](iproxystoreobject.md)** interface, and uses the returned pointer and the **[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md)** function to obtain a pointer to an IMAP store object that has been unwrapped.</span></span> <span data-ttu-id="99801-106">Uso de este almacén no ajustado permite el acceso a un mensaje en su estado actual sin invocar una descarga de todo el mensaje.</span><span class="sxs-lookup"><span data-stu-id="99801-106">Using this unwrapped store allows access to a message in its current state without invoking a download of the entire message.</span></span> 
  
<span data-ttu-id="99801-107">Debido a que **UnwrapNoRef** no incrementa el recuento de referencias para este nuevo puntero al objeto de almacén no ajustado, después de llamar correctamente a **UnwrapNoRef**, se debe llamar a [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) para mantener el recuento de referencia.</span><span class="sxs-lookup"><span data-stu-id="99801-107">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you must call [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) to maintain the reference count.</span></span> 
  
```cpp
HRESULT HrUnWrapMDB(LPMDB lpMDBIn, LPMDB* lppMDBOut) 
{ 
    HRESULT hRes = S_OK; 
    IProxyStoreObject* lpProxyObj = NULL; 
    LPMDB lpUnwrappedMDB = NULL; 
    hRes = lpMDBIn->QueryInterface(IID_IProxyStoreObject,(void**)&lpProxyObj); 
    if (SUCCEEDED(hRes) && lpProxyObj) 
    { 
        hRes = lpProxyObj->UnwrapNoRef((LPVOID*)&lpUnwrappedMDB); 
        if (SUCCEEDED(hRes) && lpUnwrappedMDB) 
        { 
            // UnwrapNoRef doesn't addref, so do it here 
            lpUnwrappedMDB->AddRef(); 
            (*lppMDBOut) = lpUnwrappedMDB; 
        } 
    } 
    if (lpProxyObj) lpProxyObj->Release(); 
    return hRes; 
}
```


