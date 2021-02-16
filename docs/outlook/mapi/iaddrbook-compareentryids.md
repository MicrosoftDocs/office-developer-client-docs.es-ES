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
ms.openlocfilehash: b6abecc298df7a86afff9338752a15615c73b3a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424262"
---
# <a name="iaddrbookcompareentryids"></a><span data-ttu-id="cbcce-103">IAddrBook::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="cbcce-103">IAddrBook::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="cbcce-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cbcce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cbcce-105">Compara dos identificadores de entrada que pertenecen a un proveedor de libreta de direcciones determinado para determinar si hacen referencia al mismo objeto de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="cbcce-105">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="cbcce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cbcce-106">Parameters</span></span>

 <span data-ttu-id="cbcce-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="cbcce-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="cbcce-108">[entrada] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID1._</span><span class="sxs-lookup"><span data-stu-id="cbcce-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="cbcce-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="cbcce-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="cbcce-110">[entrada] Puntero al primer identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="cbcce-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="cbcce-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="cbcce-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="cbcce-112">[entrada] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID2._</span><span class="sxs-lookup"><span data-stu-id="cbcce-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="cbcce-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="cbcce-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="cbcce-114">[entrada] Puntero al segundo identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="cbcce-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="cbcce-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cbcce-115">_ulFlags_</span></span>
  
> <span data-ttu-id="cbcce-116">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="cbcce-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="cbcce-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="cbcce-117">_lpulResult_</span></span>
  
> <span data-ttu-id="cbcce-118">[salida] Puntero al resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="cbcce-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="cbcce-119">El contenido de  _lpulResult_ se establece en TRUE si los dos identificadores de entrada hacen referencia al mismo objeto; de lo contrario, el contenido se establece en FALSE.</span><span class="sxs-lookup"><span data-stu-id="cbcce-119">The contents of  _lpulResult_ are set to TRUE if the two entry identifiers refer to the same object; otherwise, the contents are set to FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cbcce-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cbcce-120">Return value</span></span>

<span data-ttu-id="cbcce-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="cbcce-121">S_OK</span></span> 
  
> <span data-ttu-id="cbcce-122">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="cbcce-122">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="cbcce-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="cbcce-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="cbcce-124">Uno o ambos identificadores de entrada pasados con los parámetros  _lpEntryID1_ o  _lpEntryID2_ no son reconocidos por ningún proveedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="cbcce-124">One or both of the entry identifiers passed in with the  _lpEntryID1_ or  _lpEntryID2_ parameters are not recognized by any address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cbcce-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cbcce-125">Remarks</span></span>

<span data-ttu-id="cbcce-126">Las aplicaciones cliente y los proveedores de servicios llaman al método **CompareEntryIDs** para comparar dos identificadores de entrada que pertenecen a un único proveedor de libreta de direcciones para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="cbcce-126">Client applications and service providers call the **CompareEntryIDs** method to compare two entry identifiers that belongs to a single address book provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="cbcce-127">**CompareEntryIDs** es útil porque un objeto puede tener más de un identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="cbcce-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="cbcce-128">Esta situación puede producirse, por ejemplo, después de instalar una nueva versión de un proveedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="cbcce-128">This situation can occur, for example, after a new version of an address book provider is installed.</span></span> 
  
<span data-ttu-id="cbcce-129">MAPI pasa esta llamada al proveedor de libreta de direcciones responsable de los identificadores de entrada, determinando el proveedor adecuado al hacer coincidir la estructura [MAPIUID](mapiuid.md) en los identificadores de entrada con la estructura **MAPIUID** registrada por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="cbcce-129">MAPI passes this call to the address book provider that is responsible for the entry identifiers, determining the appropriate provider by matching the [MAPIUID](mapiuid.md) structure in the entry identifiers with the **MAPIUID** structure registered by the provider.</span></span> 
  
<span data-ttu-id="cbcce-130">Si los dos identificadores de entrada hacen referencia al mismo objeto, **CompareEntryIDs** establece el contenido del parámetro  _lpulResult_ en TRUE; si hacen referencia a diferentes objetos, **CompareEntryIDs** establece el contenido en FALSE.</span><span class="sxs-lookup"><span data-stu-id="cbcce-130">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the contents of the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets the contents to FALSE.</span></span> <span data-ttu-id="cbcce-131">En cualquier caso, **CompareEntryIDs** devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="cbcce-131">In either case, **CompareEntryIDs** returns S_OK.</span></span> <span data-ttu-id="cbcce-132">Si **CompareEntryIDs** devuelve un error, que puede producirse si ningún proveedor de libreta de direcciones ha registrado una estructura **MAPIUID** que coincida con la de los identificadores de entrada, los clientes y proveedores no deben realizar ninguna acción en función del resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="cbcce-132">If **CompareEntryIDs** returns an error, which can occur if no address book provider has registered a **MAPIUID** structure that matches the one in the entry identifiers, clients and providers should not take any action based on the result of the comparison.</span></span> <span data-ttu-id="cbcce-133">En su lugar, deben tomar el enfoque más conservador de la acción que se está realizando.</span><span class="sxs-lookup"><span data-stu-id="cbcce-133">They should instead take the most conservative approach to the action being performed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cbcce-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cbcce-134">See also</span></span>



[<span data-ttu-id="cbcce-135">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="cbcce-135">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

