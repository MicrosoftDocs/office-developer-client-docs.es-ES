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
ms.openlocfilehash: 6c79943792c8c17ee007c39b5c5c215a6fbc0699
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431046"
---
# <a name="imapisupportcompareentryids"></a><span data-ttu-id="3bae8-103">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="3bae8-103">IMAPISupport::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="3bae8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3bae8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3bae8-105">Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="3bae8-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="3bae8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3bae8-106">Parameters</span></span>

 <span data-ttu-id="3bae8-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="3bae8-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="3bae8-108">[entrada] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID1._</span><span class="sxs-lookup"><span data-stu-id="3bae8-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="3bae8-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="3bae8-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="3bae8-110">[entrada] Puntero al primer identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="3bae8-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="3bae8-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="3bae8-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="3bae8-112">[entrada] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID2._</span><span class="sxs-lookup"><span data-stu-id="3bae8-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="3bae8-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="3bae8-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="3bae8-114">[entrada] Puntero al segundo identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="3bae8-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="3bae8-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3bae8-115">_ulFlags_</span></span>
  
> <span data-ttu-id="3bae8-116">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="3bae8-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="3bae8-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="3bae8-117">_lpulResult_</span></span>
  
> <span data-ttu-id="3bae8-118">[salida] Puntero al resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="3bae8-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="3bae8-119">TRUE si los dos identificadores de entrada hacen referencia al mismo objeto; de lo contrario, FALSE.</span><span class="sxs-lookup"><span data-stu-id="3bae8-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3bae8-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3bae8-120">Return value</span></span>

<span data-ttu-id="3bae8-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="3bae8-121">S_OK</span></span> 
  
> <span data-ttu-id="3bae8-122">La comparación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="3bae8-122">The comparison was successful.</span></span>
    
<span data-ttu-id="3bae8-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="3bae8-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="3bae8-124">Uno o ambos identificadores de entrada especificados como parámetros no hacen referencia a objetos válidos, posiblemente porque actualmente están sin abrir y no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="3bae8-124">One or both of the entry identifiers specified as parameters do not refer to valid objects, possibly because they are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3bae8-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3bae8-125">Remarks</span></span>

<span data-ttu-id="3bae8-126">El **método IMAPISupport::CompareEntryIDs** se implementa para objetos de compatibilidad con la libreta de direcciones y el proveedor del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="3bae8-126">The **IMAPISupport::CompareEntryIDs** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="3bae8-127">**CompareEntryIDs** compara dos identificadores de entrada que pertenecen a un único proveedor de servicios para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="3bae8-127">**CompareEntryIDs** compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="3bae8-128">MAPI extrae la [parte MAPIUID](mapiuid.md) de los identificadores de entrada para determinar el proveedor de servicios responsable de los objetos.</span><span class="sxs-lookup"><span data-stu-id="3bae8-128">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects.</span></span> <span data-ttu-id="3bae8-129">A continuación, MAPI llama al método **CompareEntryIDs** del objeto de inicio de sesión para realizar la comparación.</span><span class="sxs-lookup"><span data-stu-id="3bae8-129">MAPI then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3bae8-130">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="3bae8-130">Notes to callers</span></span>

 <span data-ttu-id="3bae8-131">**CompareEntryIDs** es útil porque un objeto puede tener más de un identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="3bae8-131">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="3bae8-132">Esta situación puede producirse, por ejemplo, después de instalar una nueva versión de un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="3bae8-132">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="3bae8-133">Si **CompareEntryIDs** devuelve un error, no realice ninguna acción basada en el resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="3bae8-133">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="3bae8-134">En su lugar, toma el enfoque más conservador posible.</span><span class="sxs-lookup"><span data-stu-id="3bae8-134">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="3bae8-135">**CompareEntryIDs** puede producir un error si, por ejemplo, uno o ambos identificadores de entrada contienen una estructura **MAPIUID no** válida.</span><span class="sxs-lookup"><span data-stu-id="3bae8-135">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3bae8-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3bae8-136">See also</span></span>



[<span data-ttu-id="3bae8-137">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="3bae8-137">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="3bae8-138">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="3bae8-138">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

