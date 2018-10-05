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
# <a name="implementing-iunknown-in-c"></a><span data-ttu-id="b9c14-103">Implementar la interfaz IUnknown en C++</span><span class="sxs-lookup"><span data-stu-id="b9c14-103">Implementing IUnknown in C++</span></span>

<span data-ttu-id="b9c14-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9c14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9c14-105">Implementación de los métodos de [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)e [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) de la interfaz [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) en C++ es bastante sencilla.</span><span class="sxs-lookup"><span data-stu-id="b9c14-105">Implementing the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface in C++ is fairly simple.</span></span> <span data-ttu-id="b9c14-106">Después de la validación de estándar de algunos de los parámetros que se pasan en, una implementación de **QueryInterface** comprueba el identificador de la interfaz solicitada respecto de la lista de las interfaces compatibles.</span><span class="sxs-lookup"><span data-stu-id="b9c14-106">After some standard validation of the parameters that are passed in, an implementation of **QueryInterface** checks the identifier of the requested interface against the list of supported interfaces.</span></span> <span data-ttu-id="b9c14-107">Si el identificador solicitado es entre las admitidas, se llama a **AddRef** y se devuelve el puntero **this** .</span><span class="sxs-lookup"><span data-stu-id="b9c14-107">If the requested identifier is among those supported, **AddRef** is called and the **this** pointer is returned.</span></span> <span data-ttu-id="b9c14-108">Si el identificador solicitado no está en la lista admitida, el puntero de salida se establece en NULL y se devuelve el valor MAPI_E_INTERFACE_NOT_SUPPORTED.</span><span class="sxs-lookup"><span data-stu-id="b9c14-108">If the requested identifier is not on the supported list, the output pointer is set to NULL and the MAPI_E_INTERFACE_NOT_SUPPORTED value is returned.</span></span> 
  
<span data-ttu-id="b9c14-109">En el ejemplo de código siguiente se muestra cómo puede implementar **QueryInterface** en C++ para un objeto de estado, un objeto que es una subclase de la [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interfaz.</span><span class="sxs-lookup"><span data-stu-id="b9c14-109">The following code example shows how you can implement **QueryInterface** in C++ for a status object, an object that is a subclass of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="b9c14-110">**IMAPIStatus** hereda de **IUnknown** a través de [IMAPIProp: IUnknown](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="b9c14-110">**IMAPIStatus** inherits from **IUnknown** through [IMAPIProp : IUnknown](imapipropiunknown.md).</span></span> <span data-ttu-id="b9c14-111">Por lo tanto, si se le pide un autor de la llamada para cualquiera de estas interfaces, el puntero **this** puede devolverse porque están relacionados con las interfaces a través de herencia.</span><span class="sxs-lookup"><span data-stu-id="b9c14-111">Therefore, if a caller asks for any of these interfaces, the **this** pointer can be returned because the interfaces are related through inheritance.</span></span> 
  
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

<span data-ttu-id="b9c14-112">En el ejemplo de código siguiente se muestra cómo implementar los métodos **AddRef** y **Release** para la `CMyMAPIObject` objeto.</span><span class="sxs-lookup"><span data-stu-id="b9c14-112">The following code example shows how to implement the **AddRef** and **Release** methods for the  `CMyMAPIObject` object.</span></span> <span data-ttu-id="b9c14-113">Debido a que la implementación de **AddRef** y **Release** es sencilla, eligen muchos proveedores de servicios implementarlos en línea.</span><span class="sxs-lookup"><span data-stu-id="b9c14-113">Because implementing **AddRef** and **Release** is straightforward, many service providers choose to implement them inline.</span></span> <span data-ttu-id="b9c14-114">Las llamadas a las funciones de Win32 **InterlockedIncrement** e **InterlockedDecrement** garantizar la seguridad del subproceso.</span><span class="sxs-lookup"><span data-stu-id="b9c14-114">The calls to the Win32 functions **InterlockedIncrement** and **InterlockedDecrement** ensure thread safety.</span></span> <span data-ttu-id="b9c14-115">La memoria para el objeto se libera el destructor, que se llama cuando el método **versión** elimina el objeto.</span><span class="sxs-lookup"><span data-stu-id="b9c14-115">The memory for the object is freed by the destructor, which is called when the **Release** method deletes the object.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="b9c14-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9c14-116">See also</span></span>

- [<span data-ttu-id="b9c14-117">Implementar objetos MAPI</span><span class="sxs-lookup"><span data-stu-id="b9c14-117">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)
- [<span data-ttu-id="b9c14-118">Implementar la interfaz IUnknown</span><span class="sxs-lookup"><span data-stu-id="b9c14-118">Implementing the IUnknown Interface</span></span>](implementing-the-iunknown-interface.md)

