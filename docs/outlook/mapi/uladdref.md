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
ms.openlocfilehash: baf45fa33ca085f51a6f9c20f72ec1fd1545ad79
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592377"
---
# <a name="uladdref"></a><span data-ttu-id="8c3ec-103">UlAddRef</span><span class="sxs-lookup"><span data-stu-id="8c3ec-103">UlAddRef</span></span>

  
  
<span data-ttu-id="8c3ec-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c3ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c3ec-105">Proporciona una manera alternativa para invocar el método OLE **IUnknown:: AddRef**.</span><span class="sxs-lookup"><span data-stu-id="8c3ec-105">Provides an alternative way to invoke the OLE method **IUnknown::AddRef**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8c3ec-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="8c3ec-106">Header file:</span></span>  <br/> |<span data-ttu-id="8c3ec-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8c3ec-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8c3ec-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="8c3ec-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8c3ec-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8c3ec-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8c3ec-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="8c3ec-110">Called by:</span></span>  <br/> |<span data-ttu-id="8c3ec-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="8c3ec-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="8c3ec-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c3ec-112">Parameters</span></span>

 <span data-ttu-id="8c3ec-113">_pUnk_</span><span class="sxs-lookup"><span data-stu-id="8c3ec-113">_punk_</span></span>
  
> <span data-ttu-id="8c3ec-114">[entrada] Puntero a una interfaz derivada de la interfaz **IUnknown** , en otras palabras cualquier interfaz MAPI.</span><span class="sxs-lookup"><span data-stu-id="8c3ec-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8c3ec-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c3ec-115">Return value</span></span>

<span data-ttu-id="8c3ec-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="8c3ec-116">S_OK</span></span> 
  
> <span data-ttu-id="8c3ec-117">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="8c3ec-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="8c3ec-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="8c3ec-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="8c3ec-119">Un error de origen desconocido o inesperado no puede completar la operación.</span><span class="sxs-lookup"><span data-stu-id="8c3ec-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8c3ec-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8c3ec-120">Remarks</span></span>

 <span data-ttu-id="8c3ec-121">**UlAddRef** devuelve el valor devuelto por el método **IUnknown:: AddRef** , que es el nuevo valor del recuento de referencias para la interfaz.</span><span class="sxs-lookup"><span data-stu-id="8c3ec-121">**UlAddRef** returns the value returned by the **IUnknown::AddRef** method, which is the new value of the reference count for the interface.</span></span> <span data-ttu-id="8c3ec-122">El valor es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="8c3ec-122">The value is nonzero.</span></span> 
  
<span data-ttu-id="8c3ec-123">Para obtener más información acerca de **IUnknown:: AddRef**, vea [implementación de la interfaz IUnknown](implementing-the-iunknown-interface.md).</span><span class="sxs-lookup"><span data-stu-id="8c3ec-123">For more information about **IUnknown::AddRef**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

