---
title: IMAPIControlGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetLastError
api_type:
- COM
ms.assetid: 83290b8e-fffc-41c8-a01e-578d130b65c5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 10ac4e33b3f734ec2ce3205aa1897e0418cb563d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421154"
---
# <a name="imapicontrolgetlasterror"></a><span data-ttu-id="72530-103">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="72530-103">IMAPIControl::GetLastError</span></span>

  
  
<span data-ttu-id="72530-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72530-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72530-105">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error de control de botón anterior.</span><span class="sxs-lookup"><span data-stu-id="72530-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="72530-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="72530-106">Parameters</span></span>

 <span data-ttu-id="72530-107">_Valores_</span><span class="sxs-lookup"><span data-stu-id="72530-107">_hResult_</span></span>
  
> <span data-ttu-id="72530-108">a Identificador del valor de error generado en la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="72530-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="72530-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="72530-109">_ulFlags_</span></span>
  
> <span data-ttu-id="72530-110">a Máscara de máscara de marcadores que controla el tipo de las cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="72530-110">[in] A bitmask of flags that controls the type of the strings returned.</span></span> <span data-ttu-id="72530-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="72530-111">The following flag can be set:</span></span>
    
<span data-ttu-id="72530-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="72530-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="72530-113">Las cadenas de la estructura **MAPIERROR** devueltas en el parámetro _lppMAPIError_ están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="72530-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="72530-114">Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="72530-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="72530-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="72530-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="72530-116">contempla Un puntero a un puntero a una estructura **MAPIERROR** que contiene información sobre la versión, el componente y el contexto del error.</span><span class="sxs-lookup"><span data-stu-id="72530-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="72530-117">El parámetro _lppMAPIError_ puede establecerse en NULL si el proveedor no puede proporcionar una estructura **MAPIERROR** con la información adecuada.</span><span class="sxs-lookup"><span data-stu-id="72530-117">The  _lppMAPIError_ parameter can be set to NULL if the provider cannot supply a **MAPIERROR** structure with appropriate information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="72530-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72530-118">Return value</span></span>

<span data-ttu-id="72530-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="72530-119">S_OK</span></span> 
  
> <span data-ttu-id="72530-120">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="72530-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="72530-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="72530-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="72530-122">Se estableció la marca MAPI_UNICODE y la implementación no admite Unicode, o no se estableció MAPI_UNICODE y la implementación solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="72530-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="72530-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="72530-123">Remarks</span></span>

<span data-ttu-id="72530-124">Los proveedores de servicios implementan el método **IMAPIControl:: GetLastError** para proporcionar información sobre una llamada a un método anterior que no se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="72530-124">Service providers implement the **IMAPIControl::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="72530-125">MAPI puede proporcionar a los usuarios información detallada sobre el error al mostrar los datos de la estructura **MAPIERROR** en un mensaje o cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="72530-125">MAPI can give users detailed information about the error by displaying the data from the **MAPIERROR** structure in a message or dialog box.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="72530-126">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="72530-126">Notes to implementers</span></span>

<span data-ttu-id="72530-127">No es necesario tener información que incluir en la estructura **MAPIERROR** para cada error.</span><span class="sxs-lookup"><span data-stu-id="72530-127">You do not need to have information to include in the **MAPIERROR** structure for every error.</span></span> <span data-ttu-id="72530-128">Puede que no sea posible determinar cuál era el error anterior.</span><span class="sxs-lookup"><span data-stu-id="72530-128">It may not be possible to determine what the previous error was.</span></span> <span data-ttu-id="72530-129">Si tiene información, devuelva S_OK y los datos adecuados en la estructura **MAPIERROR** .</span><span class="sxs-lookup"><span data-stu-id="72530-129">If you have information, return S_OK and the appropriate data in the **MAPIERROR** structure.</span></span> <span data-ttu-id="72530-130">Si no hay información disponible, devuelva S_OK y un puntero a NULL para el parámetro _lppMAPIError_ .</span><span class="sxs-lookup"><span data-stu-id="72530-130">If no information is available, return S_OK and a pointer to NULL for the  _lppMAPIError_ parameter.</span></span> 
  
<span data-ttu-id="72530-131">Para obtener más información sobre el método **GetLastError** , vea [errores extendidos de MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="72530-131">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="72530-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="72530-132">See also</span></span>



[<span data-ttu-id="72530-133">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="72530-133">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="72530-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="72530-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="72530-135">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="72530-135">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

