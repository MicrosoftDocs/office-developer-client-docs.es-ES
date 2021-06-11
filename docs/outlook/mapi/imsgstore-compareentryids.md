---
title: IMsgStoreCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.CompareEntryIDs
api_type:
- COM
ms.assetid: 33d70748-0d3f-4be4-bcb5-7ec048887944
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2a2439bae79b497f018391983e2c4b03a35eee70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424255"
---
# <a name="imsgstorecompareentryids"></a><span data-ttu-id="93fd2-103">IMsgStore::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="93fd2-103">IMsgStore::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="93fd2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93fd2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93fd2-105">Compara dos identificadores de entrada para determinar si hacen referencia a la misma entrada en un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="93fd2-105">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span> <span data-ttu-id="93fd2-106">MAPI pasa esta llamada a un proveedor de servicios solo si ese proveedor controla los identificadores únicos (UID) de ambos identificadores de entrada que se van a comparar.</span><span class="sxs-lookup"><span data-stu-id="93fd2-106">MAPI passes this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="93fd2-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="93fd2-107">Parameters</span></span>

 <span data-ttu-id="93fd2-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="93fd2-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="93fd2-109">[in] Recuento de bytes en el identificador de entrada al que apunta el  _parámetro lpEntryID1_  _._</span><span class="sxs-lookup"><span data-stu-id="93fd2-109">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="93fd2-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="93fd2-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="93fd2-111">[in] Puntero al primer identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="93fd2-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="93fd2-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="93fd2-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="93fd2-113">[in] Recuento de bytes en el identificador de entrada señalado por el  _parámetro lpEntryID2_  _._</span><span class="sxs-lookup"><span data-stu-id="93fd2-113">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="93fd2-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="93fd2-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="93fd2-115">[in] Puntero al segundo identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="93fd2-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="93fd2-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="93fd2-116">_ulFlags_</span></span>
  
> <span data-ttu-id="93fd2-117">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="93fd2-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="93fd2-118">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="93fd2-118">_lpulResult_</span></span>
  
> <span data-ttu-id="93fd2-119">[salida] Puntero al resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="93fd2-119">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="93fd2-120">TRUE si los dos identificadores de entrada hacen referencia al mismo objeto; en caso contrario, FALSE.</span><span class="sxs-lookup"><span data-stu-id="93fd2-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="93fd2-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="93fd2-121">Return value</span></span>

<span data-ttu-id="93fd2-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="93fd2-122">S_OK</span></span> 
  
> <span data-ttu-id="93fd2-123">La comparación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="93fd2-123">The comparison was successful.</span></span>
    
<span data-ttu-id="93fd2-124">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="93fd2-124">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="93fd2-125">Uno o ambos identificadores de entrada especificados como parámetros no hacen referencia a objetos, posiblemente porque los objetos correspondientes no están abiertos y no están disponibles actualmente.</span><span class="sxs-lookup"><span data-stu-id="93fd2-125">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because the corresponding objects are unopened and unavailable at present.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="93fd2-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="93fd2-126">Remarks</span></span>

<span data-ttu-id="93fd2-127">El **método IMsgStore::CompareEntryIDs** compara dos identificadores de entrada que pertenecen al almacén de mensajes para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="93fd2-127">The **IMsgStore::CompareEntryIDs** method compares two entry identifiers that belong to the message store to determine whether they refer to the same object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="93fd2-128">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="93fd2-128">Notes to callers</span></span>

 <span data-ttu-id="93fd2-129">**CompareEntryIDs** es útil porque un objeto puede tener más de un identificador de entrada válido (por ejemplo, después de instalar una nueva versión de un proveedor de almacén de mensajes).</span><span class="sxs-lookup"><span data-stu-id="93fd2-129">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier (for example, after a new version of a message store provider is installed).</span></span> 
  
<span data-ttu-id="93fd2-130">Si **CompareEntryIDs** devuelve un error, no realice ninguna acción en función del resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="93fd2-130">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="93fd2-131">En su lugar, tome el enfoque más conservador posible.</span><span class="sxs-lookup"><span data-stu-id="93fd2-131">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="93fd2-132">**CompareEntryIDs** puede producir un error si, por ejemplo, uno o ambos identificadores de entrada contienen un **MAPIUID no válido.**</span><span class="sxs-lookup"><span data-stu-id="93fd2-132">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contains an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="93fd2-133">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="93fd2-133">MFCMAPI reference</span></span>

<span data-ttu-id="93fd2-134">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="93fd2-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="93fd2-135">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="93fd2-135">**File**</span></span>|<span data-ttu-id="93fd2-136">**Función**</span><span class="sxs-lookup"><span data-stu-id="93fd2-136">**Function**</span></span>|<span data-ttu-id="93fd2-137">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="93fd2-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="93fd2-138">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="93fd2-138">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="93fd2-139">CBaseDialog::OnCompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="93fd2-139">CBaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="93fd2-140">MFCMAPI usa el **método IMsgStore::CompareEntryIDs** para comparar los identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="93fd2-140">MFCMAPI uses the **IMsgStore::CompareEntryIDs** method to compare entry IDs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="93fd2-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="93fd2-141">See also</span></span>



[<span data-ttu-id="93fd2-142">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="93fd2-142">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="93fd2-143">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="93fd2-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="93fd2-144">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="93fd2-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

