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
ms.openlocfilehash: 3c634defcad76755fc6604a23d2091bb21e15111
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346777"
---
# <a name="implementing-iunknown-in-c"></a>Implementar la interfaz IUnknown en C

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las implementaciones del [método IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) en C son muy similares a las implementaciones de C++. Hay dos pasos básicos para la implementación: 
  
1. Validación de parámetros.
    
2. Comprobar el identificador de la interfaz solicitada con la lista de interfaces admitidas por el objeto y devolver el valor E_NO_INTERFACE o un puntero de interfaz válido. Si se devuelve un puntero de interfaz, la implementación también debe llamar al método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) para incrementar el recuento de referencias. 
    
La principal diferencia entre una implementación de **QueryInterface** en C y C++ es el primer parámetro adicional de la versión C. Dado que el puntero de objeto se agrega a la lista de parámetros, una implementación de C de **QueryInterface** debe tener más validación de parámetros que una implementación de C++. La lógica para comprobar el identificador de interfaz, incrementar el recuento de referencias y devolver un puntero de objeto debe ser idéntica en ambos idiomas. 
  
En el siguiente ejemplo de código se muestra cómo implementar **QueryInterface** en C para un objeto de estado. 
  
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

Mientras que la implementación del **método AddRef** en C es similar a una implementación de C++, una implementación de C del método [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) puede ser más compleja que una versión de C++. Esto se debe a que gran parte de la funcionalidad necesaria para liberar un objeto se puede incorporar al constructor y destructor de C++, y C no tiene dicho mecanismo. Toda esta funcionalidad debe incluirse en el **método Release.** Además, debido al parámetro adicional y a su tabla virtual explícita, se requiere más validación. 
  
La siguiente **llamada al método AddRef** ilustra una implementación típica de C para un objeto de estado. 
  
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

En el siguiente ejemplo de código se muestra una implementación típica de **Release** para un objeto de estado C. Si el recuento de referencias es 0 después de que se disminuye, una implementación de objeto de estado C debe realizar las siguientes tareas: 
  
- Libera los punteros que se mantienen en los objetos. 
    
- Establezca la tabla virtual en NULL, facilitando la depuración en caso de que el usuario de un objeto llamado **Release** continúe intentando usar el objeto. 
    
- Llama **a MAPIFreeBuffer** para liberar el objeto. 
    
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

## <a name="see-also"></a>Consulte también

- [Implementación de objetos MAPI](implementing-mapi-objects.md)
- [Implementación de la interfaz IUnknown](implementing-the-iunknown-interface.md)

