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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397838"
---
# <a name="implementing-iunknown-in-c"></a>Implementar la interfaz IUnknown en C++

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Implementación de los métodos de [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)e [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) de la interfaz [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) en C++ es bastante sencilla. Después de la validación de estándar de algunos de los parámetros que se pasan en, una implementación de **QueryInterface** comprueba el identificador de la interfaz solicitada respecto de la lista de las interfaces compatibles. Si el identificador solicitado es entre las admitidas, se llama a **AddRef** y se devuelve el puntero **this** . Si el identificador solicitado no está en la lista admitida, el puntero de salida se establece en NULL y se devuelve el valor MAPI_E_INTERFACE_NOT_SUPPORTED. 
  
En el ejemplo de código siguiente se muestra cómo puede implementar **QueryInterface** en C++ para un objeto de estado, un objeto que es una subclase de la [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interfaz. **IMAPIStatus** hereda de **IUnknown** a través de [IMAPIProp: IUnknown](imapipropiunknown.md). Por lo tanto, si se le pide un autor de la llamada para cualquiera de estas interfaces, el puntero **this** puede devolverse porque están relacionados con las interfaces a través de herencia. 
  
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

En el ejemplo de código siguiente se muestra cómo implementar los métodos **AddRef** y **Release** para la `CMyMAPIObject` objeto. Debido a que la implementación de **AddRef** y **Release** es sencilla, eligen muchos proveedores de servicios implementarlos en línea. Las llamadas a las funciones de Win32 **InterlockedIncrement** e **InterlockedDecrement** garantizar la seguridad del subproceso. La memoria para el objeto se libera el destructor, que se llama cuando el método **versión** elimina el objeto. 
  
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

## <a name="see-also"></a>Vea también

- [Implementar objetos MAPI](implementing-mapi-objects.md)
- [Implementar la interfaz IUnknown](implementing-the-iunknown-interface.md)

