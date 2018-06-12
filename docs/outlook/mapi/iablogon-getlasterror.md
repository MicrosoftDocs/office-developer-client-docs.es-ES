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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: bead72ab2b394634217c9ae219a03a98752ef27d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817089"
---
# <a name="iablogongetlasterror"></a><span data-ttu-id="ee10f-103">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="ee10f-103">IABLogon::GetLastError</span></span>

  
  
<span data-ttu-id="ee10f-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ee10f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ee10f-105">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error de proveedor de la libreta de direcciones anterior.</span><span class="sxs-lookup"><span data-stu-id="ee10f-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="ee10f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee10f-106">Parameters</span></span>

 <span data-ttu-id="ee10f-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="ee10f-107">_hResult_</span></span>
  
> <span data-ttu-id="ee10f-108">[entrada] Un identificador para el valor de error generado en la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="ee10f-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="ee10f-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ee10f-109">_ulFlags_</span></span>
  
> <span data-ttu-id="ee10f-110">[entrada] Una máscara de bits de indicadores que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="ee10f-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="ee10f-111">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="ee10f-111">The following flag can be set:</span></span>
    
<span data-ttu-id="ee10f-112">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="ee10f-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ee10f-113">Las cadenas en la estructura **MAPIERROR** devuelta en el parámetro _lppMAPIError_ están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="ee10f-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="ee10f-114">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="ee10f-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="ee10f-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="ee10f-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="ee10f-116">[out] Un puntero a un puntero a una estructura **MAPIERROR** que contiene información de versión, el componente y el contexto para el error.</span><span class="sxs-lookup"><span data-stu-id="ee10f-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="ee10f-117">El parámetro _lppMAPIError_ se puede establecer en NULL si el proveedor no puede proporcionar una estructura **MAPIERROR** con la información apropiada.</span><span class="sxs-lookup"><span data-stu-id="ee10f-117">The  _lppMAPIError_ parameter can be set to NULL if the provider cannot supply a **MAPIERROR** structure with appropriate information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ee10f-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee10f-118">Return value</span></span>

<span data-ttu-id="ee10f-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="ee10f-119">S_OK</span></span> 
  
> <span data-ttu-id="ee10f-120">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="ee10f-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="ee10f-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="ee10f-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="ee10f-122">Se ha establecido el indicador MAPI_UNICODE y el proveedor de la libreta de direcciones no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y el proveedor de la libreta de direcciones admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="ee10f-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ee10f-123">Notas</span><span class="sxs-lookup"><span data-stu-id="ee10f-123">Remarks</span></span>

<span data-ttu-id="ee10f-124">Los proveedores de la libreta de direcciones implementan el método **GetLastError** para proporcionar información acerca de una llamada de método anteriores que no se pudo.</span><span class="sxs-lookup"><span data-stu-id="ee10f-124">Address book providers implement the **GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="ee10f-125">Los autores de llamadas pueden proporcionar a sus usuarios con información detallada sobre el error mediante la inclusión de los datos de la estructura **MAPIERROR** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ee10f-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ee10f-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="ee10f-126">Notes to callers</span></span>

<span data-ttu-id="ee10f-127">Puede usar la estructura **MAPIERROR** indicada por el parámetro _lppMAPIError_ si el proveedor de la libreta de direcciones proporciona la estructura y sólo si **GetLastError** devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="ee10f-127">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if the address book provider supplies the structure and only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="ee10f-128">En ocasiones, el proveedor de la libreta de direcciones no puede determinar qué era el último error o no tiene nada más para informar sobre el error.</span><span class="sxs-lookup"><span data-stu-id="ee10f-128">Sometimes the address book provider cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="ee10f-129">En esta situación, el proveedor de la libreta de direcciones devuelve un puntero a NULL en _lppMAPIError_ en su lugar.</span><span class="sxs-lookup"><span data-stu-id="ee10f-129">In this situation, the address book provider returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="ee10f-130">Para obtener más información acerca del método **GetLastError** , vea [Errores de MAPI extendida](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="ee10f-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ee10f-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="ee10f-131">See also</span></span>



[<span data-ttu-id="ee10f-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="ee10f-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="ee10f-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ee10f-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ee10f-134">IABLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ee10f-134">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

