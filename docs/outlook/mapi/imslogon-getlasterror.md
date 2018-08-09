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
ms.openlocfilehash: a865a751f3e274008c7004315906d6705ba55161
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817821"
---
# <a name="imslogongetlasterror"></a><span data-ttu-id="1ce53-103">IMSLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="1ce53-103">IMSLogon::GetLastError</span></span>

  
  
<span data-ttu-id="1ce53-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1ce53-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1ce53-105">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el último error que se ha producido para el objeto de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1ce53-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="1ce53-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ce53-106">Parameters</span></span>

 <span data-ttu-id="1ce53-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="1ce53-107">_hResult_</span></span>
  
> <span data-ttu-id="1ce53-108">[entrada] Un tipo de datos HRESULT que contiene el valor de error generado en la llamada al método anterior para el objeto de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1ce53-108">[in] An HRESULT data type that contains the error value generated in the previous method call for the message store object.</span></span>
    
 <span data-ttu-id="1ce53-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1ce53-109">_ulFlags_</span></span>
  
> <span data-ttu-id="1ce53-110">[entrada] Una máscara de bits de indicadores que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="1ce53-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="1ce53-111">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="1ce53-111">The following flag can be set:</span></span>
    
<span data-ttu-id="1ce53-112">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="1ce53-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1ce53-113">Las cadenas en la estructura **MAPIERROR** devuelta en el parámetro _lppMAPIError_ están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="1ce53-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="1ce53-114">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="1ce53-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="1ce53-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="1ce53-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="1ce53-116">[out] Un puntero a un puntero a la estructura **MAPIERROR** devuelta que contiene información de versión, el componente y el contexto para el error.</span><span class="sxs-lookup"><span data-stu-id="1ce53-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="1ce53-117">El parámetro _lppMAPIError_ se puede establecer en NULL si no hay ningún **MAPIERROR** para devolver.</span><span class="sxs-lookup"><span data-stu-id="1ce53-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1ce53-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ce53-118">Return value</span></span>

<span data-ttu-id="1ce53-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="1ce53-119">S_OK</span></span> 
  
> <span data-ttu-id="1ce53-120">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="1ce53-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="1ce53-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="1ce53-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="1ce53-122">Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="1ce53-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1ce53-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1ce53-123">Remarks</span></span>

<span data-ttu-id="1ce53-124">Utilice el método **IMSLogon::GetLastError** para recuperar la información para mostrar en un mensaje al usuario sobre el último error devuelto desde una llamada al método para el objeto de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1ce53-124">Use the **IMSLogon::GetLastError** method to retrieve information to display in a message to the user regarding the last error returned from a method call for the message store object.</span></span> 
  
<span data-ttu-id="1ce53-125">Para liberar toda la memoria asignada por MAPI para la estructura **MAPIERROR** devuelta, aplicaciones cliente necesitan llamar a sólo la función [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="1ce53-125">To release all the memory allocated by MAPI for the returned **MAPIERROR** structure, client applications need to call only the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="1ce53-126">El valor devuelto de **GetLastError** debe ser S_OK para una aplicación que use el **MAPIERROR**.</span><span class="sxs-lookup"><span data-stu-id="1ce53-126">The return value from **GetLastError** must be S_OK for an application to use the **MAPIERROR**.</span></span> <span data-ttu-id="1ce53-127">Incluso si el valor devuelto es S_OK, que no se devuelvan un **MAPIERROR** .</span><span class="sxs-lookup"><span data-stu-id="1ce53-127">Even if the return value is S_OK, a **MAPIERROR** might not be returned.</span></span> <span data-ttu-id="1ce53-128">Si la implementación no puede determinar cuál era el último error, o si un **MAPIERROR** no está disponible para que el error, **GetLastError** devuelve un puntero a NULL en _lppMAPIError_ en su lugar.</span><span class="sxs-lookup"><span data-stu-id="1ce53-128">If the implementation cannot determine what the last error was, or if a **MAPIERROR** is not available for that error, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1ce53-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ce53-129">See also</span></span>



[<span data-ttu-id="1ce53-130">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="1ce53-130">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="1ce53-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="1ce53-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="1ce53-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1ce53-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

