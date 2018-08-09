---
title: IMAPISupportCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CompareEntryIDs
api_type:
- COM
ms.assetid: be6991d9-6353-4838-bc6b-39de51a94d8d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c939189c2c8f7d3147c3146f55deac0e032ce9df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817490"
---
# <a name="imapisupportcompareentryids"></a><span data-ttu-id="9ec0d-103">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="9ec0d-103">IMAPISupport::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="9ec0d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9ec0d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9ec0d-105">Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="9ec0d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ec0d-106">Parameters</span></span>

 <span data-ttu-id="9ec0d-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="9ec0d-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="9ec0d-108">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="9ec0d-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="9ec0d-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="9ec0d-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="9ec0d-110">[entrada] Un puntero para el primer identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="9ec0d-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="9ec0d-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="9ec0d-112">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="9ec0d-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="9ec0d-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="9ec0d-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="9ec0d-114">[entrada] Un puntero para el segundo identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="9ec0d-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9ec0d-115">_ulFlags_</span></span>
  
> <span data-ttu-id="9ec0d-116">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="9ec0d-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="9ec0d-117">_lpulResult_</span></span>
  
> <span data-ttu-id="9ec0d-118">[out] Un puntero al resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="9ec0d-119">TRUE si los identificadores de dos entrada hacen referencia al mismo objeto; en caso contrario, es FALSE.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9ec0d-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ec0d-120">Return value</span></span>

<span data-ttu-id="9ec0d-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="9ec0d-121">S_OK</span></span> 
  
> <span data-ttu-id="9ec0d-122">La comparación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-122">The comparison was successful.</span></span>
    
<span data-ttu-id="9ec0d-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="9ec0d-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="9ec0d-124">Uno o ambos de los identificadores de entrada especificados como parámetros no hacen referencia a objetos válidos, posiblemente debido a que actualmente están abiertos y no está disponible.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-124">One or both of the entry identifiers specified as parameters do not refer to valid objects, possibly because they are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9ec0d-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9ec0d-125">Remarks</span></span>

<span data-ttu-id="9ec0d-126">El método **IMAPISupport::CompareEntryIDs** se implementa para dirección libreta de direcciones y el mensaje de proveedor compatibilidad con objetos de almacén.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-126">The **IMAPISupport::CompareEntryIDs** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="9ec0d-127">**CompareEntryIDs** compara dos identificadores de entrada que pertenecen a un proveedor de servicio único para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-127">**CompareEntryIDs** compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="9ec0d-128">MAPI extrae la parte [MAPIUID](mapiuid.md) de los identificadores de entrada para determinar el proveedor de servicio responsable de los objetos.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-128">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects.</span></span> <span data-ttu-id="9ec0d-129">MAPI, a continuación, llama a **CompareEntryIDs** (método) del objeto de su inicio de sesión para llevar a cabo la comparación.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-129">MAPI then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9ec0d-130">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="9ec0d-130">Notes to callers</span></span>

 <span data-ttu-id="9ec0d-131">**CompareEntryIDs** es útil porque un objeto puede tener más de un identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-131">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="9ec0d-132">Esta situación puede suceder, por ejemplo, después de instalar una nueva versión de un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-132">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="9ec0d-133">Si **CompareEntryIDs** devuelve un error, no realice ninguna acción en función del resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-133">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="9ec0d-134">En su lugar, tomar el enfoque más conservador posible.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-134">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="9ec0d-135">**CompareEntryIDs** puede producirse un error si, por ejemplo, uno o ambos de los identificadores de entrada contienen una estructura **MAPIUID** no válida.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-135">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9ec0d-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ec0d-136">See also</span></span>



[<span data-ttu-id="9ec0d-137">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="9ec0d-137">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="9ec0d-138">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9ec0d-138">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

