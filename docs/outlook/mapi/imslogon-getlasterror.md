---
title: IMSLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.GetLastError
api_type:
- COM
ms.assetid: 3e296f6d-4833-4c68-9b84-df0b09878474
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 472502d0f033370b06a69596944350152ab794f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425879"
---
# <a name="imslogongetlasterror"></a><span data-ttu-id="ae1c8-103">IMSLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="ae1c8-103">IMSLogon::GetLastError</span></span>

  
  
<span data-ttu-id="ae1c8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae1c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae1c8-105">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el último error que se produjo en el objeto de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="ae1c8-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ae1c8-106">Parameters</span></span>

 <span data-ttu-id="ae1c8-107">_Valores_</span><span class="sxs-lookup"><span data-stu-id="ae1c8-107">_hResult_</span></span>
  
> <span data-ttu-id="ae1c8-108">a Tipo de datos HRESULT que contiene el valor de error generado en la llamada al método anterior para el objeto de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-108">[in] An HRESULT data type that contains the error value generated in the previous method call for the message store object.</span></span>
    
 <span data-ttu-id="ae1c8-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ae1c8-109">_ulFlags_</span></span>
  
> <span data-ttu-id="ae1c8-110">a Máscara de máscara de marcadores que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="ae1c8-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="ae1c8-111">The following flag can be set:</span></span>
    
<span data-ttu-id="ae1c8-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ae1c8-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ae1c8-113">Las cadenas de la estructura **MAPIERROR** devueltas en el parámetro _lppMAPIError_ están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="ae1c8-114">Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="ae1c8-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="ae1c8-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="ae1c8-116">contempla Un puntero a un puntero a la estructura **MAPIERROR** devuelta que contiene la información de versión, componente y contexto del error.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="ae1c8-117">El parámetro _lppMAPIError_ puede establecerse en NULL si no hay ningún **MAPIERROR** para devolver.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ae1c8-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ae1c8-118">Return value</span></span>

<span data-ttu-id="ae1c8-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae1c8-119">S_OK</span></span> 
  
> <span data-ttu-id="ae1c8-120">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="ae1c8-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="ae1c8-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="ae1c8-122">Se estableció la marca MAPI_UNICODE y la implementación no admite Unicode, o no se estableció MAPI_UNICODE y la implementación solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ae1c8-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ae1c8-123">Remarks</span></span>

<span data-ttu-id="ae1c8-124">Use el método **IMSLogon:: GetLastError** para recuperar la información que se mostrará en un mensaje al usuario sobre el último error devuelto desde una llamada de método para el objeto de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-124">Use the **IMSLogon::GetLastError** method to retrieve information to display in a message to the user regarding the last error returned from a method call for the message store object.</span></span> 
  
<span data-ttu-id="ae1c8-125">Para liberar toda la memoria asignada por MAPI para la estructura **MAPIERROR** devuelta, las aplicaciones cliente solo deben llamar a la función [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="ae1c8-125">To release all the memory allocated by MAPI for the returned **MAPIERROR** structure, client applications need to call only the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="ae1c8-126">El valor devuelto de **GetLastError** debe ser S_OK para que una aplicación use **MAPIERROR**.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-126">The return value from **GetLastError** must be S_OK for an application to use the **MAPIERROR**.</span></span> <span data-ttu-id="ae1c8-127">Incluso si el valor devuelto es S_OK, es posible que no se devuelva un **MAPIERROR** .</span><span class="sxs-lookup"><span data-stu-id="ae1c8-127">Even if the return value is S_OK, a **MAPIERROR** might not be returned.</span></span> <span data-ttu-id="ae1c8-128">Si la implementación no puede determinar cuál era el último error o si un **MAPIERROR** no está disponible para ese error, **GetLastError** devuelve un puntero a NULL en _lppMAPIError_ en su lugar.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-128">If the implementation cannot determine what the last error was, or if a **MAPIERROR** is not available for that error, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ae1c8-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="ae1c8-129">See also</span></span>



[<span data-ttu-id="ae1c8-130">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="ae1c8-130">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="ae1c8-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ae1c8-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ae1c8-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ae1c8-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

