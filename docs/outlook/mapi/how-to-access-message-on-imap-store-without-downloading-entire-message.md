---
title: Obtener acceso a un mensaje en un almacén IMAP sin descargar todo el mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2a93ab3e-798f-5741-d5e0-bba8c6b437c7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 194131148cc36dfff791b4cfae01862e8bbef5cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299079"
---
# <a name="access-a-message-on-an-imap-store-without-downloading-the-entire-message"></a>Obtener acceso a un mensaje en un almacén IMAP sin descargar todo el mensaje

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En este tema se muestra un ejemplo de código en C++ que consulta un almacén de mensajes para la interfaz **[IProxyStoreObject](iproxystoreobject.md)** y usa el puntero devuelto y la función **[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md)** para obtener un puntero a un objeto de almacén IMAP que se ha desencapsulado. El uso de este almacén sin envolver permite el acceso a un mensaje en su estado actual sin invocar una descarga de todo el mensaje. 
  
Dado que **UnwrapNoRef** no incrementa el recuento de referencias para este nuevo puntero al objeto de almacén sin envolver, después de llamar correctamente **a UnwrapNoRef**, debe llamar a [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) para mantener el recuento de referencias. 
  
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


