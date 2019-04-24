---
title: Implementación de la interfaz IUnknown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01bba63b-a2a1-490e-8b78-5c9ba8d9547b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5165476ea131e40153191e8625af5ea3c49f47b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310048"
---
# <a name="implementing-the-iunknown-interface"></a><span data-ttu-id="c22c7-103">Implementación de la interfaz IUnknown</span><span class="sxs-lookup"><span data-stu-id="c22c7-103">Implementing the IUnknown Interface</span></span>

  
  
<span data-ttu-id="c22c7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c22c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c22c7-105">Los métodos de la interfaz [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) , que se implementan en cada objeto MAPI, admiten la comunicación entre objetos y la administración de objetos.</span><span class="sxs-lookup"><span data-stu-id="c22c7-105">The methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface, implemented in every MAPI object, support interobject communication and object management.</span></span> 
  
 <span data-ttu-id="c22c7-106">**IUnknown** tiene tres métodos: [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)e [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c22c7-106">**IUnknown** has three methods: [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="c22c7-107">**QueryInterface** habilita un objeto para determinar si otro objeto admite una interfaz determinada.</span><span class="sxs-lookup"><span data-stu-id="c22c7-107">**QueryInterface** enables one object to determine whether another object supports a particular interface.</span></span> <span data-ttu-id="c22c7-108">Con **QueryInterface**, se puede interactuar con dos objetos que no tienen conocimientos previos sobre la funcionalidad de los demás.</span><span class="sxs-lookup"><span data-stu-id="c22c7-108">With **QueryInterface**, two objects with no prior knowledge of each other's functionality can interact.</span></span> <span data-ttu-id="c22c7-109">Si el objeto que implementa **QueryInterface** admite la interfaz en cuestión, devuelve un puntero a la implementación de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="c22c7-109">If the object that implements **QueryInterface** does support the interface in question, it returns a pointer to the implementation of the interface.</span></span> <span data-ttu-id="c22c7-110">Si el objeto no admite la interfaz solicitada, devuelve el valor MAPI_E_INTERFACE_NOT_SUPPORTED.</span><span class="sxs-lookup"><span data-stu-id="c22c7-110">If the object does not support the requested interface, it returns the MAPI_E_INTERFACE_NOT_SUPPORTED value.</span></span> 
  
<span data-ttu-id="c22c7-111">Cuando **QueryInterface** devuelve un puntero de interfaz solicitada, también debe aumentar el recuento de referencia del nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="c22c7-111">When **QueryInterface** returns a requested interface pointer, it must also increase the new object's reference count.</span></span> <span data-ttu-id="c22c7-112">El recuento de referencia de un objeto es un valor numérico que se usa para administrar la duración del objeto.</span><span class="sxs-lookup"><span data-stu-id="c22c7-112">An object's reference count is a numeric value used to manage the object's lifespan.</span></span> <span data-ttu-id="c22c7-113">Cuando el recuento de referencias es mayor que 1, la memoria del objeto no se puede liberar porque se está usando de forma activa.</span><span class="sxs-lookup"><span data-stu-id="c22c7-113">When the reference count is greater than 1, the object's memory cannot be freed because it is actively being used.</span></span> <span data-ttu-id="c22c7-114">Solo cuando el recuento de referencia cae a 0, el objeto puede liberarse de forma segura.</span><span class="sxs-lookup"><span data-stu-id="c22c7-114">It is only when the reference count drops to 0 that the object can be released safely.</span></span> 
  
<span data-ttu-id="c22c7-115">Los otros dos métodos **IUnknown** , **AddRef** y **Release**, administran el recuento de referencia.</span><span class="sxs-lookup"><span data-stu-id="c22c7-115">The other two **IUnknown** methods, **AddRef** and **Release**, manage the reference count.</span></span> <span data-ttu-id="c22c7-116">**AddRef** incrementa el recuento de referencias, mientras que **Release** lo reduce.</span><span class="sxs-lookup"><span data-stu-id="c22c7-116">**AddRef** increments the reference count, while **Release** decrements it.</span></span> <span data-ttu-id="c22c7-117">Todos los métodos o funciones de la API que devuelven punteros de interfaz, como **QueryInterface**, deben llamar a **AddRef** para incrementar el recuento de referencia.</span><span class="sxs-lookup"><span data-stu-id="c22c7-117">All methods or API functions that return interface pointers, such as **QueryInterface**, must call **AddRef** to increment the reference count.</span></span> <span data-ttu-id="c22c7-118">Todas las implementaciones de los métodos que reciben punteros de interfaz deben llamar a **Release** para disminuir el recuento cuando el puntero ya no es necesario.</span><span class="sxs-lookup"><span data-stu-id="c22c7-118">All implementations of methods that receive interface pointers must call **Release** to decrement the count when the pointer is no longer needed.</span></span> <span data-ttu-id="c22c7-119">La **versión** comprueba un recuento de referencias existente, liberando la memoria asociada a la interfaz sólo si el recuento es 0.</span><span class="sxs-lookup"><span data-stu-id="c22c7-119">**Release** checks for an existing reference count, freeing the memory associated with the interface only if the count is 0.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c22c7-120">Dado que no se requiere **AddRef** y **Release** para devolver valores precisos, los llamadores de estos métodos no deben usar los valores devueltos para determinar si un objeto sigue siendo válido o se ha destruido.</span><span class="sxs-lookup"><span data-stu-id="c22c7-120">Because **AddRef** and **Release** are not required to return accurate values, callers of these methods must not use the return values to determine whether an object is still valid or has been destroyed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c22c7-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="c22c7-121">See also</span></span>



[<span data-ttu-id="c22c7-122">Implementación de objetos MAPI</span><span class="sxs-lookup"><span data-stu-id="c22c7-122">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

