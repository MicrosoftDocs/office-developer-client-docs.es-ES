---
title: IABLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: cb4a38ff-2fdd-40ac-a613-12c3f11a1df9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 03256f2dec62d0228c4d5456dcd1b60f66b13ad2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817105"
---
# <a name="iablogoncompareentryids"></a><span data-ttu-id="708a5-103">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="708a5-103">IABLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="708a5-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="708a5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="708a5-105">Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="708a5-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span>
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulRet
);
```

## <a name="parameters"></a><span data-ttu-id="708a5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="708a5-106">Parameters</span></span>

 <span data-ttu-id="708a5-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="708a5-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="708a5-108">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="708a5-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="708a5-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="708a5-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="708a5-110">[entrada] Un puntero para el primer identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="708a5-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="708a5-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="708a5-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="708a5-112">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="708a5-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="708a5-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="708a5-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="708a5-114">[entrada] Un puntero para el segundo identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="708a5-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="708a5-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="708a5-115">_ulFlags_</span></span>
  
> <span data-ttu-id="708a5-116">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="708a5-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="708a5-117">_lpulRet_</span><span class="sxs-lookup"><span data-stu-id="708a5-117">_lpulRet_</span></span>
  
> <span data-ttu-id="708a5-118">[out] Un puntero al resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="708a5-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="708a5-119">TRUE para indicar que los identificadores de dos entrada hacen referencia al mismo objeto; en caso contrario, es FALSE.</span><span class="sxs-lookup"><span data-stu-id="708a5-119">TRUE to indicate that the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="708a5-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="708a5-120">Return value</span></span>

<span data-ttu-id="708a5-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="708a5-121">S_OK</span></span> 
  
> <span data-ttu-id="708a5-122">Los identificadores de entrada comparados correctamente.</span><span class="sxs-lookup"><span data-stu-id="708a5-122">The entry identifiers were successfully compared.</span></span>
    
<span data-ttu-id="708a5-123">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="708a5-123">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="708a5-124">Uno o ambos de los identificadores de entrada no pertenecen a la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="708a5-124">One or both of the entry identifiers do not belong to the address book provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="708a5-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="708a5-125">Remarks</span></span>

<span data-ttu-id="708a5-126">Los proveedores de la libreta de direcciones implementan el método **CompareEntryIDs** para comparar dos identificadores de entrada para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="708a5-126">Address book providers implement the **CompareEntryIDs** method to compare two entry identifiers to determine whether they refer to the same object.</span></span> 
  
 <span data-ttu-id="708a5-127">**CompareEntryIDs** es útil porque un objeto puede tener más de un identificador de entrada válido; Esta situación puede suceder, por ejemplo, cuando se compara un identificador de entrada a corto plazo con un identificador de entrada a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="708a5-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier; such a situation can occur, for example, when you compare a short-term entry identifier with a long-term entry identifier.</span></span> 
  
<span data-ttu-id="708a5-128">Para obtener más información acerca de cómo crear los identificadores de entrada, vea [Identificadores de entrada de MAPI](mapi-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="708a5-128">For more information about how to create entry identifiers, see [MAPI Entry Identifiers](mapi-entry-identifiers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="708a5-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="708a5-129">See also</span></span>



[<span data-ttu-id="708a5-130">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="708a5-130">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

