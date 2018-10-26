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
ms.openlocfilehash: 050068b542616d1ad4d133b289aba46db2888519
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587820"
---
# <a name="imapisessionenumadrtypes"></a><span data-ttu-id="2fbe4-103">IMAPISession::EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="2fbe4-103">IMAPISession::EnumAdrTypes</span></span>

  
  
<span data-ttu-id="2fbe4-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2fbe4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2fbe4-105">En desuso.</span><span class="sxs-lookup"><span data-stu-id="2fbe4-105">Deprecated.</span></span> <span data-ttu-id="2fbe4-106">Devuelve los tipos de direcciones que se pueden controlar por todos los proveedores de transporte en la sesión.</span><span class="sxs-lookup"><span data-stu-id="2fbe4-106">Returns the address types that can be handled by all of the transport providers in the session.</span></span> 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a><span data-ttu-id="2fbe4-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="2fbe4-107">Parameters</span></span>

 <span data-ttu-id="2fbe4-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2fbe4-108">_ulFlags_</span></span>
  
> <span data-ttu-id="2fbe4-109">[entrada] Una máscara de bits de marcadores que indica el formato para los tipos de dirección devuelta.</span><span class="sxs-lookup"><span data-stu-id="2fbe4-109">[in] A bitmask of flags that indicates the format for the returned address types.</span></span> <span data-ttu-id="2fbe4-110">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="2fbe4-110">The following flag can be set:</span></span>
    
<span data-ttu-id="2fbe4-111">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2fbe4-111">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2fbe4-112">Los tipos de direcciones están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="2fbe4-112">The address types are in Unicode format.</span></span> <span data-ttu-id="2fbe4-113">Si no está establecido el indicador MAPI_UNICODE., los tipos de direcciones están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="2fbe4-113">If the MAPI_UNICODE flag is not set, the address types are in ANSI format.</span></span>
    
 <span data-ttu-id="2fbe4-114">_lpcAdrTypes_</span><span class="sxs-lookup"><span data-stu-id="2fbe4-114">_lpcAdrTypes_</span></span>
  
> <span data-ttu-id="2fbe4-115">[out] Un puntero a un recuento de los tipos de dirección indicada por el parámetro _lpppszAdrTypes_ .</span><span class="sxs-lookup"><span data-stu-id="2fbe4-115">[out] A pointer to a count of address types pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
    
 <span data-ttu-id="2fbe4-116">_lpppszAdrTypes_</span><span class="sxs-lookup"><span data-stu-id="2fbe4-116">_lpppszAdrTypes_</span></span>
  
> <span data-ttu-id="2fbe4-117">[out] Un puntero a una matriz de punteros a tipos de direcciones.</span><span class="sxs-lookup"><span data-stu-id="2fbe4-117">[out] A pointer to an array of pointers to address types.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2fbe4-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2fbe4-118">Return value</span></span>

<span data-ttu-id="2fbe4-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="2fbe4-119">S_OK</span></span> 
  
> <span data-ttu-id="2fbe4-120">Los tipos de direcciones se recuperaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="2fbe4-120">The address types were successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2fbe4-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2fbe4-121">Remarks</span></span>

<span data-ttu-id="2fbe4-122">El método **IMAPISession:: EnumAdrTypes** devuelve una lista de los tipos de direcciones que se pueden controlar por todos los proveedores de transporte activo en la sesión.</span><span class="sxs-lookup"><span data-stu-id="2fbe4-122">The **IMAPISession::EnumAdrTypes** method returns a list of the address types that can be handled by all of the active transport providers in the session.</span></span> <span data-ttu-id="2fbe4-123">No se incluyen los tipos de direcciones para los proveedores de transporte que no están cargados actualmente en la lista.</span><span class="sxs-lookup"><span data-stu-id="2fbe4-123">The address types for transport providers that are not currently loaded are not included in the list.</span></span> <span data-ttu-id="2fbe4-124">Registrar los proveedores de transporte para controlar uno o varios tipos de direcciones cuando MAPI llama a su método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="2fbe4-124">Transport providers register to handle one or more address types when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2fbe4-125">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="2fbe4-125">Notes to callers</span></span>

<span data-ttu-id="2fbe4-126">Llamar a [MAPIFreeBuffer](mapifreebuffer.md) para liberar la matriz de cadena indicada por el parámetro _lpppszAdrTypes_ .</span><span class="sxs-lookup"><span data-stu-id="2fbe4-126">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the string array pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2fbe4-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="2fbe4-127">See also</span></span>



[<span data-ttu-id="2fbe4-128">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="2fbe4-128">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="2fbe4-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="2fbe4-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="2fbe4-130">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="2fbe4-130">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

