---
title: Implementar la interfaz IUnknown en C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 68519f6c-fba8-47f5-9401-316e276f770e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 08f3f3f937320d8a986b2002c761a37f0f749227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330180"
---
# <a name="implementing-iunknown-in-c"></a>Implementar la interfaz IUnknown en C++

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Implementar los métodos [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)e [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) de la interfaz [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) en C++ es bastante sencillo. Después de una validación estándar de los parámetros que se pasan, una implementación de **QueryInterface** comprueba el identificador de la interfaz solicitada con la lista de interfaces admitidas. Si el identificador solicitado está entre los admitidos, se llama a **AddRef** y se **devuelve** este puntero. Si el identificador solicitado no está en la lista admitida, el puntero de salida se establece en NULL y se devuelve MAPI_E_INTERFACE_NOT_SUPPORTED valor. 
  
En el siguiente ejemplo de código se muestra cómo implementar **QueryInterface** en C++ para un objeto de estado, un objeto que es una subclase de la [interfaz IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md) **IMAPIStatus** hereda de **IUnknown** a [través de IMAPIProp : IUnknown](imapipropiunknown.md). Por lo tanto, si el autor de  la llamada solicita cualquiera de estas interfaces, este puntero puede devolverse porque las interfaces están relacionadas a través de la herencia. 
  
```cpp
HRESULT CMyMAPIObject::QueryInterface (REFIID   riid,
                                       LPVOID * ppvObj)
{
    // Always set out parameter to NULL, validating it first.
    if (!ppvObj)
        return E_INVALIDARG;
    *ppvObj = NULL;
    if (riid == IID_IUnknown || riid == IID_IMAPIProp ||
        riid == IID_IMAPIStatus)
    {
        // Increment the reference count and return the pointer.
        *ppvObj = (LPVOID)this;
        AddRef();
        return NOERROR;
    }
    return E_NOINTERFACE;
}

```

En el siguiente ejemplo de código se muestra cómo implementar los **métodos AddRef** y **Release** para el  `CMyMAPIObject` objeto. Dado que la **implementación de AddRef** y **Release** es sencilla, muchos proveedores de servicios eligen implementarlas en línea. Las llamadas a las funciones Win32 **InterlockedIncrement** e **InterlockedDecrement** garantizan la seguridad de los subprocesos. El destructor libera la memoria del objeto, que se llama cuando el **método Release** elimina el objeto. 
  
```cpp
ULONG CMyMAPIObject::AddRef()
{
    InterlockedIncrement(m_cRef);
    return m_cRef;
}
ULONG CMyMAPIObject::Release()
{
    // Decrement the object's internal counter.
    ULONG ulRefCount = InterlockedDecrement(m_cRef);
    if (0 == m_cRef)
    {
        delete this;
    }
    return ulRefCount;
}
 
```

## <a name="see-also"></a>Consulte también

- [Implementación de objetos MAPI](implementing-mapi-objects.md)
- [Implementación de la interfaz IUnknown](implementing-the-iunknown-interface.md)

