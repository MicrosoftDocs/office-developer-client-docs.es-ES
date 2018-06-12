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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 9906cb9510716b3be11a1b8bcf12f06e73789445
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817297"
---
# <a name="imapiformfactorygetlasterror"></a><span data-ttu-id="17f49-103">IMAPIFormFactory::GetLastError</span><span class="sxs-lookup"><span data-stu-id="17f49-103">IMAPIFormFactory::GetLastError</span></span>

  
  
<span data-ttu-id="17f49-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="17f49-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="17f49-105">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se producen al objeto de fábrica de formulario.</span><span class="sxs-lookup"><span data-stu-id="17f49-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form factory object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="17f49-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17f49-106">Parameters</span></span>

 <span data-ttu-id="17f49-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="17f49-107">_hResult_</span></span>
  
> <span data-ttu-id="17f49-108">[entrada] Un tipo de datos HRESULT que contiene el valor de error generado en la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="17f49-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="17f49-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="17f49-109">_ulFlags_</span></span>
  
> <span data-ttu-id="17f49-110">[entrada] Una máscara de bits de indicadores que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="17f49-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="17f49-111">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="17f49-111">The following flag can be set:</span></span> 
    
<span data-ttu-id="17f49-112">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="17f49-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="17f49-113">Las cadenas en la estructura **MAPIERROR** devuelta en el parámetro _lppMAPIError_ están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="17f49-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="17f49-114">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="17f49-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="17f49-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="17f49-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="17f49-116">[out] Un puntero a un puntero a la estructura **MAPIERROR** devuelta que contiene información de versión, el componente y el contexto para el error.</span><span class="sxs-lookup"><span data-stu-id="17f49-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="17f49-117">Este parámetro puede establecerse en NULL si no hay ninguna estructura **MAPIERROR** para devolver.</span><span class="sxs-lookup"><span data-stu-id="17f49-117">This parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="17f49-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17f49-118">Return value</span></span>

<span data-ttu-id="17f49-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="17f49-119">S_OK</span></span> 
  
> <span data-ttu-id="17f49-120">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="17f49-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="17f49-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="17f49-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="17f49-122">Se ha establecido el indicador MAPI_UNICODE y **GetLastError** no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y **GetLastError** admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="17f49-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** supports only Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="17f49-123">Notas</span><span class="sxs-lookup"><span data-stu-id="17f49-123">Remarks</span></span>

<span data-ttu-id="17f49-124">El método **IMAPIFormFactory::GetLastError** proporciona información acerca de una llamada de método anteriores que no se pudo.</span><span class="sxs-lookup"><span data-stu-id="17f49-124">The **IMAPIFormFactory::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="17f49-125">Los autores de llamadas pueden proporcionar a sus usuarios con información detallada sobre el error mediante la inclusión de los datos de la estructura **MAPIERROR** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="17f49-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="17f49-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="17f49-126">Notes to callers</span></span>

<span data-ttu-id="17f49-127">Se puede hacer uso de la **MAPIERROR** estructura indicada por el parámetro _lppMAPIError_ si MAPI proporciona uno sólo si **GetLastError** devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="17f49-127">You can make use of the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if MAPI supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="17f49-128">En ocasiones, MAPI no puede determinar qué era el último error o no tiene nada más para informar sobre el error.</span><span class="sxs-lookup"><span data-stu-id="17f49-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="17f49-129">En esta situación, se devuelve un puntero a NULL en _lppMAPIError_ en su lugar.</span><span class="sxs-lookup"><span data-stu-id="17f49-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="17f49-130">Para obtener más información acerca del método **GetLastError** , vea [Uso de errores extendido](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="17f49-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="17f49-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="17f49-131">See also</span></span>



[<span data-ttu-id="17f49-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="17f49-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="17f49-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="17f49-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="17f49-134">IMAPIFormFactory: IUnknown</span><span class="sxs-lookup"><span data-stu-id="17f49-134">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

