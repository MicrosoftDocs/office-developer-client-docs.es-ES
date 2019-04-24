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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338440"
---
# <a name="imapisessionenumadrtypes"></a><span data-ttu-id="a4ad4-103">IMAPISession::EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="a4ad4-103">IMAPISession::EnumAdrTypes</span></span>

  
  
<span data-ttu-id="a4ad4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4ad4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4ad4-105">En desuso.</span><span class="sxs-lookup"><span data-stu-id="a4ad4-105">Deprecated.</span></span> <span data-ttu-id="a4ad4-106">Devuelve los tipos de direcciones que pueden controlar todos los proveedores de transporte de la sesión.</span><span class="sxs-lookup"><span data-stu-id="a4ad4-106">Returns the address types that can be handled by all of the transport providers in the session.</span></span> 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a><span data-ttu-id="a4ad4-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="a4ad4-107">Parameters</span></span>

 <span data-ttu-id="a4ad4-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a4ad4-108">_ulFlags_</span></span>
  
> <span data-ttu-id="a4ad4-109">a Máscara de direcciones de marcadores que indica el formato de los tipos de dirección devueltos.</span><span class="sxs-lookup"><span data-stu-id="a4ad4-109">[in] A bitmask of flags that indicates the format for the returned address types.</span></span> <span data-ttu-id="a4ad4-110">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="a4ad4-110">The following flag can be set:</span></span>
    
<span data-ttu-id="a4ad4-111">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a4ad4-111">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a4ad4-112">Los tipos de dirección están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="a4ad4-112">The address types are in Unicode format.</span></span> <span data-ttu-id="a4ad4-113">Si no se establece la marca MAPI_UNICODE, los tipos de dirección están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="a4ad4-113">If the MAPI_UNICODE flag is not set, the address types are in ANSI format.</span></span>
    
 <span data-ttu-id="a4ad4-114">_lpcAdrTypes_</span><span class="sxs-lookup"><span data-stu-id="a4ad4-114">_lpcAdrTypes_</span></span>
  
> <span data-ttu-id="a4ad4-115">contempla Un puntero a un recuento de tipos de direcciones apuntado por el parámetro _lpppszAdrTypes_ .</span><span class="sxs-lookup"><span data-stu-id="a4ad4-115">[out] A pointer to a count of address types pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
    
 <span data-ttu-id="a4ad4-116">_lpppszAdrTypes_</span><span class="sxs-lookup"><span data-stu-id="a4ad4-116">_lpppszAdrTypes_</span></span>
  
> <span data-ttu-id="a4ad4-117">contempla Un puntero a una matriz de punteros a tipos de direcciones.</span><span class="sxs-lookup"><span data-stu-id="a4ad4-117">[out] A pointer to an array of pointers to address types.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a4ad4-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4ad4-118">Return value</span></span>

<span data-ttu-id="a4ad4-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="a4ad4-119">S_OK</span></span> 
  
> <span data-ttu-id="a4ad4-120">Los tipos de dirección se recuperaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="a4ad4-120">The address types were successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a4ad4-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a4ad4-121">Remarks</span></span>

<span data-ttu-id="a4ad4-122">El método **IMAPISession:: EnumAdrTypes** devuelve una lista de los tipos de direcciones que pueden controlar todos los proveedores de transporte activos en la sesión.</span><span class="sxs-lookup"><span data-stu-id="a4ad4-122">The **IMAPISession::EnumAdrTypes** method returns a list of the address types that can be handled by all of the active transport providers in the session.</span></span> <span data-ttu-id="a4ad4-123">Los tipos de dirección para los proveedores de transporte que no están cargados actualmente no se incluyen en la lista.</span><span class="sxs-lookup"><span data-stu-id="a4ad4-123">The address types for transport providers that are not currently loaded are not included in the list.</span></span> <span data-ttu-id="a4ad4-124">Los proveedores de transporte se registran para controlar uno o varios tipos de direcciones cuando MAPI llama a su método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="a4ad4-124">Transport providers register to handle one or more address types when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a4ad4-125">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="a4ad4-125">Notes to callers</span></span>

<span data-ttu-id="a4ad4-126">Llame a [MAPIFreeBuffer](mapifreebuffer.md) para liberar la matriz de cadenas señalada por el parámetro _lpppszAdrTypes_ .</span><span class="sxs-lookup"><span data-stu-id="a4ad4-126">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the string array pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a4ad4-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4ad4-127">See also</span></span>



[<span data-ttu-id="a4ad4-128">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="a4ad4-128">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="a4ad4-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a4ad4-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a4ad4-130">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a4ad4-130">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

