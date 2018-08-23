---
title: Obtener acceso a un mensaje en un almacén IMAP sin descargar el mensaje completo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2a93ab3e-798f-5741-d5e0-bba8c6b437c7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5a5a327ff74a4058d8eb15928912ca075e55ea95
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564391"
---
# <a name="access-a-message-on-an-imap-store-without-downloading-the-entire-message"></a>Obtener acceso a un mensaje en un almacén IMAP sin descargar el mensaje completo

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En este tema se muestra un ejemplo de código en C++ que las consultas de un almacén de mensajes para la interfaz de **[IProxyStoreObject](iproxystoreobject.md)** y usa el puntero devuelto y la función **[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md)** para obtener un puntero a un objeto de almacén IMAP que ha sido los secretos de. Uso de este almacén no ajustado permite el acceso a un mensaje en su estado actual sin invocar una descarga de todo el mensaje. 
  
Debido a que **UnwrapNoRef** no incrementa el recuento de referencias para este nuevo puntero al objeto de almacén no ajustado, después de llamar correctamente a **UnwrapNoRef**, se debe llamar a [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) para mantener el recuento de referencia. 
  
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


