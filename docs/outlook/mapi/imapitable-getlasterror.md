---
title: IMAPITableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetLastError
api_type:
- COM
ms.assetid: 832e2c18-ddba-4d18-a391-710d21fe23e6
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8b7b1db5bcc718858b01f122f53406c885998741
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593819"
---
# <a name="imapitablegetlasterror"></a><span data-ttu-id="5bb03-103">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="5bb03-103">IMAPITable::GetLastError</span></span>

  
  
<span data-ttu-id="5bb03-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5bb03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5bb03-105">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior en la tabla.</span><span class="sxs-lookup"><span data-stu-id="5bb03-105">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span> 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="5bb03-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5bb03-106">Parameters</span></span>

 <span data-ttu-id="5bb03-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="5bb03-107">_hResult_</span></span>
  
> <span data-ttu-id="5bb03-108">[entrada] HRESULT que contiene el error generado en la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="5bb03-108">[in] HRESULT containing the error generated in the previous method call.</span></span>
    
 <span data-ttu-id="5bb03-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5bb03-109">_ulFlags_</span></span>
  
> <span data-ttu-id="5bb03-110">[entrada] Máscara de bits de indicadores que controla el tipo de las cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="5bb03-110">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="5bb03-111">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="5bb03-111">The following flag can be set:</span></span>
    
<span data-ttu-id="5bb03-112">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="5bb03-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5bb03-113">Las cadenas en la estructura **MAPIERROR** devuelta en el parámetro _lppMAPIError_ están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="5bb03-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="5bb03-114">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="5bb03-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="5bb03-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="5bb03-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="5bb03-116">[out] Puntero a un puntero a la estructura **MAPIERROR** devuelta que contiene información de versión, el componente y el contexto para el error.</span><span class="sxs-lookup"><span data-stu-id="5bb03-116">[out] Pointer to a pointer to the returned **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="5bb03-117">El parámetro _lppMAPIError_ se puede establecer en NULL si no se puede proporcionar una estructura **MAPIERROR** con la información apropiada.</span><span class="sxs-lookup"><span data-stu-id="5bb03-117">The  _lppMAPIError_ parameter can be set to NULL if a **MAPIERROR** structure with appropriate information cannot be provided.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5bb03-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5bb03-118">Return value</span></span>

<span data-ttu-id="5bb03-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="5bb03-119">S_OK</span></span> 
  
> <span data-ttu-id="5bb03-120">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="5bb03-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="5bb03-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="5bb03-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="5bb03-122">Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación sólo es compatible con Unicode.</span><span class="sxs-lookup"><span data-stu-id="5bb03-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5bb03-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5bb03-123">Remarks</span></span>

<span data-ttu-id="5bb03-124">El método **IMAPITable::GetLastError** devuelve información detallada, si está disponible, acerca de una llamada al método anterior con errores.</span><span class="sxs-lookup"><span data-stu-id="5bb03-124">The **IMAPITable::GetLastError** method returns detailed information, if available, about a prior method call that failed.</span></span> <span data-ttu-id="5bb03-125">Esta información se puede mostrar en un mensaje o un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="5bb03-125">This information can be displayed in a message or a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5bb03-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="5bb03-126">Notes to callers</span></span>

<span data-ttu-id="5bb03-127">Llamar a **GetLastError** cada vez que necesite mostrar información sobre un error al usuario.</span><span class="sxs-lookup"><span data-stu-id="5bb03-127">Call **GetLastError** whenever you need to display information about an error to the user.</span></span> 
  
<span data-ttu-id="5bb03-128">Se puede hacer uso de la [MAPIERROR](mapierror.md) estructura indicada por el parámetro _lppMAPIError_ si el objeto de tabla suministra uno sólo si **GetLastError** devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="5bb03-128">You can make use of the [MAPIERROR](mapierror.md) structure pointed to by the  _lppMAPIError_ parameter if the table object supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="5bb03-129">En ocasiones, la implementación de la tabla no puede determinar qué era el último error o no tiene nada más para informar sobre el error.</span><span class="sxs-lookup"><span data-stu-id="5bb03-129">Sometimes the table implementation cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="5bb03-130">En esta situación, el puntero en _lppMAPIError_ se establece en NULL.</span><span class="sxs-lookup"><span data-stu-id="5bb03-130">In this situation, the pointer at  _lppMAPIError_ is set to NULL.</span></span> 
  
<span data-ttu-id="5bb03-131">Para liberar toda la memoria asignada para la estructura **MAPIERROR** , llame a la función [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="5bb03-131">To release all the memory allocated for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="5bb03-132">Para obtener más información acerca del método **GetLastError** , vea [Errores de MAPI extendida](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="5bb03-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5bb03-133">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="5bb03-133">See also</span></span>



[<span data-ttu-id="5bb03-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="5bb03-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="5bb03-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="5bb03-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="5bb03-136">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5bb03-136">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

