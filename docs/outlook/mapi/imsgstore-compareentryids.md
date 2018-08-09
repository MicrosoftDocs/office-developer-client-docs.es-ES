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
ms.openlocfilehash: a1c5cdc67bc64f20dd8ba0a5e8682c5e2f97294f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817751"
---
# <a name="imsgstorecompareentryids"></a><span data-ttu-id="82f4f-103">IMsgStore::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="82f4f-103">IMsgStore::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="82f4f-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="82f4f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="82f4f-105">Compara dos identificadores de entrada para determinar si hacen referencia a la misma entrada en un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="82f4f-105">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span> <span data-ttu-id="82f4f-106">MAPI pasa esta llamada a un proveedor de servicio únicamente si los identificadores únicos (UID) en ambos identificadores de entrada que se va a comparar son resueltos por dicho proveedor.</span><span class="sxs-lookup"><span data-stu-id="82f4f-106">MAPI passes this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="82f4f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82f4f-107">Parameters</span></span>

 <span data-ttu-id="82f4f-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="82f4f-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="82f4f-109">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID1_ _._</span><span class="sxs-lookup"><span data-stu-id="82f4f-109">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="82f4f-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="82f4f-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="82f4f-111">[entrada] Un puntero para el primer identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="82f4f-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="82f4f-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="82f4f-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="82f4f-113">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID2_ _._</span><span class="sxs-lookup"><span data-stu-id="82f4f-113">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="82f4f-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="82f4f-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="82f4f-115">[entrada] Un puntero para el segundo identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="82f4f-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="82f4f-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="82f4f-116">_ulFlags_</span></span>
  
> <span data-ttu-id="82f4f-117">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="82f4f-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="82f4f-118">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="82f4f-118">_lpulResult_</span></span>
  
> <span data-ttu-id="82f4f-119">[out] Un puntero al resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="82f4f-119">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="82f4f-120">TRUE si los identificadores de dos entrada hacen referencia al mismo objeto; en caso contrario, es FALSE.</span><span class="sxs-lookup"><span data-stu-id="82f4f-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="82f4f-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82f4f-121">Return value</span></span>

<span data-ttu-id="82f4f-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="82f4f-122">S_OK</span></span> 
  
> <span data-ttu-id="82f4f-123">La comparación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="82f4f-123">The comparison was successful.</span></span>
    
<span data-ttu-id="82f4f-124">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="82f4f-124">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="82f4f-125">Uno o ambos de los identificadores de entrada especificados como parámetros no hacen referencia a objetos, posiblemente debido a que los objetos correspondientes están sin abrir y no está disponible en presentan.</span><span class="sxs-lookup"><span data-stu-id="82f4f-125">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because the corresponding objects are unopened and unavailable at present.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="82f4f-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="82f4f-126">Remarks</span></span>

<span data-ttu-id="82f4f-127">El método **IMsgStore::CompareEntryIDs** compara dos identificadores de entrada que pertenecen al almacén de mensajes para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="82f4f-127">The **IMsgStore::CompareEntryIDs** method compares two entry identifiers that belong to the message store to determine whether they refer to the same object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="82f4f-128">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="82f4f-128">Notes to callers</span></span>

 <span data-ttu-id="82f4f-129">**CompareEntryIDs** es útil porque un objeto puede tener más de un identificador de entrada válido (por ejemplo, después de instalar una nueva versión de un proveedor de almacén de mensajes).</span><span class="sxs-lookup"><span data-stu-id="82f4f-129">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier (for example, after a new version of a message store provider is installed).</span></span> 
  
<span data-ttu-id="82f4f-130">Si **CompareEntryIDs** devuelve un error, no realice ninguna acción en función del resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="82f4f-130">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="82f4f-131">En su lugar, tomar el enfoque más conservador posible.</span><span class="sxs-lookup"><span data-stu-id="82f4f-131">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="82f4f-132">**CompareEntryIDs** puede producirse un error si, por ejemplo, uno o ambos de los identificadores de entrada contiene un **MAPIUID**de no válido.</span><span class="sxs-lookup"><span data-stu-id="82f4f-132">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contains an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="82f4f-133">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="82f4f-133">MFCMAPI reference</span></span>

<span data-ttu-id="82f4f-134">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="82f4f-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="82f4f-135">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="82f4f-135">**File**</span></span>|<span data-ttu-id="82f4f-136">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="82f4f-136">**Function**</span></span>|<span data-ttu-id="82f4f-137">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="82f4f-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="82f4f-138">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="82f4f-138">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="82f4f-139">CBaseDialog::OnCompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="82f4f-139">CBaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="82f4f-140">MFCMAPI usa el método **IMsgStore::CompareEntryIDs** para comparar los identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="82f4f-140">MFCMAPI uses the **IMsgStore::CompareEntryIDs** method to compare entry IDs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="82f4f-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="82f4f-141">See also</span></span>



[<span data-ttu-id="82f4f-142">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="82f4f-142">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="82f4f-143">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="82f4f-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="82f4f-144">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="82f4f-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

