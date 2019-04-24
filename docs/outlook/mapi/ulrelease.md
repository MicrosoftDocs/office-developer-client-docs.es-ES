---
title: UlRelease
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlRelease
api_type:
- COM
ms.assetid: 95db96ef-f95f-41da-b216-f717c23bffd2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 288e34a159db48b1344524b87f02b045259f1565
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315298"
---
# <a name="ulrelease"></a><span data-ttu-id="b828e-103">UlRelease</span><span class="sxs-lookup"><span data-stu-id="b828e-103">UlRelease</span></span>

  
  
<span data-ttu-id="b828e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b828e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b828e-105">Proporciona una forma alternativa para invocar el método OLE **IUnknown:: Release**.</span><span class="sxs-lookup"><span data-stu-id="b828e-105">Provides an alternative way to invoke the OLE method **IUnknown::Release**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b828e-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="b828e-106">Header file:</span></span>  <br/> |<span data-ttu-id="b828e-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b828e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b828e-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="b828e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b828e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b828e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b828e-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="b828e-110">Called by:</span></span>  <br/> |<span data-ttu-id="b828e-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="b828e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="b828e-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="b828e-112">Parameters</span></span>

 <span data-ttu-id="b828e-113">_punk_</span><span class="sxs-lookup"><span data-stu-id="b828e-113">_punk_</span></span>
  
> <span data-ttu-id="b828e-114">a Puntero a una interfaz derivada de la interfaz **IUnknown** , en otras palabras, cualquier interfaz MAPI.</span><span class="sxs-lookup"><span data-stu-id="b828e-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b828e-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b828e-115">Return value</span></span>

<span data-ttu-id="b828e-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="b828e-116">S_OK</span></span> 
  
> <span data-ttu-id="b828e-117">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="b828e-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="b828e-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="b828e-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="b828e-119">Un error de origen inesperado o desconocido impidió que se completara la operación.</span><span class="sxs-lookup"><span data-stu-id="b828e-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b828e-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b828e-120">Remarks</span></span>

<span data-ttu-id="b828e-121">El recuento de referencia es el número de punteros existentes en el objeto que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="b828e-121">The reference count is the number of existing pointers to the object to be released.</span></span> 
  
<span data-ttu-id="b828e-122">Si el parámetro _punk_ es null, la función regresa inmediatamente sin llamar a **IUnknown:: Release**</span><span class="sxs-lookup"><span data-stu-id="b828e-122">If the  _punk_ parameter is NULL, the function returns immediately without calling **IUnknown::Release**</span></span>
  
 <span data-ttu-id="b828e-123">**UlRelease** devuelve el valor devuelto por el método **IUnknown:: Release** , que puede ser igual que el recuento de referencias para el objeto que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="b828e-123">**UlRelease** returns the value returned by the **IUnknown::Release** method, which can be equal to the reference count for the object to be released.</span></span> 
  
<span data-ttu-id="b828e-124">Para obtener más información acerca de **IUnknown:: Release**, vea [implementar la interfaz IUnknown](implementing-the-iunknown-interface.md).</span><span class="sxs-lookup"><span data-stu-id="b828e-124">For more information about **IUnknown::Release**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

