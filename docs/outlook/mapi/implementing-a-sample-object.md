---
title: Implementación de un objeto de ejemplo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 23b6ad1a-0b50-429f-8819-ab72c56581c2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7d2f5fc2f26019902b27750613f7c360a751cd51
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582934"
---
# <a name="implementing-a-sample-object"></a><span data-ttu-id="4f9ae-103">Implementación de un objeto de ejemplo</span><span class="sxs-lookup"><span data-stu-id="4f9ae-103">Implementing a sample object</span></span>

<span data-ttu-id="4f9ae-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f9ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f9ae-105">Objetos del receptor de aviso: los objetos que admiten la [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) interfaz — son MAPI objetos que implementan las aplicaciones cliente para procesar las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="4f9ae-105">Advise sink objects — objects that support the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface — are MAPI objects that client applications implement for processing notifications.</span></span> <span data-ttu-id="4f9ae-106">**IMAPIAdviseSink** hereda directamente de [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) y contiene un solo método, **OnNotify**.</span><span class="sxs-lookup"><span data-stu-id="4f9ae-106">**IMAPIAdviseSink** inherits directly from [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) and contains only one method, **OnNotify**.</span></span> <span data-ttu-id="4f9ae-107">Por lo tanto, para implementar un objeto de receptor advise, un cliente crea código para los tres métodos de **IUnknown** y para [OnNotify](imapiadvisesink-onnotify.md).</span><span class="sxs-lookup"><span data-stu-id="4f9ae-107">Therefore, to implement an advise sink object, a client creates code for the three methods in **IUnknown** and for [OnNotify](imapiadvisesink-onnotify.md).</span></span>
  
<span data-ttu-id="4f9ae-108">El archivo de encabezado Mapidefs.h define una implementación de interfaz **IMAPIAdviseSink** utilizando **DECLARE_MAPI_INTERFACE**, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="4f9ae-108">The Mapidefs.h header file defines an **IMAPIAdviseSink** interface implementation by using **DECLARE_MAPI_INTERFACE**, as follows:</span></span>
  
```cpp
#define      INTERFACE  IMAPIAdviseSink
DECLARE_MAPI_INTERFACE_(IMAPIAdviseSink, IUnknown)
{
    BEGIN_INTERFACE
    MAPI_IUNKNOWN_METHODS(PURE)
    MAPI_IMAPIADVISESINK_METHODS(PURE)
};
 
```

<span data-ttu-id="4f9ae-109">Los clientes que implementan de aviso receptor objetos pueden definir sus interfaces en sus objetos manualmente o con las macros **MAPI_IUNKNOWN_METHODS** y **MAPI_IMAPIADVISESINK_METHODS** .</span><span class="sxs-lookup"><span data-stu-id="4f9ae-109">Clients that implement advise sink objects can define their interfaces in their objects manually or with the **MAPI_IUNKNOWN_METHODS** and **MAPI_IMAPIADVISESINK_METHODS** macros.</span></span> <span data-ttu-id="4f9ae-110">Los implementadores de objeto deben utilizar las macros de interfaz siempre que sea posible para garantizar la coherencia entre objetos y para ahorrar tiempo y esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="4f9ae-110">Object implementers should use the interface macros whenever possible to ensure consistency across objects and to save time and effort.</span></span> 
  
<span data-ttu-id="4f9ae-111">Implementación de los métodos de [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) e [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) es relativamente simple, debido a que normalmente se necesitan sólo unas pocas líneas de código.</span><span class="sxs-lookup"><span data-stu-id="4f9ae-111">Implementing the [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) and [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) methods is relatively simple because typically only a few lines of code are needed.</span></span> <span data-ttu-id="4f9ae-112">Por lo tanto, los clientes y proveedores de servicios que implementan objetos pueden hacer que sus implementaciones de **AddRef** y **Release** en línea.</span><span class="sxs-lookup"><span data-stu-id="4f9ae-112">Therefore, clients and service providers that implement objects can make their **AddRef** and **Release** implementations inline.</span></span> <span data-ttu-id="4f9ae-113">El código siguiente muestra cómo definir un C++ objeto receptor con implementaciones en línea de **AddRef** y **Release**de aviso.</span><span class="sxs-lookup"><span data-stu-id="4f9ae-113">The following code shows how to define a C++ advise sink object with inline implementations of **AddRef** and **Release**.</span></span>
  
```cpp
class  CMAPIAdviseSink : public IMAPIAdviseSink
{
public:
    STDMETHODIMP QueryInterface
                    (REFIID                     riid,
                     LPVOID *                   ppvObj);
    inline STDMETHODIMP_(ULONG) AddRef
                    () { InterlockedIncrement(m_cRef);
                         ++m_cRef;
                         InterlockedDecrement(m_cRef);
                         return m_cRef; };
    inline STDMETHODIMP_(ULONG) Release
                    () { InterlockedIncrement(m_cRef);
                         ULONG ulCount = --m_cRef;
                         InterlockedDecrement(m_cRef);
                         if (!ulCount)  delete this;
                         return ulCount;};
    MAPI_IMAPIADVISESINK_METHODS(IMPL);
    BOOL WINAPI AddConnection (LPMDB pMDBObj, ULONG ulConnection);
    void WINAPI RemoveAllLinks (LPMDB pMDBObj);
// Constructors and destructors.
public :
    inline CMAPIAdviseSink  (CStoreClient * pStore)
                            { m_cRef = 1;
                              m_ulConnection = 0;
                              m_pStore = pStore;
                              AddRef;};
    ~CMAPIAdviseSink () {Release};
private :
    ULONG               m_cRef;
    CStoreClient *      m_pStore;
    ULONG               m_ulConnection;
};
 
```

<span data-ttu-id="4f9ae-114">En C, el objeto de receptor de advise se compone de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="4f9ae-114">In C, the advise sink object is composed of the following elements:</span></span>
  
- <span data-ttu-id="4f9ae-115">Un puntero a una tabla virtual que contiene punteros a las implementaciones de cada uno de los métodos de **IUnknown** y **IMAPIAdviseSink**.</span><span class="sxs-lookup"><span data-stu-id="4f9ae-115">A pointer to a vtable that contains pointers to implementations of each of the methods in **IUnknown** and **IMAPIAdviseSink**.</span></span>
    
- <span data-ttu-id="4f9ae-116">Miembros de datos.</span><span class="sxs-lookup"><span data-stu-id="4f9ae-116">Data members.</span></span>
    
<span data-ttu-id="4f9ae-117">En el ejemplo de código siguiente se muestra cómo definir un objeto de receptor advise en C y construir su tabla vtable.</span><span class="sxs-lookup"><span data-stu-id="4f9ae-117">The following code example shows how to define an advise sink object in C and construct its vtable.</span></span> 
  
```cpp
// Object definition.
typedef struct _ADVISESINK
{
    const ADVISE_Vtbl FAR *    lpVtbl;
    ULONG             cRef;
    STORECLIENT      *pStore;
    ULONG             ulConnection;
} ADVISESINK, *LPADVISESINK;
// vtable definition.
static const ADVISE_Vtbl vtblADVISE =
{
    ADVISE_QueryInterface,
    ADVISE_AddRef,
    ADVISE_Release,
    ADVISE_OnNotify
};
 
```

<span data-ttu-id="4f9ae-118">Después de declarar un objeto de C, debe inicializar estableciendo el puntero vtable en la dirección de la tabla vtable construida, tal como se muestra en el siguiente código:</span><span class="sxs-lookup"><span data-stu-id="4f9ae-118">After you declare an object in C, you must initialize it by setting the vtable pointer to the address of the constructed vtable, as shown in the following code:</span></span>
  
```cpp
LPADVISESINK lpMyObj = NULL;
HRESULT hr = (*lpAllocateBuffer) (sizeof(ADVISESINK),
                 (LPVOID *)&lpMyObj);
lpMyObj->lpVtbl = &vtblADVISE;
 
```

## <a name="see-also"></a><span data-ttu-id="4f9ae-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f9ae-119">See also</span></span>

- [<span data-ttu-id="4f9ae-120">Información general sobre MAPI (propiedad)</span><span class="sxs-lookup"><span data-stu-id="4f9ae-120">MAPI Property Overview</span></span>](mapi-property-overview.md)
- [<span data-ttu-id="4f9ae-121">Implementar objetos MAPI</span><span class="sxs-lookup"><span data-stu-id="4f9ae-121">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

