---
title: Implementación de objetos en C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 24fc4d78-726d-40ff-bad2-25dc298bd51a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d07d756abded137d3268daf7dd0998f0c953cb1d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563950"
---
# <a name="implementing-objects-in-c"></a><span data-ttu-id="4f329-103">Implementación de objetos en C</span><span class="sxs-lookup"><span data-stu-id="4f329-103">Implementing objects in C</span></span>

<span data-ttu-id="4f329-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f329-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f329-105">Las aplicaciones cliente y proveedores de servicios de escrito en C definición objetos MAPI mediante la creación de una estructura de datos y una matriz de punteros a función ordenada conocido como una tabla de función virtual o vtable.</span><span class="sxs-lookup"><span data-stu-id="4f329-105">Client applications and service providers written in C define MAPI objects by creating a data structure and an array of ordered function pointers known as a virtual function table, or vtable.</span></span> <span data-ttu-id="4f329-106">Un puntero a la tabla vtable debe ser el primer miembro de la estructura de datos.</span><span class="sxs-lookup"><span data-stu-id="4f329-106">A pointer to the vtable must be the first member of the data structure.</span></span>
  
<span data-ttu-id="4f329-107">En la tabla vtable propio, hay un puntero por cada método en cada interfaz admitido por el objeto.</span><span class="sxs-lookup"><span data-stu-id="4f329-107">In the vtable itself, there is one pointer for every method in each interface supported by the object.</span></span> <span data-ttu-id="4f329-108">El orden de los punteros debe seguir el orden de los métodos en la especificación de la interfaz publicado en el archivo de encabezado Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="4f329-108">The order of the pointers must follow the order of the methods in the interface specification published in the Mapidefs.h header file.</span></span> <span data-ttu-id="4f329-109">Cada puntero de función en la tabla vtable se establece en la dirección de la implementación del método real.</span><span class="sxs-lookup"><span data-stu-id="4f329-109">Each function pointer in the vtable is set to the address of the actual implementation of the method.</span></span> <span data-ttu-id="4f329-110">En C++, el compilador establece automáticamente la tabla vtable.</span><span class="sxs-lookup"><span data-stu-id="4f329-110">In C++, the compiler automatically sets up the vtable.</span></span> <span data-ttu-id="4f329-111">En C, no lo hace.</span><span class="sxs-lookup"><span data-stu-id="4f329-111">In C, it does not.</span></span> 
  
<span data-ttu-id="4f329-112">En la siguiente ilustración se muestra cómo funciona esto.</span><span class="sxs-lookup"><span data-stu-id="4f329-112">The following illustration shows how this works.</span></span> <span data-ttu-id="4f329-113">El cuadro en el extremo izquierdo representa a un cliente que necesita utilizar un objeto de proveedor de servicio.</span><span class="sxs-lookup"><span data-stu-id="4f329-113">The box on the far left represents a client that needs to use a service provider object.</span></span> <span data-ttu-id="4f329-114">A través de la sesión, el cliente obtiene un puntero al objeto, **lpObject**.</span><span class="sxs-lookup"><span data-stu-id="4f329-114">Through the session, the client obtains a pointer to the object, **lpObject**.</span></span> <span data-ttu-id="4f329-115">La tabla vtable aparece en primer lugar en el objeto seguido por métodos y datos privados.</span><span class="sxs-lookup"><span data-stu-id="4f329-115">The vtable appears first in the object followed by private data and methods.</span></span> <span data-ttu-id="4f329-116">El puntero vtable apunta a la tabla vtable real, que contiene punteros a cada una de las implementaciones de los métodos de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="4f329-116">The vtable pointer points to the actual vtable, which contains pointers to each of the implementations of the methods in the interface.</span></span> 
  
<span data-ttu-id="4f329-117">**Implementación de objeto**</span><span class="sxs-lookup"><span data-stu-id="4f329-117">**Object implementation**</span></span>
  
<span data-ttu-id="4f329-118">![Implementación de objeto] (media/amapi_42.gif "Implementación de objeto")</span><span class="sxs-lookup"><span data-stu-id="4f329-118">![Object implementation](media/amapi_42.gif "Object implementation")</span></span>
  
<span data-ttu-id="4f329-119">En el ejemplo de código siguiente se muestra cómo un proveedor de servicios de C puede definir un objeto de estado simple.</span><span class="sxs-lookup"><span data-stu-id="4f329-119">The following code example shows how a C service provider can define a simple status object.</span></span> <span data-ttu-id="4f329-120">El primer miembro es el puntero vtable; el resto del objeto se compone de miembros de datos.</span><span class="sxs-lookup"><span data-stu-id="4f329-120">The first member is the vtable pointer; the rest of the object is made up of data members.</span></span> 
  
```C
typedef struct _MYSTATUSOBJECT
{
    const STATUS_Vtbl FAR *lpVtbl;
    ULONG              cRef;
    ANOTHEROBJ        *pObj;
    LPMAPIPROP         lpProp;
    LPFREEBUFFER       lpFreeBuf;
} MYSTATUSOBJECT, *LPMYSTATUSOBJ;
 
```

<span data-ttu-id="4f329-121">Debido a que este objeto es un objeto de estado, el vtable incluye punteros a las implementaciones de cada uno de los métodos en el [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interfaz, así como punteros a las implementaciones de cada uno de los métodos de las interfaces base: **IUnknown **y **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="4f329-121">Because this object is a status object, the vtable includes pointers to implementations of each of the methods in the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, as well as pointers to implementations of each of the methods in the base interfaces — **IUnknown** and **IMAPIProp**.</span></span> <span data-ttu-id="4f329-122">El orden de los métodos en la tabla vtable coincide con el orden especificado, tal como se define en el archivo de encabezado Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="4f329-122">The order of methods in the vtable matches the specified order as defined in the Mapidefs.h header file.</span></span>
  
```js
static const MYOBJECT_Vtbl vtblSTATUS =
{
    STATUS_QueryInterface,
    STATUS_AddRef,
    STATUS_Release,
    STATUS_GetLastError,
    STATUS_SaveChanges,
    STATUS_GetProps,
    STATUS_GetPropList,
    STATUS_OpenProperty,
    STATUS_SetProps,
    STATUS_DeleteProps,
    STATUS_CopyTo,
    STATUS_CopyProps,
    STATUS_GetNamesFromIDs,
    STATUS_GetIDsFromNames,
    STATUS_ValidateState,
    STATUS_SettingsDialog,
    STATUS_ChangePassword,
    STATUS_FlushQueues
};
 
```

<span data-ttu-id="4f329-123">Los clientes y proveedores de servicios de escrito en C utilizan objetos indirectamente a través de la tabla vtable y agregar un puntero de objeto como el primer parámetro en cada llamada.</span><span class="sxs-lookup"><span data-stu-id="4f329-123">Clients and service providers written in C use objects indirectly through the vtable and add an object pointer as the first parameter in every call.</span></span> <span data-ttu-id="4f329-124">Todas las llamadas a un método de interfaz MAPI requiere un puntero al objeto que se llama como su primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="4f329-124">Every call to a MAPI interface method requires a pointer to the object being called as its first parameter.</span></span> <span data-ttu-id="4f329-125">C++ define un puntero especial conocido como el puntero **this** para este propósito.</span><span class="sxs-lookup"><span data-stu-id="4f329-125">C++ defines a special pointer known as the **this** pointer for this purpose.</span></span> <span data-ttu-id="4f329-126">El compilador de C++ agrega implícitamente el puntero **this** como el primer parámetro para cada llamada al método.</span><span class="sxs-lookup"><span data-stu-id="4f329-126">The C++ compiler implicitly adds the **this** pointer as the first parameter to every method call.</span></span> <span data-ttu-id="4f329-127">En C no hay ningún puntero con estas características; se debe agregarse explícitamente.</span><span class="sxs-lookup"><span data-stu-id="4f329-127">In C there is no such pointer; it must be explicitly added.</span></span> 
  
<span data-ttu-id="4f329-128">El código siguiente muestra cómo un cliente puede realizar una llamada a una instancia de MYSTATUSOBJECT:</span><span class="sxs-lookup"><span data-stu-id="4f329-128">The following code demonstrates how a client can make a call to an instance of MYSTATUSOBJECT:</span></span>
  
```C
lpMyObj->lpVtbl->ValidateState(lpMyObj, ulUIParam, ulFlags);
 
```

## <a name="see-also"></a><span data-ttu-id="4f329-129">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="4f329-129">See also</span></span>

- [<span data-ttu-id="4f329-130">Implementar objetos MAPI</span><span class="sxs-lookup"><span data-stu-id="4f329-130">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

