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
ms.openlocfilehash: 48ddb5a7c4e013c03138b08d9dadcdc0991faeec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438375"
---
# <a name="iablogoncompareentryids"></a><span data-ttu-id="e8f5f-103">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="e8f5f-103">IABLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="e8f5f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8f5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8f5f-105">Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="e8f5f-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="e8f5f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8f5f-106">Parameters</span></span>

 <span data-ttu-id="e8f5f-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="e8f5f-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="e8f5f-108">[entrada] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID1._</span><span class="sxs-lookup"><span data-stu-id="e8f5f-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="e8f5f-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="e8f5f-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="e8f5f-110">[entrada] Puntero al primer identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="e8f5f-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="e8f5f-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="e8f5f-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="e8f5f-112">[entrada] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID2._</span><span class="sxs-lookup"><span data-stu-id="e8f5f-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="e8f5f-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="e8f5f-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="e8f5f-114">[entrada] Puntero al segundo identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="e8f5f-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="e8f5f-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e8f5f-115">_ulFlags_</span></span>
  
> <span data-ttu-id="e8f5f-116">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e8f5f-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="e8f5f-117">_lpulRet_</span><span class="sxs-lookup"><span data-stu-id="e8f5f-117">_lpulRet_</span></span>
  
> <span data-ttu-id="e8f5f-118">[salida] Puntero al resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="e8f5f-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="e8f5f-119">TRUE para indicar que los dos identificadores de entrada hacen referencia al mismo objeto; de lo contrario, FALSE.</span><span class="sxs-lookup"><span data-stu-id="e8f5f-119">TRUE to indicate that the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e8f5f-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8f5f-120">Return value</span></span>

<span data-ttu-id="e8f5f-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="e8f5f-121">S_OK</span></span> 
  
> <span data-ttu-id="e8f5f-122">Los identificadores de entrada se compararon correctamente.</span><span class="sxs-lookup"><span data-stu-id="e8f5f-122">The entry identifiers were successfully compared.</span></span>
    
<span data-ttu-id="e8f5f-123">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e8f5f-123">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="e8f5f-124">Uno o ambos identificadores de entrada no pertenecen al proveedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="e8f5f-124">One or both of the entry identifiers do not belong to the address book provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e8f5f-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e8f5f-125">Remarks</span></span>

<span data-ttu-id="e8f5f-126">Los proveedores de libretas de direcciones implementan el método **CompareEntryIDs** para comparar dos identificadores de entrada para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="e8f5f-126">Address book providers implement the **CompareEntryIDs** method to compare two entry identifiers to determine whether they refer to the same object.</span></span> 
  
 <span data-ttu-id="e8f5f-127">**CompareEntryIDs** es útil porque un objeto puede tener más de un identificador de entrada válido; esta situación puede ocurrir, por ejemplo, cuando se compara un identificador de entrada a corto plazo con un identificador de entrada a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="e8f5f-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier; such a situation can occur, for example, when you compare a short-term entry identifier with a long-term entry identifier.</span></span> 
  
<span data-ttu-id="e8f5f-128">Para obtener más información acerca de cómo crear identificadores de entrada, vea [Identificadores de entrada MAPI](mapi-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="e8f5f-128">For more information about how to create entry identifiers, see [MAPI Entry Identifiers](mapi-entry-identifiers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e8f5f-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e8f5f-129">See also</span></span>



[<span data-ttu-id="e8f5f-130">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e8f5f-130">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

