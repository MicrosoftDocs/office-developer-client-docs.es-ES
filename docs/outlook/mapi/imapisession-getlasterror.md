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
ms.openlocfilehash: 7477213ee854be1ae71b47a0c1b339c4c13b6f04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435582"
---
# <a name="imapisessiongetlasterror"></a><span data-ttu-id="1aed5-103">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="1aed5-103">IMAPISession::GetLastError</span></span>

  
  
<span data-ttu-id="1aed5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1aed5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1aed5-105">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error de sesión anterior.</span><span class="sxs-lookup"><span data-stu-id="1aed5-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="1aed5-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="1aed5-106">Parameters</span></span>

 <span data-ttu-id="1aed5-107">_Valores_</span><span class="sxs-lookup"><span data-stu-id="1aed5-107">_hResult_</span></span>
  
> <span data-ttu-id="1aed5-108">a Identificador del valor de error generado en la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="1aed5-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="1aed5-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1aed5-109">_ulFlags_</span></span>
  
> <span data-ttu-id="1aed5-110">a Máscara de máscara de marcadores que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="1aed5-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="1aed5-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="1aed5-111">The following flag can be set:</span></span>
    
<span data-ttu-id="1aed5-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1aed5-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1aed5-113">Las cadenas de la estructura **MAPIERROR** devueltas en el parámetro _lppMAPIError_ están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="1aed5-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="1aed5-114">Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="1aed5-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="1aed5-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="1aed5-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="1aed5-116">contempla Un puntero a un puntero a una estructura **MAPIERROR** que contiene información sobre la versión, el componente y el contexto del error.</span><span class="sxs-lookup"><span data-stu-id="1aed5-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="1aed5-117">El parámetro _lppMAPIError_ puede establecerse en NULL si MAPI no puede proporcionar la información adecuada para una estructura **MAPIERROR** .</span><span class="sxs-lookup"><span data-stu-id="1aed5-117">The  _lppMAPIError_ parameter can be set to NULL if MAPI cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1aed5-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1aed5-118">Return value</span></span>

<span data-ttu-id="1aed5-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="1aed5-119">S_OK</span></span> 
  
> <span data-ttu-id="1aed5-120">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="1aed5-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="1aed5-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="1aed5-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="1aed5-122">La marca MAPI_UNICODE se estableció y la sesión no es compatible con Unicode.</span><span class="sxs-lookup"><span data-stu-id="1aed5-122">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1aed5-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1aed5-123">Remarks</span></span>

<span data-ttu-id="1aed5-124">El método **IMAPISession:: GetLastError** recupera información sobre el último error devuelto por una llamada al método **IMAPISession** .</span><span class="sxs-lookup"><span data-stu-id="1aed5-124">The **IMAPISession::GetLastError** method retrieves information about the last error that was returned by an **IMAPISession** method call.</span></span> <span data-ttu-id="1aed5-125">Los clientes pueden proporcionar a sus usuarios información detallada acerca del error al incluir esta información en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1aed5-125">Clients can provide their users with detailed information about the error by including this information in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1aed5-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="1aed5-126">Notes to callers</span></span>

<span data-ttu-id="1aed5-127">Puede usar la estructura **MAPIERROR** , si MAPI proporciona uno, apuntado por el parámetro _LppMAPIError_ solo si **GetLastError** Devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="1aed5-127">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="1aed5-128">A veces MAPI no puede determinar qué ha sido el último error o no tiene nada más que informar sobre el error.</span><span class="sxs-lookup"><span data-stu-id="1aed5-128">Sometimes MAPI cannot determine what the last error was, or it has nothing more to report about the error.</span></span> <span data-ttu-id="1aed5-129">En esta situación, **GetLastError** devuelve un puntero a NULL en _lppMAPIError_ en su lugar.</span><span class="sxs-lookup"><span data-stu-id="1aed5-129">In this situation, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="1aed5-130">Para obtener más información sobre el método **GetLastError** , vea [errores extendidos de MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="1aed5-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1aed5-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="1aed5-131">See also</span></span>



[<span data-ttu-id="1aed5-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="1aed5-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="1aed5-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="1aed5-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="1aed5-134">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1aed5-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="1aed5-135">Errores extendidos de MAPI</span><span class="sxs-lookup"><span data-stu-id="1aed5-135">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

