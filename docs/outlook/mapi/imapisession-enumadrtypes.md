---
title: IMAPISessionEnumAdrTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.EnumAdrTypes
api_type:
- COM
ms.assetid: 9a3702a4-8a6b-4c0c-a90f-02be3a2bfa05
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3b2e41c4b1bfc4879717df0c73bbcd45a724ca60
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439292"
---
# <a name="imapisessionenumadrtypes"></a><span data-ttu-id="eb8ff-103">IMAPISession::EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="eb8ff-103">IMAPISession::EnumAdrTypes</span></span>

  
  
<span data-ttu-id="eb8ff-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb8ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb8ff-105">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="eb8ff-105">Deprecated.</span></span> <span data-ttu-id="eb8ff-106">Devuelve los tipos de direcciones que pueden controlar todos los proveedores de transporte de la sesión.</span><span class="sxs-lookup"><span data-stu-id="eb8ff-106">Returns the address types that can be handled by all of the transport providers in the session.</span></span> 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a><span data-ttu-id="eb8ff-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="eb8ff-107">Parameters</span></span>

 <span data-ttu-id="eb8ff-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="eb8ff-108">_ulFlags_</span></span>
  
> <span data-ttu-id="eb8ff-109">[in] Máscara de bits de marcas que indica el formato de los tipos de direcciones devueltos.</span><span class="sxs-lookup"><span data-stu-id="eb8ff-109">[in] A bitmask of flags that indicates the format for the returned address types.</span></span> <span data-ttu-id="eb8ff-110">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="eb8ff-110">The following flag can be set:</span></span>
    
<span data-ttu-id="eb8ff-111">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="eb8ff-111">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="eb8ff-112">Los tipos de direcciones están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="eb8ff-112">The address types are in Unicode format.</span></span> <span data-ttu-id="eb8ff-113">Si la MAPI_UNICODE no está establecida, los tipos de direcciones están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="eb8ff-113">If the MAPI_UNICODE flag is not set, the address types are in ANSI format.</span></span>
    
 <span data-ttu-id="eb8ff-114">_lpcAdrTypes_</span><span class="sxs-lookup"><span data-stu-id="eb8ff-114">_lpcAdrTypes_</span></span>
  
> <span data-ttu-id="eb8ff-115">[salida] Puntero a un recuento de tipos de direcciones señalados por el _parámetro lpppszAdrTypes._</span><span class="sxs-lookup"><span data-stu-id="eb8ff-115">[out] A pointer to a count of address types pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
    
 <span data-ttu-id="eb8ff-116">_lpppszAdrTypes_</span><span class="sxs-lookup"><span data-stu-id="eb8ff-116">_lpppszAdrTypes_</span></span>
  
> <span data-ttu-id="eb8ff-117">[salida] Puntero a una matriz de punteros a tipos de direcciones.</span><span class="sxs-lookup"><span data-stu-id="eb8ff-117">[out] A pointer to an array of pointers to address types.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="eb8ff-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eb8ff-118">Return value</span></span>

<span data-ttu-id="eb8ff-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="eb8ff-119">S_OK</span></span> 
  
> <span data-ttu-id="eb8ff-120">Los tipos de direcciones se recuperaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="eb8ff-120">The address types were successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eb8ff-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eb8ff-121">Remarks</span></span>

<span data-ttu-id="eb8ff-122">El **método IMAPISession::EnumAdrTypes** devuelve una lista de los tipos de direcciones que pueden controlar todos los proveedores de transporte activo de la sesión.</span><span class="sxs-lookup"><span data-stu-id="eb8ff-122">The **IMAPISession::EnumAdrTypes** method returns a list of the address types that can be handled by all of the active transport providers in the session.</span></span> <span data-ttu-id="eb8ff-123">Los tipos de direcciones para los proveedores de transporte que no están cargados actualmente no se incluyen en la lista.</span><span class="sxs-lookup"><span data-stu-id="eb8ff-123">The address types for transport providers that are not currently loaded are not included in the list.</span></span> <span data-ttu-id="eb8ff-124">Los proveedores de transporte se registran para controlar uno o más tipos de direcciones cuando MAPI llama a su [método IXPLogon::AddressTypes.](ixplogon-addresstypes.md)</span><span class="sxs-lookup"><span data-stu-id="eb8ff-124">Transport providers register to handle one or more address types when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="eb8ff-125">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="eb8ff-125">Notes to callers</span></span>

<span data-ttu-id="eb8ff-126">Llama [a MAPIFreeBuffer para](mapifreebuffer.md) liberar la matriz de cadenas a la que apunta el parámetro _lpppszAdrTypes._</span><span class="sxs-lookup"><span data-stu-id="eb8ff-126">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the string array pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eb8ff-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb8ff-127">See also</span></span>



[<span data-ttu-id="eb8ff-128">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="eb8ff-128">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="eb8ff-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="eb8ff-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="eb8ff-130">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="eb8ff-130">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

