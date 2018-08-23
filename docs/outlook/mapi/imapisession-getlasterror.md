---
title: IMAPISessionGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetLastError
api_type:
- COM
ms.assetid: 38cb3692-a5f8-403a-9615-9bd5868af23c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 34de52693d8484abb28d2ee2f7b86f15e8bd037b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574107"
---
# <a name="imapisessiongetlasterror"></a><span data-ttu-id="0452e-103">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="0452e-103">IMAPISession::GetLastError</span></span>

  
  
<span data-ttu-id="0452e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0452e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0452e-105">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error de la sesión anterior.</span><span class="sxs-lookup"><span data-stu-id="0452e-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="0452e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0452e-106">Parameters</span></span>

 <span data-ttu-id="0452e-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="0452e-107">_hResult_</span></span>
  
> <span data-ttu-id="0452e-108">[entrada] Un identificador para el valor de error generado en la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="0452e-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="0452e-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0452e-109">_ulFlags_</span></span>
  
> <span data-ttu-id="0452e-110">[entrada] Una máscara de bits de indicadores que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="0452e-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="0452e-111">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="0452e-111">The following flag can be set:</span></span>
    
<span data-ttu-id="0452e-112">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="0452e-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0452e-113">Las cadenas en la estructura **MAPIERROR** devuelta en el parámetro _lppMAPIError_ están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="0452e-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="0452e-114">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="0452e-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="0452e-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="0452e-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="0452e-116">[out] Un puntero a un puntero a una estructura **MAPIERROR** que contiene información de versión, el componente y el contexto para el error.</span><span class="sxs-lookup"><span data-stu-id="0452e-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="0452e-117">El parámetro _lppMAPIError_ se puede establecer en NULL si MAPI no puede proporcionar la información adecuada para una estructura **MAPIERROR** .</span><span class="sxs-lookup"><span data-stu-id="0452e-117">The  _lppMAPIError_ parameter can be set to NULL if MAPI cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0452e-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0452e-118">Return value</span></span>

<span data-ttu-id="0452e-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="0452e-119">S_OK</span></span> 
  
> <span data-ttu-id="0452e-120">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="0452e-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="0452e-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="0452e-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="0452e-122">Se ha establecido el indicador MAPI_UNICODE y la sesión no es compatible con Unicode.</span><span class="sxs-lookup"><span data-stu-id="0452e-122">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0452e-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0452e-123">Remarks</span></span>

<span data-ttu-id="0452e-124">El método **IMAPISession::GetLastError** recupera información sobre el último error que se ha devuelto por una llamada al método **IMAPISession** .</span><span class="sxs-lookup"><span data-stu-id="0452e-124">The **IMAPISession::GetLastError** method retrieves information about the last error that was returned by an **IMAPISession** method call.</span></span> <span data-ttu-id="0452e-125">Los clientes pueden proporcionar a sus usuarios con información detallada sobre el error mediante la inclusión de esta información en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0452e-125">Clients can provide their users with detailed information about the error by including this information in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0452e-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="0452e-126">Notes to callers</span></span>

<span data-ttu-id="0452e-127">Puede usar la estructura **MAPIERROR** , si MAPI proporciona uno, indicada por el sólo de si de parámetro _lppMAPIError_ **GetLastError** devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="0452e-127">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="0452e-128">En ocasiones, MAPI no puede determinar cuál era el último error o no tiene nada más para informar sobre el error.</span><span class="sxs-lookup"><span data-stu-id="0452e-128">Sometimes MAPI cannot determine what the last error was, or it has nothing more to report about the error.</span></span> <span data-ttu-id="0452e-129">En esta situación, **GetLastError** devuelve un puntero a NULL en _lppMAPIError_ en su lugar.</span><span class="sxs-lookup"><span data-stu-id="0452e-129">In this situation, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="0452e-130">Para obtener más información acerca del método **GetLastError** , vea [Errores de MAPI extendida](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="0452e-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0452e-131">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="0452e-131">See also</span></span>



[<span data-ttu-id="0452e-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="0452e-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="0452e-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="0452e-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="0452e-134">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0452e-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="0452e-135">MAPI extendida de errores</span><span class="sxs-lookup"><span data-stu-id="0452e-135">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

