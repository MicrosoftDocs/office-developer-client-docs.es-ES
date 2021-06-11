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
ms.openlocfilehash: 804bd23a148b942fd4580d1e3465fc1f65ff5978
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431515"
---
# <a name="lpfnbutton"></a><span data-ttu-id="b6181-103">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="b6181-103">LPFNBUTTON</span></span>

  
  
<span data-ttu-id="b6181-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6181-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6181-105">Define una función de devolución de llamada que llama MAPI para activar un control de botón opcional en un cuadro de diálogo de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="b6181-105">Defines a callback function that MAPI calls to activate an optional button control in an address book dialog box.</span></span> <span data-ttu-id="b6181-106">Este botón suele ser un **botón Detalles.**</span><span class="sxs-lookup"><span data-stu-id="b6181-106">This button is typically a **Details** button.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b6181-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="b6181-107">Header file:</span></span>  <br/> |<span data-ttu-id="b6181-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b6181-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b6181-109">Función definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="b6181-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="b6181-110">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="b6181-110">Service providers</span></span>  <br/> |
|<span data-ttu-id="b6181-111">Función definida llamada por:</span><span class="sxs-lookup"><span data-stu-id="b6181-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="b6181-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="b6181-112">MAPI</span></span>  <br/> |
   
```cpp
SCODE (STDMETHODCALLTYPE FAR * LPFNBUTTON)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext,
  ULONG cbEntryID,
  LPENTRYID lpSelection,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b6181-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="b6181-113">Parameters</span></span>

 <span data-ttu-id="b6181-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b6181-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="b6181-115">[in] Identificador de las ventanas primarias de los cuadros de diálogo o ventanas que muestra esta función.</span><span class="sxs-lookup"><span data-stu-id="b6181-115">[in] Handle of the parent windows for any dialog boxes or windows this function displays.</span></span>
    
 <span data-ttu-id="b6181-116">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="b6181-116">_lpvContext_</span></span>
  
> <span data-ttu-id="b6181-117">[in] Puntero a un valor arbitrario pasado a la función de devolución de llamada cuando MAPI lo llama.</span><span class="sxs-lookup"><span data-stu-id="b6181-117">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="b6181-118">Este valor puede representar una dirección de importancia para la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="b6181-118">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="b6181-119">Normalmente, para el código C++,  _lpvContext_ representa un puntero a un objeto C++.</span><span class="sxs-lookup"><span data-stu-id="b6181-119">Typically, for C++ code,  _lpvContext_ represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="b6181-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b6181-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="b6181-121">[in] Tamaño, en bytes, del identificador de entrada señalado por el _parámetro lpSelection._</span><span class="sxs-lookup"><span data-stu-id="b6181-121">[in] Size, in bytes, of the entry identifier pointed to by the  _lpSelection_ parameter.</span></span> 
    
 <span data-ttu-id="b6181-122">_lpSelection_</span><span class="sxs-lookup"><span data-stu-id="b6181-122">_lpSelection_</span></span>
  
> <span data-ttu-id="b6181-123">[in] Puntero al identificador de entrada que define la selección en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b6181-123">[in] Pointer to the entry identifier defining the selection in the dialog box.</span></span>
    
 <span data-ttu-id="b6181-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b6181-124">_ulFlags_</span></span>
  
> <span data-ttu-id="b6181-125">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b6181-125">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b6181-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b6181-126">Return value</span></span>

<span data-ttu-id="b6181-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="b6181-127">S_OK</span></span> 
  
> <span data-ttu-id="b6181-128">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="b6181-128">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b6181-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b6181-129">Remarks</span></span>

<span data-ttu-id="b6181-130">Las aplicaciones cliente llaman a una función de devolución de llamada basada en el **prototipo LPFNBUTTON** para definir un botón en un cuadro de diálogo de detalles.</span><span class="sxs-lookup"><span data-stu-id="b6181-130">Client applications call a callback function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="b6181-131">El cliente pasa un puntero a la función de devolución de llamada en llamadas al método [IAddrBook::D etails.](iaddrbook-details.md)</span><span class="sxs-lookup"><span data-stu-id="b6181-131">The client passes a pointer to the callback function in calls to the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="b6181-132">Los proveedores de servicios llaman a una función de enlace basada en el **prototipo LPFNBUTTON** para definir un botón en un cuadro de diálogo de detalles.</span><span class="sxs-lookup"><span data-stu-id="b6181-132">Service providers call a hook function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="b6181-133">El proveedor pasa un puntero a esta función de enlace en llamadas al método [IMAPISupport::D etails.](imapisupport-details.md)</span><span class="sxs-lookup"><span data-stu-id="b6181-133">The provider passes a pointer to this hook function in calls to the [IMAPISupport::Details](imapisupport-details.md) method.</span></span> 
  
<span data-ttu-id="b6181-134">En ambos casos, cuando se muestra el cuadro de diálogo y el usuario elige el botón definido, MAPI llama **a LPFNBUTTON**.</span><span class="sxs-lookup"><span data-stu-id="b6181-134">In both cases, when the dialog box is displayed and the user chooses the defined button, MAPI calls **LPFNBUTTON**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b6181-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6181-135">See also</span></span>



[<span data-ttu-id="b6181-136">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="b6181-136">BuildDisplayTable</span></span>](builddisplaytable.md)

