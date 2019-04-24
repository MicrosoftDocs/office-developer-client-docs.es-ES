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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349031"
---
# <a name="iablogongetlasterror"></a><span data-ttu-id="26f57-103">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="26f57-103">IABLogon::GetLastError</span></span>

  
  
<span data-ttu-id="26f57-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26f57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26f57-105">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior del proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="26f57-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="26f57-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="26f57-106">Parameters</span></span>

 <span data-ttu-id="26f57-107">_Valores_</span><span class="sxs-lookup"><span data-stu-id="26f57-107">_hResult_</span></span>
  
> <span data-ttu-id="26f57-108">a Identificador del valor de error generado en la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="26f57-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="26f57-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="26f57-109">_ulFlags_</span></span>
  
> <span data-ttu-id="26f57-110">a Máscara de máscara de marcadores que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="26f57-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="26f57-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="26f57-111">The following flag can be set:</span></span>
    
<span data-ttu-id="26f57-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="26f57-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="26f57-113">Las cadenas de la estructura **MAPIERROR** devueltas en el parámetro _lppMAPIError_ están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="26f57-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="26f57-114">Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="26f57-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="26f57-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="26f57-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="26f57-116">contempla Un puntero a un puntero a una estructura **MAPIERROR** que contiene información sobre la versión, el componente y el contexto del error.</span><span class="sxs-lookup"><span data-stu-id="26f57-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="26f57-117">El parámetro _lppMAPIError_ puede establecerse en NULL si el proveedor no puede proporcionar una estructura **MAPIERROR** con la información adecuada.</span><span class="sxs-lookup"><span data-stu-id="26f57-117">The  _lppMAPIError_ parameter can be set to NULL if the provider cannot supply a **MAPIERROR** structure with appropriate information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="26f57-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26f57-118">Return value</span></span>

<span data-ttu-id="26f57-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="26f57-119">S_OK</span></span> 
  
> <span data-ttu-id="26f57-120">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="26f57-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="26f57-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="26f57-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="26f57-122">Se estableció la marca MAPI_UNICODE y el proveedor de la libreta de direcciones no admite Unicode, o no se estableció MAPI_UNICODE y el proveedor de la libreta de direcciones solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="26f57-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="26f57-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="26f57-123">Remarks</span></span>

<span data-ttu-id="26f57-124">Los proveedores de la libreta de direcciones implementan el método **GetLastError** para proporcionar información sobre una llamada a un método anterior que no se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="26f57-124">Address book providers implement the **GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="26f57-125">Los autores de llamadas pueden proporcionar a sus usuarios información detallada acerca del error al incluir los datos de la estructura **MAPIERROR** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="26f57-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="26f57-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="26f57-126">Notes to callers</span></span>

<span data-ttu-id="26f57-127">Puede usar la estructura **MAPIERROR** apuntado por el parámetro _lppMAPIError_ si el proveedor de la libreta de direcciones proporciona la estructura y solo si **GetLastError** Devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="26f57-127">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if the address book provider supplies the structure and only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="26f57-128">A veces, el proveedor de la libreta de direcciones no puede determinar qué ha sido el último error o no tiene nada más para informar sobre el error.</span><span class="sxs-lookup"><span data-stu-id="26f57-128">Sometimes the address book provider cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="26f57-129">En esta situación, el proveedor de la libreta de direcciones devuelve un puntero a NULL en _lppMAPIError_ en su lugar.</span><span class="sxs-lookup"><span data-stu-id="26f57-129">In this situation, the address book provider returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="26f57-130">Para obtener más información sobre el método **GetLastError** , vea [errores extendidos de MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="26f57-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="26f57-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="26f57-131">See also</span></span>



[<span data-ttu-id="26f57-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="26f57-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="26f57-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="26f57-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="26f57-134">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="26f57-134">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

