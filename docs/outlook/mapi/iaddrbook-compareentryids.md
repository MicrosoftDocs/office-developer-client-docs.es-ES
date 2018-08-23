---
title: IAddrBookCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBookCompareEntryIDs
api_type:
- COM
ms.assetid: 7dabc1d3-5ea4-482f-91a9-9ef3009eddd2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d6f983e49132e7ab6ea402a8e32bb5ec56d1efba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564853"
---
# <a name="iaddrbookcompareentryids"></a><span data-ttu-id="cfdd2-103">IAddrBook::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="cfdd2-103">IAddrBook::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="cfdd2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cfdd2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cfdd2-105">Compara dos identificadores de entrada que pertenecen a un proveedor de libreta de direcciones concreto para determinar si hacen referencia al mismo objeto de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="cfdd2-105">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span> 
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a><span data-ttu-id="cfdd2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cfdd2-106">Parameters</span></span>

 <span data-ttu-id="cfdd2-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="cfdd2-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="cfdd2-108">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="cfdd2-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="cfdd2-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="cfdd2-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="cfdd2-110">[entrada] Un puntero para el primer identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="cfdd2-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="cfdd2-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="cfdd2-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="cfdd2-112">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="cfdd2-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="cfdd2-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="cfdd2-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="cfdd2-114">[entrada] Un puntero para el segundo identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="cfdd2-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="cfdd2-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cfdd2-115">_ulFlags_</span></span>
  
> <span data-ttu-id="cfdd2-116">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="cfdd2-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="cfdd2-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="cfdd2-117">_lpulResult_</span></span>
  
> <span data-ttu-id="cfdd2-118">[out] Un puntero al resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="cfdd2-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="cfdd2-119">El contenido de _lpulResult_ está establecido en TRUE si los identificadores de dos entrada hacen referencia al mismo objeto; de lo contrario, el contenido se establece en FALSE.</span><span class="sxs-lookup"><span data-stu-id="cfdd2-119">The contents of  _lpulResult_ are set to TRUE if the two entry identifiers refer to the same object; otherwise, the contents are set to FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cfdd2-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cfdd2-120">Return value</span></span>

<span data-ttu-id="cfdd2-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="cfdd2-121">S_OK</span></span> 
  
> <span data-ttu-id="cfdd2-122">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="cfdd2-122">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="cfdd2-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="cfdd2-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="cfdd2-124">Cualquier proveedor de la libreta de direcciones no reconoce uno o ambos de los identificadores de entrada pasados con los parámetros _lpEntryID1_ o _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="cfdd2-124">One or both of the entry identifiers passed in with the  _lpEntryID1_ or  _lpEntryID2_ parameters are not recognized by any address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cfdd2-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cfdd2-125">Remarks</span></span>

<span data-ttu-id="cfdd2-126">Las aplicaciones cliente y proveedores llamada de servicio **CompareEntryIDs** (método) para comparar dos identificadores de entrada que pertenece a un proveedor de libreta de direcciones único para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="cfdd2-126">Client applications and service providers call the **CompareEntryIDs** method to compare two entry identifiers that belongs to a single address book provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="cfdd2-127">**CompareEntryIDs** es útil porque un objeto puede tener más de un identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="cfdd2-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="cfdd2-128">Esta situación puede suceder, por ejemplo, después de instalar una nueva versión de un proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="cfdd2-128">This situation can occur, for example, after a new version of an address book provider is installed.</span></span> 
  
<span data-ttu-id="cfdd2-129">MAPI pasa esta llamada a la libreta de direcciones que se encarga de los identificadores de entrada, determinar el proveedor adecuado de forma que coincidan con la estructura [MAPIUID](mapiuid.md) en los identificadores de entrada con la estructura **MAPIUID** registrada por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="cfdd2-129">MAPI passes this call to the address book provider that is responsible for the entry identifiers, determining the appropriate provider by matching the [MAPIUID](mapiuid.md) structure in the entry identifiers with the **MAPIUID** structure registered by the provider.</span></span> 
  
<span data-ttu-id="cfdd2-130">Si los identificadores de dos entrada hacer referencia al mismo objeto, **CompareEntryIDs** establece el contenido del parámetro _lpulResult_ en TRUE; Si hacen referencia a objetos diferentes, **CompareEntryIDs** establece el contenido en FALSE.</span><span class="sxs-lookup"><span data-stu-id="cfdd2-130">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the contents of the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets the contents to FALSE.</span></span> <span data-ttu-id="cfdd2-131">En cualquier caso, **CompareEntryIDs** devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="cfdd2-131">In either case, **CompareEntryIDs** returns S_OK.</span></span> <span data-ttu-id="cfdd2-132">Si **CompareEntryIDs** devuelve un error, lo que puede ocurrir si ningún proveedor de libreta de direcciones ha registrado una estructura **MAPIUID** que coincida con el de los identificadores de entrada, los clientes y proveedores no deben realizar ninguna acción en función del resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="cfdd2-132">If **CompareEntryIDs** returns an error, which can occur if no address book provider has registered a **MAPIUID** structure that matches the one in the entry identifiers, clients and providers should not take any action based on the result of the comparison.</span></span> <span data-ttu-id="cfdd2-133">En su lugar, que deben seguir el enfoque más conservador para la acción que se lleva a cabo.</span><span class="sxs-lookup"><span data-stu-id="cfdd2-133">They should instead take the most conservative approach to the action being performed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cfdd2-134">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="cfdd2-134">See also</span></span>



[<span data-ttu-id="cfdd2-135">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="cfdd2-135">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

