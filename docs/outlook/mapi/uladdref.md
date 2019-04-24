---
title: UlAddRef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlAddRef
api_type:
- COM
ms.assetid: 9b897cbc-90b2-4c60-b5f1-dc78e7e7952d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f9e55153830dbe41a2b4a48454157c900d96cf90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315375"
---
# <a name="uladdref"></a><span data-ttu-id="4b88d-103">UlAddRef</span><span class="sxs-lookup"><span data-stu-id="4b88d-103">UlAddRef</span></span>

  
  
<span data-ttu-id="4b88d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b88d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b88d-105">Proporciona una forma alternativa para invocar al método OLE **IUnknown:: AddRef**.</span><span class="sxs-lookup"><span data-stu-id="4b88d-105">Provides an alternative way to invoke the OLE method **IUnknown::AddRef**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4b88d-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="4b88d-106">Header file:</span></span>  <br/> |<span data-ttu-id="4b88d-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4b88d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4b88d-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="4b88d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4b88d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4b88d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4b88d-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="4b88d-110">Called by:</span></span>  <br/> |<span data-ttu-id="4b88d-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="4b88d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="4b88d-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="4b88d-112">Parameters</span></span>

 <span data-ttu-id="4b88d-113">_punk_</span><span class="sxs-lookup"><span data-stu-id="4b88d-113">_punk_</span></span>
  
> <span data-ttu-id="4b88d-114">a Puntero a una interfaz derivada de la interfaz **IUnknown** , en otras palabras, cualquier interfaz MAPI.</span><span class="sxs-lookup"><span data-stu-id="4b88d-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4b88d-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b88d-115">Return value</span></span>

<span data-ttu-id="4b88d-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="4b88d-116">S_OK</span></span> 
  
> <span data-ttu-id="4b88d-117">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="4b88d-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="4b88d-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="4b88d-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="4b88d-119">Un error de origen inesperado o desconocido impidió que se completara la operación.</span><span class="sxs-lookup"><span data-stu-id="4b88d-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4b88d-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4b88d-120">Remarks</span></span>

 <span data-ttu-id="4b88d-121">**UlAddRef** devuelve el valor devuelto por el método **IUnknown:: AddRef** , que es el nuevo valor del recuento de referencias para la interfaz.</span><span class="sxs-lookup"><span data-stu-id="4b88d-121">**UlAddRef** returns the value returned by the **IUnknown::AddRef** method, which is the new value of the reference count for the interface.</span></span> <span data-ttu-id="4b88d-122">El valor es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="4b88d-122">The value is nonzero.</span></span> 
  
<span data-ttu-id="4b88d-123">Para obtener más información acerca de **IUnknown:: AddRef**, vea [implementar la interfaz IUnknown](implementing-the-iunknown-interface.md).</span><span class="sxs-lookup"><span data-stu-id="4b88d-123">For more information about **IUnknown::AddRef**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

