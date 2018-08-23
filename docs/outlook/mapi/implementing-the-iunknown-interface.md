---
title: Implementar la interfaz IUnknown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01bba63b-a2a1-490e-8b78-5c9ba8d9547b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f9ab3b75743d882aca0145b73b8ef707204cc8de
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571902"
---
# <a name="implementing-the-iunknown-interface"></a><span data-ttu-id="9028e-103">Implementar la interfaz IUnknown</span><span class="sxs-lookup"><span data-stu-id="9028e-103">Implementing the IUnknown Interface</span></span>

  
  
<span data-ttu-id="9028e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9028e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9028e-105">Los métodos de la interfaz [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) , implementada en cada objeto MAPI, admiten la administración de comunicación y objeto entre.</span><span class="sxs-lookup"><span data-stu-id="9028e-105">The methods of the [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) interface, implemented in every MAPI object, support interobject communication and object management.</span></span> 
  
 <span data-ttu-id="9028e-106">**IUnknown** tiene tres métodos: [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx), [IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)e [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="9028e-106">**IUnknown** has three methods: [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx), [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx), and [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="9028e-107">**QueryInterface** permite a un objeto determinar si otro objeto admite una interfaz determinada.</span><span class="sxs-lookup"><span data-stu-id="9028e-107">**QueryInterface** enables one object to determine whether another object supports a particular interface.</span></span> <span data-ttu-id="9028e-108">Con **QueryInterface**, pueden interactuar dos objetos sin conocimiento previo de la funcionalidad del otro.</span><span class="sxs-lookup"><span data-stu-id="9028e-108">With **QueryInterface**, two objects with no prior knowledge of each other's functionality can interact.</span></span> <span data-ttu-id="9028e-109">Si el objeto que implementa **QueryInterface** es compatible con la interfaz en cuestión, devuelve un puntero a la implementación de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="9028e-109">If the object that implements **QueryInterface** does support the interface in question, it returns a pointer to the implementation of the interface.</span></span> <span data-ttu-id="9028e-110">Si el objeto no admite la interfaz solicitada, devuelve el valor MAPI_E_INTERFACE_NOT_SUPPORTED.</span><span class="sxs-lookup"><span data-stu-id="9028e-110">If the object does not support the requested interface, it returns the MAPI_E_INTERFACE_NOT_SUPPORTED value.</span></span> 
  
<span data-ttu-id="9028e-111">Cuando **QueryInterface** devuelve un puntero de interfaz solicitada, también debe aumentar el recuento de referencia del nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="9028e-111">When **QueryInterface** returns a requested interface pointer, it must also increase the new object's reference count.</span></span> <span data-ttu-id="9028e-112">Recuento de referencia de un objeto es un valor numérico que se usa para administrar el ciclo de vida del objeto.</span><span class="sxs-lookup"><span data-stu-id="9028e-112">An object's reference count is a numeric value used to manage the object's lifespan.</span></span> <span data-ttu-id="9028e-113">Cuando el recuento de referencia es mayor que 1, la memoria del objeto no se puede liberar porque se usa activamente.</span><span class="sxs-lookup"><span data-stu-id="9028e-113">When the reference count is greater than 1, the object's memory cannot be freed because it is actively being used.</span></span> <span data-ttu-id="9028e-114">Es solo cuando el recuento de referencia cae a 0 que el objeto puede liberarse de forma segura.</span><span class="sxs-lookup"><span data-stu-id="9028e-114">It is only when the reference count drops to 0 that the object can be released safely.</span></span> 
  
<span data-ttu-id="9028e-115">Los otros dos métodos **IUnknown** , **AddRef** y **Release**, administran el recuento de referencia.</span><span class="sxs-lookup"><span data-stu-id="9028e-115">The other two **IUnknown** methods, **AddRef** and **Release**, manage the reference count.</span></span> <span data-ttu-id="9028e-116">**AddRef** se incrementa el recuento de referencia, mientras se disminuye **versión** lo.</span><span class="sxs-lookup"><span data-stu-id="9028e-116">**AddRef** increments the reference count, while **Release** decrements it.</span></span> <span data-ttu-id="9028e-117">Todos los métodos o funciones de la API que devuelven punteros a la interfaz, como **QueryInterface**, deben llamar a **AddRef** para incrementar el recuento de referencia.</span><span class="sxs-lookup"><span data-stu-id="9028e-117">All methods or API functions that return interface pointers, such as **QueryInterface**, must call **AddRef** to increment the reference count.</span></span> <span data-ttu-id="9028e-118">Todas las implementaciones de los métodos que reciben punteros a la interfaz deben llamar a **Release** para disminuir el recuento cuando el puntero ya no es necesario.</span><span class="sxs-lookup"><span data-stu-id="9028e-118">All implementations of methods that receive interface pointers must call **Release** to decrement the count when the pointer is no longer needed.</span></span> <span data-ttu-id="9028e-119">**Versión** se comprueba para un recuento de referencia existente, liberar la memoria asociada con la interfaz sólo si el recuento es 0.</span><span class="sxs-lookup"><span data-stu-id="9028e-119">**Release** checks for an existing reference count, freeing the memory associated with the interface only if the count is 0.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9028e-120">Debido a que no están necesario **AddRef** y **Release** para devolver valores precisos, los autores de llamadas de estos métodos no deben utilizar los valores devueltos para determinar si un objeto todavía es válido o se destruye.</span><span class="sxs-lookup"><span data-stu-id="9028e-120">Because **AddRef** and **Release** are not required to return accurate values, callers of these methods must not use the return values to determine whether an object is still valid or has been destroyed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9028e-121">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="9028e-121">See also</span></span>



[<span data-ttu-id="9028e-122">Implementar objetos MAPI</span><span class="sxs-lookup"><span data-stu-id="9028e-122">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

