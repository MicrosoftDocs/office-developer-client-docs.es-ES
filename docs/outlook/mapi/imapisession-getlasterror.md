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
# <a name="imapisessiongetlasterror"></a><span data-ttu-id="f8553-103">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="f8553-103">IMAPISession::GetLastError</span></span>

  
  
<span data-ttu-id="f8553-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8553-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8553-105">Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error de sesión anterior.</span><span class="sxs-lookup"><span data-stu-id="f8553-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="f8553-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="f8553-106">Parameters</span></span>

 <span data-ttu-id="f8553-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="f8553-107">_hResult_</span></span>
  
> <span data-ttu-id="f8553-108">[in] Identificador del valor de error generado en la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="f8553-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="f8553-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f8553-109">_ulFlags_</span></span>
  
> <span data-ttu-id="f8553-110">[in] Máscara de bits de marcas que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="f8553-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="f8553-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="f8553-111">The following flag can be set:</span></span>
    
<span data-ttu-id="f8553-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f8553-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f8553-113">Las cadenas de la **estructura MAPIERROR** devueltas en el parámetro  _lppMAPIError_ están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="f8553-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="f8553-114">Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="f8553-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="f8553-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="f8553-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="f8553-116">[salida] Puntero a un puntero a una **estructura MAPIERROR** que contiene información de versión, componente y contexto del error.</span><span class="sxs-lookup"><span data-stu-id="f8553-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="f8553-117">El _parámetro lppMAPIError_ se puede establecer en NULL si MAPI no puede proporcionar información adecuada para una **estructura MAPIERROR.**</span><span class="sxs-lookup"><span data-stu-id="f8553-117">The  _lppMAPIError_ parameter can be set to NULL if MAPI cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f8553-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8553-118">Return value</span></span>

<span data-ttu-id="f8553-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="f8553-119">S_OK</span></span> 
  
> <span data-ttu-id="f8553-120">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="f8553-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="f8553-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="f8553-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="f8553-122">La MAPI_UNICODE se estableció y la sesión no admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="f8553-122">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f8553-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f8553-123">Remarks</span></span>

<span data-ttu-id="f8553-124">El **método IMAPISession::GetLastError** recupera información sobre el último error devuelto por una llamada al método **IMAPISession.**</span><span class="sxs-lookup"><span data-stu-id="f8553-124">The **IMAPISession::GetLastError** method retrieves information about the last error that was returned by an **IMAPISession** method call.</span></span> <span data-ttu-id="f8553-125">Los clientes pueden proporcionar a sus usuarios información detallada sobre el error mediante la inclusión de esta información en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f8553-125">Clients can provide their users with detailed information about the error by including this information in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f8553-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="f8553-126">Notes to callers</span></span>

<span data-ttu-id="f8553-127">Puede usar la estructura **MAPIERROR,** si MAPI proporciona una, apuntada por el parámetro  _lppMAPIError_ solo si **GetLastError** devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="f8553-127">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="f8553-128">A veces MAPI no puede determinar cuál fue el último error o no tiene nada más que informar sobre el error.</span><span class="sxs-lookup"><span data-stu-id="f8553-128">Sometimes MAPI cannot determine what the last error was, or it has nothing more to report about the error.</span></span> <span data-ttu-id="f8553-129">En esta situación, **GetLastError** devuelve un puntero a NULL en  _lppMAPIError en_ su lugar.</span><span class="sxs-lookup"><span data-stu-id="f8553-129">In this situation, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="f8553-130">Para obtener más información acerca **del método GetLastError,** vea [Mapi Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="f8553-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f8553-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8553-131">See also</span></span>



[<span data-ttu-id="f8553-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="f8553-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="f8553-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f8553-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f8553-134">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f8553-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="f8553-135">Errores extendidos mapi</span><span class="sxs-lookup"><span data-stu-id="f8553-135">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

