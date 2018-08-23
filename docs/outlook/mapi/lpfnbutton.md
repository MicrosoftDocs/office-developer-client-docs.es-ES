---
title: LPFNBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LPFNBUTTON
api_type:
- COM
ms.assetid: cb91ae1d-1ea8-4f02-a1f1-f2a356a71477
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3b302de68f27e85c67430f82bd3e2c33009600e9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591355"
---
# <a name="lpfnbutton"></a><span data-ttu-id="6fa4f-103">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="6fa4f-103">LPFNBUTTON</span></span>

  
  
<span data-ttu-id="6fa4f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6fa4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6fa4f-105">Define una función de devolución de llamada que llama MAPI para activar un control de botón opcional en un cuadro de diálogo de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="6fa4f-105">Defines a callback function that MAPI calls to activate an optional button control in an address book dialog box.</span></span> <span data-ttu-id="6fa4f-106">Normalmente, este botón es un botón de **Detalles** .</span><span class="sxs-lookup"><span data-stu-id="6fa4f-106">This button is typically a **Details** button.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6fa4f-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="6fa4f-107">Header file:</span></span>  <br/> |<span data-ttu-id="6fa4f-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6fa4f-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6fa4f-109">Función definido implementada por:</span><span class="sxs-lookup"><span data-stu-id="6fa4f-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="6fa4f-110">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="6fa4f-110">Service providers</span></span>  <br/> |
|<span data-ttu-id="6fa4f-111">Llamado por una función definida:</span><span class="sxs-lookup"><span data-stu-id="6fa4f-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="6fa4f-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="6fa4f-112">MAPI</span></span>  <br/> |
   
```cpp
SCODE (STDMETHODCALLTYPE FAR * LPFNBUTTON)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext,
  ULONG cbEntryID,
  LPENTRYID lpSelection,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="6fa4f-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6fa4f-113">Parameters</span></span>

 <span data-ttu-id="6fa4f-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6fa4f-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="6fa4f-115">[entrada] Controlador de las ventanas de primario para todos los cuadros de diálogo o windows que muestra esta función.</span><span class="sxs-lookup"><span data-stu-id="6fa4f-115">[in] Handle of the parent windows for any dialog boxes or windows this function displays.</span></span>
    
 <span data-ttu-id="6fa4f-116">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="6fa4f-116">_lpvContext_</span></span>
  
> <span data-ttu-id="6fa4f-117">[entrada] Puntero a un valor arbitrario se pasa a la función de devolución de llamada cuando llama a MAPI.</span><span class="sxs-lookup"><span data-stu-id="6fa4f-117">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="6fa4f-118">Este valor puede representar una dirección de importancia a la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="6fa4f-118">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="6fa4f-119">Normalmente, para el código de C++, _lpvContext_ representa un puntero a un objeto de C++.</span><span class="sxs-lookup"><span data-stu-id="6fa4f-119">Typically, for C++ code,  _lpvContext_ represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="6fa4f-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="6fa4f-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="6fa4f-121">[entrada] Tamaño, en bytes, del identificador de entrada que señala el parámetro _lpSelection_ .</span><span class="sxs-lookup"><span data-stu-id="6fa4f-121">[in] Size, in bytes, of the entry identifier pointed to by the  _lpSelection_ parameter.</span></span> 
    
 <span data-ttu-id="6fa4f-122">_lpSelection_</span><span class="sxs-lookup"><span data-stu-id="6fa4f-122">_lpSelection_</span></span>
  
> <span data-ttu-id="6fa4f-123">[entrada] Puntero a la definición de la selección en el cuadro de diálogo de identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="6fa4f-123">[in] Pointer to the entry identifier defining the selection in the dialog box.</span></span>
    
 <span data-ttu-id="6fa4f-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6fa4f-124">_ulFlags_</span></span>
  
> <span data-ttu-id="6fa4f-125">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="6fa4f-125">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6fa4f-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6fa4f-126">Return value</span></span>

<span data-ttu-id="6fa4f-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="6fa4f-127">S_OK</span></span> 
  
> <span data-ttu-id="6fa4f-128">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="6fa4f-128">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6fa4f-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6fa4f-129">Remarks</span></span>

<span data-ttu-id="6fa4f-130">Las aplicaciones cliente de llamar a una función de devolución de llamada según el prototipo **LPFNBUTTON** para definir un botón en un cuadro de diálogo detalles.</span><span class="sxs-lookup"><span data-stu-id="6fa4f-130">Client applications call a callback function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="6fa4f-131">El cliente pasa un puntero a la función de devolución de llamada en las llamadas al método [IAddrBook::Details](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="6fa4f-131">The client passes a pointer to the callback function in calls to the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="6fa4f-132">Proveedores de servicios de llamar a una función de enlace según el prototipo **LPFNBUTTON** para definir un botón en un cuadro de diálogo detalles.</span><span class="sxs-lookup"><span data-stu-id="6fa4f-132">Service providers call a hook function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="6fa4f-133">El proveedor pasa un puntero a esta función de enlace en las llamadas al método [IMAPISupport::Details](imapisupport-details.md) .</span><span class="sxs-lookup"><span data-stu-id="6fa4f-133">The provider passes a pointer to this hook function in calls to the [IMAPISupport::Details](imapisupport-details.md) method.</span></span> 
  
<span data-ttu-id="6fa4f-134">En ambos casos, cuando se muestra el cuadro de diálogo y el usuario elige el botón definido, MAPI llama **LPFNBUTTON**.</span><span class="sxs-lookup"><span data-stu-id="6fa4f-134">In both cases, when the dialog box is displayed and the user chooses the defined button, MAPI calls **LPFNBUTTON**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6fa4f-135">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="6fa4f-135">See also</span></span>



[<span data-ttu-id="6fa4f-136">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="6fa4f-136">BuildDisplayTable</span></span>](builddisplaytable.md)

