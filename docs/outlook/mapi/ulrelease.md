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
ms.openlocfilehash: 46c37dbcf1aa3b0469281b8db99f210bda0918be
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582304"
---
# <a name="ulrelease"></a><span data-ttu-id="b21d5-103">UlRelease</span><span class="sxs-lookup"><span data-stu-id="b21d5-103">UlRelease</span></span>

  
  
<span data-ttu-id="b21d5-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b21d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b21d5-105">Proporciona una manera alternativa para invocar el método OLE **IUnknown:: Release**.</span><span class="sxs-lookup"><span data-stu-id="b21d5-105">Provides an alternative way to invoke the OLE method **IUnknown::Release**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b21d5-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="b21d5-106">Header file:</span></span>  <br/> |<span data-ttu-id="b21d5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b21d5-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b21d5-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="b21d5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b21d5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b21d5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b21d5-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="b21d5-110">Called by:</span></span>  <br/> |<span data-ttu-id="b21d5-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="b21d5-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="b21d5-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b21d5-112">Parameters</span></span>

 <span data-ttu-id="b21d5-113">_pUnk_</span><span class="sxs-lookup"><span data-stu-id="b21d5-113">_punk_</span></span>
  
> <span data-ttu-id="b21d5-114">[entrada] Puntero a una interfaz derivada de la interfaz **IUnknown** , en otras palabras cualquier interfaz MAPI.</span><span class="sxs-lookup"><span data-stu-id="b21d5-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b21d5-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b21d5-115">Return value</span></span>

<span data-ttu-id="b21d5-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="b21d5-116">S_OK</span></span> 
  
> <span data-ttu-id="b21d5-117">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="b21d5-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="b21d5-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="b21d5-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="b21d5-119">Un error de origen desconocido o inesperado no puede completar la operación.</span><span class="sxs-lookup"><span data-stu-id="b21d5-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b21d5-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b21d5-120">Remarks</span></span>

<span data-ttu-id="b21d5-121">El recuento de referencia es el número de punteros existentes para el objeto que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="b21d5-121">The reference count is the number of existing pointers to the object to be released.</span></span> 
  
<span data-ttu-id="b21d5-122">Si el parámetro _punk_ es NULL, la función devuelve inmediatamente sin llamar a **IUnknown:: Release**</span><span class="sxs-lookup"><span data-stu-id="b21d5-122">If the  _punk_ parameter is NULL, the function returns immediately without calling **IUnknown::Release**</span></span>
  
 <span data-ttu-id="b21d5-123">**UlRelease** devuelve el valor devuelto por el método **IUnknown:: Release** , que puede ser igual que el recuento de referencia para el objeto que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="b21d5-123">**UlRelease** returns the value returned by the **IUnknown::Release** method, which can be equal to the reference count for the object to be released.</span></span> 
  
<span data-ttu-id="b21d5-124">Para obtener más información acerca de **IUnknown:: Release**, vea [implementación de la interfaz IUnknown](implementing-the-iunknown-interface.md).</span><span class="sxs-lookup"><span data-stu-id="b21d5-124">For more information about **IUnknown::Release**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

