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
# <a name="implementing-iunknown-in-c"></a><span data-ttu-id="9bb01-103">Implementar la interfaz IUnknown en C</span><span class="sxs-lookup"><span data-stu-id="9bb01-103">Implementing IUnknown in C</span></span>

<span data-ttu-id="9bb01-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9bb01-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9bb01-105">Las implementaciones del método [IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) en C son muy similares a las implementaciones de C++.</span><span class="sxs-lookup"><span data-stu-id="9bb01-105">Implementations of the [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) method in C are very similar to C++ implementations.</span></span> <span data-ttu-id="9bb01-106">Hay dos pasos básicos para la implementación:</span><span class="sxs-lookup"><span data-stu-id="9bb01-106">There are two basic steps to the implementation:</span></span> 
  
1. <span data-ttu-id="9bb01-107">Validación de parámetros.</span><span class="sxs-lookup"><span data-stu-id="9bb01-107">Validating parameters.</span></span>
    
2. <span data-ttu-id="9bb01-108">El identificador de la interfaz solicitada respecto de la lista de interfaces compatibles con el objeto de comprobación y devolver el valor E_NO_INTERFACE o un puntero de interfaz válido.</span><span class="sxs-lookup"><span data-stu-id="9bb01-108">Checking the identifier of the requested interface against the list of interfaces supported by the object and returning either the E_NO_INTERFACE value or a valid interface pointer.</span></span> <span data-ttu-id="9bb01-109">Si se devuelve un puntero de interfaz, la implementación también debe llamar al método [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) para incrementar el recuento de referencia.</span><span class="sxs-lookup"><span data-stu-id="9bb01-109">If an interface pointer is returned, the implementation should also call the [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) method to increment the reference count.</span></span> 
    
<span data-ttu-id="9bb01-110">La diferencia principal entre una implementación de **QueryInterface** en C y C++ es el primer parámetro adicional en la versión de C.</span><span class="sxs-lookup"><span data-stu-id="9bb01-110">The main difference between an implementation of **QueryInterface** in C and C++ is the additional first parameter in the C version.</span></span> <span data-ttu-id="9bb01-111">Dado que el puntero de objeto se agrega a la lista de parámetros, una implementación de C de **QueryInterface** debe tener más validación de parámetro que una implementación de C++.</span><span class="sxs-lookup"><span data-stu-id="9bb01-111">Because the object pointer is added to the parameter list, a C implementation of **QueryInterface** must have more parameter validation than a C++ implementation.</span></span> <span data-ttu-id="9bb01-112">La lógica para comprobar el identificador de interfaz, incrementar el recuento de referencia y la devolución de un puntero de objeto debe ser idéntica en ambos lenguajes.</span><span class="sxs-lookup"><span data-stu-id="9bb01-112">The logic for checking the interface identifier, incrementing the reference count, and returning an object pointer should be identical in both languages.</span></span> 
  
<span data-ttu-id="9bb01-113">En el ejemplo de código siguiente se muestra cómo implementar **QueryInterface** en C para un objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="9bb01-113">The following code example shows how to implement **QueryInterface** in C for a status object.</span></span> 
  
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

<span data-ttu-id="9bb01-114">Mientras que la implementación del método **AddRef** en C es similar a una implementación de C++, una implementación de C del método [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) puede obtener más elaborada que una versión de C++.</span><span class="sxs-lookup"><span data-stu-id="9bb01-114">Whereas the implementation of the **AddRef** method in C is similar to a C++ implementation, a C implementation of the [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method can get more elaborate than a C++ version.</span></span> <span data-ttu-id="9bb01-115">Esto es debido a que muchas de las funciones relacionadas con la liberación de un objeto pueden incorporarse en el constructor de C++ y el destructor y C no tiene ningún mecanismo de este tipo.</span><span class="sxs-lookup"><span data-stu-id="9bb01-115">This is because much of the functionality involved with freeing an object can be incorporated into the C++ constructor and destructor, and C has no such mechanism.</span></span> <span data-ttu-id="9bb01-116">Toda esta funcionalidad debe estar incluido en el método de la **versión** .</span><span class="sxs-lookup"><span data-stu-id="9bb01-116">All of this functionality must be included in the **Release** method.</span></span> <span data-ttu-id="9bb01-117">Además, debido a los parámetros adicionales y su tabla vtable explícita, validación más es necesario.</span><span class="sxs-lookup"><span data-stu-id="9bb01-117">Also, because of the additional parameter and its explicit vtable, more validation is required.</span></span> 
  
<span data-ttu-id="9bb01-118">La siguiente llamada al método **AddRef** ilustra una implementación típica de C para un objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="9bb01-118">The following **AddRef** method call illustrates a typical C implementation for a status object.</span></span> 
  
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

<span data-ttu-id="9bb01-119">En el ejemplo de código siguiente se muestra una implementación típica de **versión** para un objeto de estado de C.</span><span class="sxs-lookup"><span data-stu-id="9bb01-119">The following code example shows a typical implementation of **Release** for a C status object.</span></span> <span data-ttu-id="9bb01-120">Si el recuento de referencia es 0 una vez disminuye, una implementación de objeto de estado de C debe realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="9bb01-120">If the reference count is 0 after it is decremented, a C status object implementation should perform the following tasks:</span></span> 
  
- <span data-ttu-id="9bb01-121">Cualquier retenidos punteros a objetos de la versión.</span><span class="sxs-lookup"><span data-stu-id="9bb01-121">Release any held pointers to objects.</span></span> 
    
- <span data-ttu-id="9bb01-122">Establecer la tabla vtable en NULL, facilitar la depuración en el caso donde usuario de un objeto denominado **versión** aún siguió intenta usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="9bb01-122">Set the vtable to NULL, facilitating debugging in the case where an object's user called **Release** yet continued to try to use the object.</span></span> 
    
- <span data-ttu-id="9bb01-123">Llamar a **MAPIFreeBuffer** para liberar el objeto.</span><span class="sxs-lookup"><span data-stu-id="9bb01-123">Call **MAPIFreeBuffer** to free the object.</span></span> 
    
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

## <a name="see-also"></a><span data-ttu-id="9bb01-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="9bb01-124">See also</span></span>

- [<span data-ttu-id="9bb01-125">Implementar objetos MAPI</span><span class="sxs-lookup"><span data-stu-id="9bb01-125">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)
- [<span data-ttu-id="9bb01-126">Implementar la interfaz IUnknown</span><span class="sxs-lookup"><span data-stu-id="9bb01-126">Implementing the IUnknown Interface</span></span>](implementing-the-iunknown-interface.md)
