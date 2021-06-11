---
title: IABLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetLastError
api_type:
- COM
ms.assetid: d157e29e-7731-4e47-b4a7-e8622b223001
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 311299b00143667b3f2fb22bd7be6c3a52c7141d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434252"
---
# <a name="iablogongetlasterror"></a><span data-ttu-id="23539-103">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="23539-103">IABLogon::GetLastError</span></span>

  
  
<span data-ttu-id="23539-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23539-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23539-105">Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error del proveedor de libreta de direcciones anterior.</span><span class="sxs-lookup"><span data-stu-id="23539-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="23539-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="23539-106">Parameters</span></span>

 <span data-ttu-id="23539-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="23539-107">_hResult_</span></span>
  
> <span data-ttu-id="23539-108">[in] Identificador del valor de error generado en la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="23539-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="23539-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="23539-109">_ulFlags_</span></span>
  
> <span data-ttu-id="23539-110">[in] Máscara de bits de marcas que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="23539-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="23539-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="23539-111">The following flag can be set:</span></span>
    
<span data-ttu-id="23539-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="23539-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="23539-113">Las cadenas de la **estructura MAPIERROR** devueltas en el parámetro  _lppMAPIError_ están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="23539-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="23539-114">Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="23539-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="23539-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="23539-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="23539-116">[salida] Puntero a un puntero a una **estructura MAPIERROR** que contiene información de versión, componente y contexto del error.</span><span class="sxs-lookup"><span data-stu-id="23539-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="23539-117">El  _parámetro lppMAPIError_ se puede establecer en NULL si el proveedor no puede proporcionar una **estructura MAPIERROR** con la información adecuada.</span><span class="sxs-lookup"><span data-stu-id="23539-117">The  _lppMAPIError_ parameter can be set to NULL if the provider cannot supply a **MAPIERROR** structure with appropriate information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="23539-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23539-118">Return value</span></span>

<span data-ttu-id="23539-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="23539-119">S_OK</span></span> 
  
> <span data-ttu-id="23539-120">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="23539-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="23539-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="23539-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="23539-122">Se estableció MAPI_UNICODE marca y el proveedor de libreta de direcciones no admite Unicode o MAPI_UNICODE no se estableció y el proveedor de libreta de direcciones solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="23539-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="23539-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="23539-123">Remarks</span></span>

<span data-ttu-id="23539-124">Los proveedores de libreta de direcciones implementan **el método GetLastError** para proporcionar información acerca de una llamada al método anterior que falló.</span><span class="sxs-lookup"><span data-stu-id="23539-124">Address book providers implement the **GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="23539-125">Los autores de llamadas pueden proporcionar a sus usuarios información detallada sobre el error al incluir los datos de la estructura **MAPIERROR** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="23539-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="23539-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="23539-126">Notes to callers</span></span>

<span data-ttu-id="23539-127">Puede usar la estructura **MAPIERROR** a la que apunta el parámetro  _lppMAPIError_ si el proveedor de libreta de direcciones proporciona la estructura y solo si **GetLastError** devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="23539-127">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if the address book provider supplies the structure and only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="23539-128">A veces, el proveedor de libreta de direcciones no puede determinar cuál fue el último error o no tiene nada más que informar sobre el error.</span><span class="sxs-lookup"><span data-stu-id="23539-128">Sometimes the address book provider cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="23539-129">En esta situación, el proveedor de libreta de direcciones devuelve un puntero a NULL en  _lppMAPIError en_ su lugar.</span><span class="sxs-lookup"><span data-stu-id="23539-129">In this situation, the address book provider returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="23539-130">Para obtener más información acerca **del método GetLastError,** vea [Mapi Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="23539-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="23539-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="23539-131">See also</span></span>



[<span data-ttu-id="23539-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="23539-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="23539-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="23539-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="23539-134">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="23539-134">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

