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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279611"
---
# <a name="iablogoncompareentryids"></a><span data-ttu-id="4e081-103">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="4e081-103">IABLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="4e081-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e081-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e081-105">Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="4e081-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="4e081-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="4e081-106">Parameters</span></span>

 <span data-ttu-id="4e081-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="4e081-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="4e081-108">a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="4e081-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="4e081-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="4e081-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="4e081-110">a Puntero al primer identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="4e081-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="4e081-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="4e081-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="4e081-112">a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="4e081-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="4e081-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="4e081-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="4e081-114">a Puntero al segundo identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="4e081-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="4e081-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4e081-115">_ulFlags_</span></span>
  
> <span data-ttu-id="4e081-116">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="4e081-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="4e081-117">_lpulRet_</span><span class="sxs-lookup"><span data-stu-id="4e081-117">_lpulRet_</span></span>
  
> <span data-ttu-id="4e081-118">contempla Un puntero al resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="4e081-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="4e081-119">TRUE para indicar que los dos identificadores de entrada hacen referencia al mismo objeto; de lo contrario, FALSE.</span><span class="sxs-lookup"><span data-stu-id="4e081-119">TRUE to indicate that the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4e081-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e081-120">Return value</span></span>

<span data-ttu-id="4e081-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="4e081-121">S_OK</span></span> 
  
> <span data-ttu-id="4e081-122">Los identificadores de entrada se comparó correctamente.</span><span class="sxs-lookup"><span data-stu-id="4e081-122">The entry identifiers were successfully compared.</span></span>
    
<span data-ttu-id="4e081-123">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4e081-123">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="4e081-124">Uno o ambos de los identificadores de entrada no pertenecen al proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="4e081-124">One or both of the entry identifiers do not belong to the address book provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4e081-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4e081-125">Remarks</span></span>

<span data-ttu-id="4e081-126">Los proveedores de la libreta de direcciones implementan el método **CompareEntryIDs** para comparar dos identificadores de entrada para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="4e081-126">Address book providers implement the **CompareEntryIDs** method to compare two entry identifiers to determine whether they refer to the same object.</span></span> 
  
 <span data-ttu-id="4e081-127">**CompareEntryIDs** es útil porque un objeto puede tener más de un identificador de entrada válido; una situación de este tipo puede ocurrir, por ejemplo, cuando se compara un identificador de entrada a corto plazo con un identificador de entrada a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="4e081-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier; such a situation can occur, for example, when you compare a short-term entry identifier with a long-term entry identifier.</span></span> 
  
<span data-ttu-id="4e081-128">Para obtener más información acerca de cómo crear identificadores de entrada, consulte identificadores de [entrada MAPI](mapi-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="4e081-128">For more information about how to create entry identifiers, see [MAPI Entry Identifiers](mapi-entry-identifiers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4e081-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e081-129">See also</span></span>



[<span data-ttu-id="4e081-130">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4e081-130">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

