---
title: IMAPIControlGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetLastError
api_type:
- COM
ms.assetid: 83290b8e-fffc-41c8-a01e-578d130b65c5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 10ac4e33b3f734ec2ce3205aa1897e0418cb563d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421154"
---
# <a name="imapicontrolgetlasterror"></a><span data-ttu-id="54ca5-103">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="54ca5-103">IMAPIControl::GetLastError</span></span>

  
  
<span data-ttu-id="54ca5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54ca5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54ca5-105">Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error de control de botón anterior.</span><span class="sxs-lookup"><span data-stu-id="54ca5-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="54ca5-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="54ca5-106">Parameters</span></span>

 <span data-ttu-id="54ca5-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="54ca5-107">_hResult_</span></span>
  
> <span data-ttu-id="54ca5-108">[in] Identificador del valor de error generado en la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="54ca5-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="54ca5-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="54ca5-109">_ulFlags_</span></span>
  
> <span data-ttu-id="54ca5-110">[in] Máscara de bits de marcas que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="54ca5-110">[in] A bitmask of flags that controls the type of the strings returned.</span></span> <span data-ttu-id="54ca5-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="54ca5-111">The following flag can be set:</span></span>
    
<span data-ttu-id="54ca5-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="54ca5-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="54ca5-113">Las cadenas de la **estructura MAPIERROR** devueltas en el parámetro  _lppMAPIError_ están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="54ca5-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="54ca5-114">Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="54ca5-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="54ca5-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="54ca5-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="54ca5-116">[salida] Puntero a un puntero a una **estructura MAPIERROR** que contiene información de versión, componente y contexto del error.</span><span class="sxs-lookup"><span data-stu-id="54ca5-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="54ca5-117">El  _parámetro lppMAPIError_ se puede establecer en NULL si el proveedor no puede proporcionar una **estructura MAPIERROR** con la información adecuada.</span><span class="sxs-lookup"><span data-stu-id="54ca5-117">The  _lppMAPIError_ parameter can be set to NULL if the provider cannot supply a **MAPIERROR** structure with appropriate information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="54ca5-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54ca5-118">Return value</span></span>

<span data-ttu-id="54ca5-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="54ca5-119">S_OK</span></span> 
  
> <span data-ttu-id="54ca5-120">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="54ca5-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="54ca5-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="54ca5-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="54ca5-122">La marca MAPI_UNICODE se estableció y la implementación no admite Unicode, o MAPI_UNICODE no se estableció y la implementación solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="54ca5-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="54ca5-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="54ca5-123">Remarks</span></span>

<span data-ttu-id="54ca5-124">Los proveedores de servicios implementan **el método IMAPIControl::GetLastError** para proporcionar información sobre una llamada al método anterior que no se pudo realizar.</span><span class="sxs-lookup"><span data-stu-id="54ca5-124">Service providers implement the **IMAPIControl::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="54ca5-125">MAPI puede proporcionar a los usuarios información detallada sobre el error mostrando los datos de la estructura **MAPIERROR** en un mensaje o cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="54ca5-125">MAPI can give users detailed information about the error by displaying the data from the **MAPIERROR** structure in a message or dialog box.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="54ca5-126">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="54ca5-126">Notes to implementers</span></span>

<span data-ttu-id="54ca5-127">No es necesario tener información para incluir en la estructura **MAPIERROR** para cada error.</span><span class="sxs-lookup"><span data-stu-id="54ca5-127">You do not need to have information to include in the **MAPIERROR** structure for every error.</span></span> <span data-ttu-id="54ca5-128">Es posible que no sea posible determinar cuál fue el error anterior.</span><span class="sxs-lookup"><span data-stu-id="54ca5-128">It may not be possible to determine what the previous error was.</span></span> <span data-ttu-id="54ca5-129">Si tiene información, devuelva S_OK y los datos adecuados en la **estructura MAPIERROR.**</span><span class="sxs-lookup"><span data-stu-id="54ca5-129">If you have information, return S_OK and the appropriate data in the **MAPIERROR** structure.</span></span> <span data-ttu-id="54ca5-130">Si no hay información disponible, devuelve S_OK y un puntero a NULL para el parámetro _lppMAPIError._</span><span class="sxs-lookup"><span data-stu-id="54ca5-130">If no information is available, return S_OK and a pointer to NULL for the  _lppMAPIError_ parameter.</span></span> 
  
<span data-ttu-id="54ca5-131">Para obtener más información acerca **del método GetLastError,** vea [Mapi Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="54ca5-131">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="54ca5-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="54ca5-132">See also</span></span>



[<span data-ttu-id="54ca5-133">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="54ca5-133">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="54ca5-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="54ca5-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="54ca5-135">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="54ca5-135">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

