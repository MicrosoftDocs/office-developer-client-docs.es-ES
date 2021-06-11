---
title: IMAPIFormFactoryGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.GetLastError
api_type:
- COM
ms.assetid: 4b1d85f6-7996-4839-b985-abf83e305651
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2c83f7788d9c01ab02f1a2bc39a35abe2c5a21c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417013"
---
# <a name="imapiformfactorygetlasterror"></a><span data-ttu-id="340bf-103">IMAPIFormFactory::GetLastError</span><span class="sxs-lookup"><span data-stu-id="340bf-103">IMAPIFormFactory::GetLastError</span></span>

  
  
<span data-ttu-id="340bf-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="340bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="340bf-105">Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produjo en el objeto de fábrica de formularios.</span><span class="sxs-lookup"><span data-stu-id="340bf-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form factory object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="340bf-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="340bf-106">Parameters</span></span>

 <span data-ttu-id="340bf-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="340bf-107">_hResult_</span></span>
  
> <span data-ttu-id="340bf-108">[in] Tipo de datos HRESULT que contiene el valor de error generado en la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="340bf-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="340bf-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="340bf-109">_ulFlags_</span></span>
  
> <span data-ttu-id="340bf-110">[in] Máscara de bits de marcas que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="340bf-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="340bf-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="340bf-111">The following flag can be set:</span></span> 
    
<span data-ttu-id="340bf-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="340bf-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="340bf-113">Las cadenas de la **estructura MAPIERROR** devueltas en el parámetro  _lppMAPIError_ están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="340bf-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="340bf-114">Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="340bf-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="340bf-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="340bf-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="340bf-116">[salida] Puntero a un puntero a la estructura **MAPIERROR** devuelta que contiene información de versión, componente y contexto del error.</span><span class="sxs-lookup"><span data-stu-id="340bf-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="340bf-117">Este parámetro se puede establecer en NULL si no hay ninguna **estructura MAPIERROR** que devolver.</span><span class="sxs-lookup"><span data-stu-id="340bf-117">This parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="340bf-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="340bf-118">Return value</span></span>

<span data-ttu-id="340bf-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="340bf-119">S_OK</span></span> 
  
> <span data-ttu-id="340bf-120">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="340bf-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="340bf-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="340bf-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="340bf-122">La marca MAPI_UNICODE se estableció y **GetLastError** no admite Unicode o MAPI_UNICODE no se estableció y **GetLastError** solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="340bf-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** supports only Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="340bf-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="340bf-123">Remarks</span></span>

<span data-ttu-id="340bf-124">El **método IMAPIFormFactory::GetLastError** proporciona información sobre una llamada de método anterior que falló.</span><span class="sxs-lookup"><span data-stu-id="340bf-124">The **IMAPIFormFactory::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="340bf-125">Los autores de llamadas pueden proporcionar a sus usuarios información detallada sobre el error al incluir los datos de la estructura **MAPIERROR** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="340bf-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="340bf-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="340bf-126">Notes to callers</span></span>

<span data-ttu-id="340bf-127">Puede usar la estructura **MAPIERROR** a la que apunta el parámetro  _lppMAPIError_ si MAPI proporciona uno solo si **GetLastError** devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="340bf-127">You can make use of the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if MAPI supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="340bf-128">A veces MAPI no puede determinar cuál fue el último error o no tiene nada más que informar sobre el error.</span><span class="sxs-lookup"><span data-stu-id="340bf-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="340bf-129">En esta situación, se devuelve un puntero a NULL en  _lppMAPIError_ en su lugar.</span><span class="sxs-lookup"><span data-stu-id="340bf-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="340bf-130">Para obtener más información sobre el **método GetLastError,** vea [Using Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="340bf-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="340bf-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="340bf-131">See also</span></span>



[<span data-ttu-id="340bf-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="340bf-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="340bf-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="340bf-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="340bf-134">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="340bf-134">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

