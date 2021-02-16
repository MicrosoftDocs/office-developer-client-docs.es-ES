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
# <a name="implementing-iunknown-in-c"></a><span data-ttu-id="c5ff9-103">Implementar la interfaz IUnknown en C++</span><span class="sxs-lookup"><span data-stu-id="c5ff9-103">Implementing IUnknown in C++</span></span>

<span data-ttu-id="c5ff9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5ff9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5ff9-105">Implementar los métodos [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)e [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) de la interfaz [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) en C++ es bastante sencillo.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-105">Implementing the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface in C++ is fairly simple.</span></span> <span data-ttu-id="c5ff9-106">Después de una validación estándar de los parámetros que se pasan, una implementación de **QueryInterface** comprueba el identificador de la interfaz solicitada con la lista de interfaces admitidas.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-106">After some standard validation of the parameters that are passed in, an implementation of **QueryInterface** checks the identifier of the requested interface against the list of supported interfaces.</span></span> <span data-ttu-id="c5ff9-107">Si el identificador solicitado está entre los admitidos, se llama a **AddRef** y se **devuelve** este puntero.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-107">If the requested identifier is among those supported, **AddRef** is called and the **this** pointer is returned.</span></span> <span data-ttu-id="c5ff9-108">Si el identificador solicitado no está en la lista admitida, el puntero de salida se establece en NULL y se devuelve MAPI_E_INTERFACE_NOT_SUPPORTED valor.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-108">If the requested identifier is not on the supported list, the output pointer is set to NULL and the MAPI_E_INTERFACE_NOT_SUPPORTED value is returned.</span></span> 
  
<span data-ttu-id="c5ff9-109">En el siguiente ejemplo de código se muestra cómo implementar **QueryInterface** en C++ para un objeto de estado, un objeto que es una subclase de la [interfaz IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="c5ff9-109">The following code example shows how you can implement **QueryInterface** in C++ for a status object, an object that is a subclass of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="c5ff9-110">**IMAPIStatus** hereda de **IUnknown** a [través de IMAPIProp : IUnknown](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="c5ff9-110">**IMAPIStatus** inherits from **IUnknown** through [IMAPIProp : IUnknown](imapipropiunknown.md).</span></span> <span data-ttu-id="c5ff9-111">Por lo tanto, si el autor de  la llamada solicita cualquiera de estas interfaces, este puntero puede devolverse porque las interfaces están relacionadas a través de la herencia.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-111">Therefore, if a caller asks for any of these interfaces, the **this** pointer can be returned because the interfaces are related through inheritance.</span></span> 
  
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

<span data-ttu-id="c5ff9-112">En el siguiente ejemplo de código se muestra cómo implementar los **métodos AddRef** y **Release** para el  `CMyMAPIObject` objeto.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-112">The following code example shows how to implement the **AddRef** and **Release** methods for the  `CMyMAPIObject` object.</span></span> <span data-ttu-id="c5ff9-113">Dado que la **implementación de AddRef** y **Release** es sencilla, muchos proveedores de servicios eligen implementarlas en línea.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-113">Because implementing **AddRef** and **Release** is straightforward, many service providers choose to implement them inline.</span></span> <span data-ttu-id="c5ff9-114">Las llamadas a las funciones Win32 **InterlockedIncrement** e **InterlockedDecrement** garantizan la seguridad de los subprocesos.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-114">The calls to the Win32 functions **InterlockedIncrement** and **InterlockedDecrement** ensure thread safety.</span></span> <span data-ttu-id="c5ff9-115">El destructor libera la memoria del objeto, que se llama cuando el **método Release** elimina el objeto.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-115">The memory for the object is freed by the destructor, which is called when the **Release** method deletes the object.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="c5ff9-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c5ff9-116">See also</span></span>

- [<span data-ttu-id="c5ff9-117">Implementación de objetos MAPI</span><span class="sxs-lookup"><span data-stu-id="c5ff9-117">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)
- [<span data-ttu-id="c5ff9-118">Implementación de la interfaz IUnknown</span><span class="sxs-lookup"><span data-stu-id="c5ff9-118">Implementing the IUnknown Interface</span></span>](implementing-the-iunknown-interface.md)

