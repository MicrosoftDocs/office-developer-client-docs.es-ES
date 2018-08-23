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
ms.openlocfilehash: 65bf7debcae1367ccad9e109242fd4a72839a94e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584929"
---
# <a name="iprofadmingetlasterror"></a><span data-ttu-id="d5f93-103">IProfAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d5f93-103">IProfAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="d5f93-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5f93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5f93-105">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produjeron en un objeto de administración de perfiles.</span><span class="sxs-lookup"><span data-stu-id="d5f93-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="d5f93-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5f93-106">Parameters</span></span>

 <span data-ttu-id="d5f93-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="d5f93-107">_hResult_</span></span>
  
> <span data-ttu-id="d5f93-108">[entrada] Un tipo de datos HRESULT que contiene el valor de error generado en la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="d5f93-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="d5f93-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d5f93-109">_ulFlags_</span></span>
  
> <span data-ttu-id="d5f93-110">[entrada] Una máscara de bits de indicadores que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="d5f93-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="d5f93-111">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="d5f93-111">The following flag can be set:</span></span>
    
<span data-ttu-id="d5f93-112">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="d5f93-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d5f93-113">Las cadenas en la estructura [MAPIERROR](mapierror.md) devuelta en el parámetro _lppMAPIError_ están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="d5f93-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="d5f93-114">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="d5f93-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="d5f93-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="d5f93-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="d5f93-116">[out] Un puntero a un puntero a la estructura **MAPIERROR** que contiene información de versión, el componente y el contexto para el error.</span><span class="sxs-lookup"><span data-stu-id="d5f93-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="d5f93-117">El parámetro _lppMAPIError_ se puede establecer en NULL si no hay ninguna estructura **MAPIERROR** para devolver.</span><span class="sxs-lookup"><span data-stu-id="d5f93-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d5f93-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5f93-118">Return value</span></span>

<span data-ttu-id="d5f93-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="d5f93-119">S_OK</span></span> 
  
> <span data-ttu-id="d5f93-120">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="d5f93-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="d5f93-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="d5f93-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="d5f93-122">Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="d5f93-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d5f93-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d5f93-123">Remarks</span></span>

<span data-ttu-id="d5f93-124">El método **IProfAdmin::GetLastError** recupera información sobre el último error devuelto desde una llamada al método para el objeto de administración de perfiles.</span><span class="sxs-lookup"><span data-stu-id="d5f93-124">The **IProfAdmin::GetLastError** method retrieves information about the last error returned from a method call for the profile administration object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d5f93-125">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="d5f93-125">Notes to callers</span></span>

<span data-ttu-id="d5f93-126">Puede usar la estructura **MAPIERROR** , si MAPI proporciona uno, indicada por el sólo de si de parámetro _lppMAPIError_ **GetLastError** devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="d5f93-126">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="d5f93-127">En ocasiones, MAPI no puede determinar qué era el último error o no tiene nada más para informar sobre el error.</span><span class="sxs-lookup"><span data-stu-id="d5f93-127">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="d5f93-128">En esta situación, se devuelve un puntero a NULL en _lppMAPIError_.</span><span class="sxs-lookup"><span data-stu-id="d5f93-128">In this situation, a pointer to NULL is returned in  _lppMAPIError_.</span></span> 
  
<span data-ttu-id="d5f93-129">Para liberar toda la memoria asignada por MAPI para la estructura **MAPIERROR** , llame a la función [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="d5f93-129">To release all the memory allocated by MAPI for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="d5f93-130">Para obtener más información acerca del método **GetLastError** , vea [Uso de errores extendido](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="d5f93-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d5f93-131">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="d5f93-131">See also</span></span>



[<span data-ttu-id="d5f93-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="d5f93-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="d5f93-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d5f93-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="d5f93-134">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d5f93-134">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

