---
title: IProfAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetLastError
api_type:
- COM
ms.assetid: bb161d7b-ae5b-4f8e-a506-8346ac5e583d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b6964ecde3a78bd1e9ce0ae1dcab0342c5a21a03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430776"
---
# <a name="iprofadmingetlasterror"></a><span data-ttu-id="565e6-103">IProfAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="565e6-103">IProfAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="565e6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="565e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="565e6-105">Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produjo en un objeto de administración de perfiles.</span><span class="sxs-lookup"><span data-stu-id="565e6-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="565e6-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="565e6-106">Parameters</span></span>

 <span data-ttu-id="565e6-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="565e6-107">_hResult_</span></span>
  
> <span data-ttu-id="565e6-108">[in] Tipo de datos HRESULT que contiene el valor de error generado en la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="565e6-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="565e6-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="565e6-109">_ulFlags_</span></span>
  
> <span data-ttu-id="565e6-110">[in] Máscara de bits de marcas que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="565e6-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="565e6-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="565e6-111">The following flag can be set:</span></span>
    
<span data-ttu-id="565e6-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="565e6-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="565e6-113">Las cadenas de la [estructura MAPIERROR](mapierror.md) devueltas en el parámetro  _lppMAPIError_ están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="565e6-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="565e6-114">Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="565e6-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="565e6-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="565e6-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="565e6-116">[salida] Puntero a un puntero a la estructura **MAPIERROR** que contiene información de versión, componente y contexto del error.</span><span class="sxs-lookup"><span data-stu-id="565e6-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="565e6-117">El  _parámetro lppMAPIError_ se puede establecer en NULL si no hay ninguna **estructura MAPIERROR** que devolver.</span><span class="sxs-lookup"><span data-stu-id="565e6-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="565e6-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="565e6-118">Return value</span></span>

<span data-ttu-id="565e6-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="565e6-119">S_OK</span></span> 
  
> <span data-ttu-id="565e6-120">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="565e6-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="565e6-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="565e6-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="565e6-122">La marca MAPI_UNICODE se estableció y la implementación no admite Unicode, o MAPI_UNICODE no se estableció y la implementación solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="565e6-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="565e6-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="565e6-123">Remarks</span></span>

<span data-ttu-id="565e6-124">El **método IProfAdmin::GetLastError** recupera información sobre el último error devuelto de una llamada de método para el objeto de administración de perfiles.</span><span class="sxs-lookup"><span data-stu-id="565e6-124">The **IProfAdmin::GetLastError** method retrieves information about the last error returned from a method call for the profile administration object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="565e6-125">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="565e6-125">Notes to callers</span></span>

<span data-ttu-id="565e6-126">Puede usar la estructura **MAPIERROR,** si MAPI proporciona una, apuntada por el parámetro  _lppMAPIError_ solo si **GetLastError** devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="565e6-126">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="565e6-127">A veces MAPI no puede determinar cuál fue el último error o no tiene nada más que informar sobre el error.</span><span class="sxs-lookup"><span data-stu-id="565e6-127">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="565e6-128">En esta situación, se devuelve un puntero a NULL en  _lppMAPIError_.</span><span class="sxs-lookup"><span data-stu-id="565e6-128">In this situation, a pointer to NULL is returned in  _lppMAPIError_.</span></span> 
  
<span data-ttu-id="565e6-129">Para liberar toda la memoria asignada por MAPI para la estructura **MAPIERROR,** llame a la [función MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="565e6-129">To release all the memory allocated by MAPI for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="565e6-130">Para obtener más información sobre el **método GetLastError,** vea [Using Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="565e6-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="565e6-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="565e6-131">See also</span></span>



[<span data-ttu-id="565e6-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="565e6-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="565e6-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="565e6-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="565e6-134">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="565e6-134">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

