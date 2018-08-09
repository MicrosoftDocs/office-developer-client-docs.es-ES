---
title: Implementar la interfaz IUnknown en C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 807b6dc4-cdb7-40a4-87d7-ebc1ad5fab76
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d12201d8476d15021e896a44797ae5fc21178802
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817700"
---
# <a name="implementing-iunknown-in-c"></a>Implementar la interfaz IUnknown en C

**Hace referencia a**: Outlook 
  
Las implementaciones del método [IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) en C son muy similares a las implementaciones de C++. Hay dos pasos básicos para la implementación: 
  
1. Validación de parámetros.
    
2. El identificador de la interfaz solicitada respecto de la lista de interfaces compatibles con el objeto de comprobación y devolver el valor E_NO_INTERFACE o un puntero de interfaz válido. Si se devuelve un puntero de interfaz, la implementación también debe llamar al método [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) para incrementar el recuento de referencia. 
    
La diferencia principal entre una implementación de **QueryInterface** en C y C++ es el primer parámetro adicional en la versión de C. Dado que el puntero de objeto se agrega a la lista de parámetros, una implementación de C de **QueryInterface** debe tener más validación de parámetro que una implementación de C++. La lógica para comprobar el identificador de interfaz, incrementar el recuento de referencia y la devolución de un puntero de objeto debe ser idéntica en ambos lenguajes. 
  
En el ejemplo de código siguiente se muestra cómo implementar **QueryInterface** en C para un objeto de estado. 
  
```cpp
STDMETHODIMP STATUS_QueryInterface(LPMYSTATUSOBJ lpMyObj, REFIID riid,
                                   LPVOID FAR * lppvObj)
{
    HRESULT hr = hrSuccess;
    // Validate the object pointer.
    if (!lpMyObj || lpMyObj->lpVtbl != &vtblSTATUS )
    {
        hr = ResultFromScode(E_INVALIDARG);
        return hr;
    }
    // Validate other parameters.
    if (!lppvObj)
    {
        hr = ResultFromScode(E_INVALIDARG);
        return hr;
    }
    // Set the output pointer to NULL.
    *lppvObj = NULL;
    // Check the interface identifier.
    if (memcmp(riid, &IID_IUnknown, sizeof(IID)) &&
        memcmp(riid, &IID_IMAPIProp, sizeof(IID)) &&
        memcmp(riid, &IID_IMAPIStatus, sizeof(IID)))
    {
        hr = ResultFromScode(E_NOINTERFACE);
        return hr;
    }
    // The interface is supported. Increment the reference count and return.
    lpMyObj->lpVtbl->AddRef(lpMyObj);
    *lppvObj = lpMyObj;
    return hr;
}

```

Mientras que la implementación del método **AddRef** en C es similar a una implementación de C++, una implementación de C del método [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) puede obtener más elaborada que una versión de C++. Esto es debido a que muchas de las funciones relacionadas con la liberación de un objeto pueden incorporarse en el constructor de C++ y el destructor y C no tiene ningún mecanismo de este tipo. Toda esta funcionalidad debe estar incluido en el método de la **versión** . Además, debido a los parámetros adicionales y su tabla vtable explícita, validación más es necesario. 
  
La siguiente llamada al método **AddRef** ilustra una implementación típica de C para un objeto de estado. 
  
```cpp
STDMETHODIMP_(ULONG) STATUS_AddRef(LPMYSTATUSOBJ lpMyObj)
{
    LONG cRef;
    // Check to see whether it has a lpVtbl object member.
    if (!lpMyObj || lpMyObj->lpVtbl != &vtblSTATUS)
    {
        return 1;
    }
    // Check the method.
    if (STATUS_AddRef != lpMyObj->lpVtbl->AddRef)
    {
        return 1;
    }
    InterlockedIncrement(lpMyObj->cRef);
    cRef = ++lpMyObj->cRef;
    InterlockedDecrement (lpMyObj->cRef);
    return cRef;
}

```

En el ejemplo de código siguiente se muestra una implementación típica de **versión** para un objeto de estado de C. Si el recuento de referencia es 0 una vez disminuye, una implementación de objeto de estado de C debe realizar las siguientes tareas: 
  
- Cualquier retenidos punteros a objetos de la versión. 
    
- Establecer la tabla vtable en NULL, facilitar la depuración en el caso donde usuario de un objeto denominado **versión** aún siguió intenta usar el objeto. 
    
- Llamar a **MAPIFreeBuffer** para liberar el objeto. 
    
```cpp
STDMETHODIMP_(ULONG) STATUS_Release(LPMYSTATUSOBJ lpMyObj)
{
    LONG cRef;
    // Check the size of the vtable.
    if (!lpMyObj)
    {
        return 1;
    }
    // Check whether the vtable is correct.
    if (lpMyObj->lpVtbl != &vtblSTATUS)
    {
        return 1;
    }
    InterlockedIncrement(lpMyObj->cRef);
    cRef = --lpMyObj->cRef;
    InterlockedIncrement (lpMyObj->cRef);
    if (cRef == 0)
    {
        lpMyObj->lpVtbl->Release(lpMyObj);
        DeleteCriticalSection(&lpMyObj->cs);
        // Release the IMAPIProp pointer.
        lpMyObj->lpProp->Release(lpMyObj->lpProp);
        lpMyObj->lpVtbl = NULL;
        lpMyObj->lpFreeBuff(lpMyObj);
        return 0;
    }
    return cRef;
}

```

## <a name="see-also"></a>Vea también

- [Implementar objetos MAPI](implementing-mapi-objects.md)
- [Implementar la interfaz IUnknown](implementing-the-iunknown-interface.md)

