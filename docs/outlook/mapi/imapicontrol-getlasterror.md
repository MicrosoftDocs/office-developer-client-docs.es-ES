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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 2be5e40de6894b99d9de86423e99dd95a08bc04c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817197"
---
# <a name="imapicontrolgetlasterror"></a><span data-ttu-id="54fe3-103">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="54fe3-103">IMAPIControl::GetLastError</span></span>

  
  
<span data-ttu-id="54fe3-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="54fe3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="54fe3-105">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error de control de botón anterior.</span><span class="sxs-lookup"><span data-stu-id="54fe3-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="54fe3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54fe3-106">Parameters</span></span>

 <span data-ttu-id="54fe3-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="54fe3-107">_hResult_</span></span>
  
> <span data-ttu-id="54fe3-108">[entrada] Un identificador para el valor de error generado en la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="54fe3-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="54fe3-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="54fe3-109">_ulFlags_</span></span>
  
> <span data-ttu-id="54fe3-110">[entrada] Una máscara de bits de indicadores que controla el tipo de las cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="54fe3-110">[in] A bitmask of flags that controls the type of the strings returned.</span></span> <span data-ttu-id="54fe3-111">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="54fe3-111">The following flag can be set:</span></span>
    
<span data-ttu-id="54fe3-112">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="54fe3-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="54fe3-113">Las cadenas en la estructura **MAPIERROR** devuelta en el parámetro _lppMAPIError_ están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="54fe3-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="54fe3-114">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="54fe3-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="54fe3-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="54fe3-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="54fe3-116">[out] Un puntero a un puntero a una estructura **MAPIERROR** que contiene información de versión, el componente y el contexto para el error.</span><span class="sxs-lookup"><span data-stu-id="54fe3-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="54fe3-117">El parámetro _lppMAPIError_ se puede establecer en NULL si el proveedor no puede proporcionar una estructura **MAPIERROR** con la información apropiada.</span><span class="sxs-lookup"><span data-stu-id="54fe3-117">The  _lppMAPIError_ parameter can be set to NULL if the provider cannot supply a **MAPIERROR** structure with appropriate information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="54fe3-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54fe3-118">Return value</span></span>

<span data-ttu-id="54fe3-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="54fe3-119">S_OK</span></span> 
  
> <span data-ttu-id="54fe3-120">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="54fe3-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="54fe3-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="54fe3-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="54fe3-122">Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="54fe3-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="54fe3-123">Notas</span><span class="sxs-lookup"><span data-stu-id="54fe3-123">Remarks</span></span>

<span data-ttu-id="54fe3-124">Proveedores de servicios de implementan el método **IMAPIControl::GetLastError** para proporcionar información acerca de una llamada al método anterior con errores.</span><span class="sxs-lookup"><span data-stu-id="54fe3-124">Service providers implement the **IMAPIControl::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="54fe3-125">MAPI puede dar a los usuarios información detallada sobre el error mediante la presentación de los datos de la estructura **MAPIERROR** en un cuadro de diálogo o mensaje.</span><span class="sxs-lookup"><span data-stu-id="54fe3-125">MAPI can give users detailed information about the error by displaying the data from the **MAPIERROR** structure in a message or dialog box.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="54fe3-126">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="54fe3-126">Notes to implementers</span></span>

<span data-ttu-id="54fe3-127">No es necesario tener información que debe incluirse en la estructura **MAPIERROR** para cada error.</span><span class="sxs-lookup"><span data-stu-id="54fe3-127">You do not need to have information to include in the **MAPIERROR** structure for every error.</span></span> <span data-ttu-id="54fe3-128">Es posible que no pueda determinar la causa del error anterior.</span><span class="sxs-lookup"><span data-stu-id="54fe3-128">It may not be possible to determine what the previous error was.</span></span> <span data-ttu-id="54fe3-129">Si dispone de información, devolver S_OK y los datos adecuados en la estructura **MAPIERROR** .</span><span class="sxs-lookup"><span data-stu-id="54fe3-129">If you have information, return S_OK and the appropriate data in the **MAPIERROR** structure.</span></span> <span data-ttu-id="54fe3-130">Si no hay información disponible, puede devolver S_OK y un puntero en NULL para el parámetro _lppMAPIError_ .</span><span class="sxs-lookup"><span data-stu-id="54fe3-130">If no information is available, return S_OK and a pointer to NULL for the  _lppMAPIError_ parameter.</span></span> 
  
<span data-ttu-id="54fe3-131">Para obtener más información acerca del método **GetLastError** , vea [Errores de MAPI extendida](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="54fe3-131">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="54fe3-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="54fe3-132">See also</span></span>



[<span data-ttu-id="54fe3-133">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="54fe3-133">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="54fe3-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="54fe3-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="54fe3-135">IMAPIControl: IUnknown</span><span class="sxs-lookup"><span data-stu-id="54fe3-135">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

