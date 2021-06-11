---
title: IMAPISessionCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.CompareEntryIDs
api_type:
- COM
ms.assetid: 319f10e9-db8d-4d16-aa1f-6cf5fef493eb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4dfde82aa843072168288f4e0b0084dfccd5cd2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427818"
---
# <a name="imapisessioncompareentryids"></a><span data-ttu-id="cd67e-103">IMAPISession::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="cd67e-103">IMAPISession::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="cd67e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd67e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd67e-105">Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="cd67e-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="cd67e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd67e-106">Parameters</span></span>

 <span data-ttu-id="cd67e-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="cd67e-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="cd67e-108">[in] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID1._</span><span class="sxs-lookup"><span data-stu-id="cd67e-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="cd67e-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="cd67e-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="cd67e-110">[in] Puntero al primer identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="cd67e-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="cd67e-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="cd67e-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="cd67e-112">[in] Número de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID2._</span><span class="sxs-lookup"><span data-stu-id="cd67e-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="cd67e-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="cd67e-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="cd67e-114">[in] Puntero al segundo identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="cd67e-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="cd67e-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cd67e-115">_ulFlags_</span></span>
  
> <span data-ttu-id="cd67e-116">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="cd67e-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="cd67e-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="cd67e-117">_lpulResult_</span></span>
  
> <span data-ttu-id="cd67e-118">[salida] Puntero al resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="cd67e-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="cd67e-119">TRUE si los dos identificadores de entrada hacen referencia al mismo objeto; en caso contrario, FALSE.</span><span class="sxs-lookup"><span data-stu-id="cd67e-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cd67e-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd67e-120">Return value</span></span>

<span data-ttu-id="cd67e-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd67e-121">S_OK</span></span> 
  
> <span data-ttu-id="cd67e-122">La comparación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="cd67e-122">The comparison was successful.</span></span>
    
<span data-ttu-id="cd67e-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="cd67e-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="cd67e-124">Uno o ambos identificadores de entrada especificados como parámetros no hacen referencia a objetos, posiblemente porque estos objetos están actualmente sin abrir y no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="cd67e-124">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because these objects are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cd67e-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cd67e-125">Remarks</span></span>

<span data-ttu-id="cd67e-126">El **método IMAPISession::CompareEntryIDs** compara dos identificadores de entrada que pertenecen a un único proveedor de servicios para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="cd67e-126">The **IMAPISession::CompareEntryIDs** method compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="cd67e-127">MAPI extrae la parte [MAPIUID](mapiuid.md) de los identificadores de entrada para determinar el proveedor de servicios responsable de los objetos y, a continuación, llama al método **CompareEntryIDs** del objeto de inicio de sesión para realizar la comparación.</span><span class="sxs-lookup"><span data-stu-id="cd67e-127">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects and then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="cd67e-128">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="cd67e-128">Notes to callers</span></span>

<span data-ttu-id="cd67e-129">El **método CompareEntryIDs** es útil porque un objeto puede tener más de un identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="cd67e-129">The **CompareEntryIDs** method is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="cd67e-130">Esta situación puede producirse, por ejemplo, después de instalar una nueva versión de un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="cd67e-130">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="cd67e-131">Si **CompareEntryIDs** devuelve un error, no realice ninguna acción en función del resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="cd67e-131">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="cd67e-132">En su lugar, tome el enfoque más conservador posible.</span><span class="sxs-lookup"><span data-stu-id="cd67e-132">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="cd67e-133">**CompareEntryIDs** puede producir un error si, por ejemplo, uno o ambos identificadores de entrada contienen un **MAPIUID no válido**.</span><span class="sxs-lookup"><span data-stu-id="cd67e-133">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cd67e-134">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="cd67e-134">MFCMAPI reference</span></span>

<span data-ttu-id="cd67e-135">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="cd67e-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cd67e-136">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="cd67e-136">**File**</span></span>|<span data-ttu-id="cd67e-137">**Función**</span><span class="sxs-lookup"><span data-stu-id="cd67e-137">**Function**</span></span>|<span data-ttu-id="cd67e-138">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="cd67e-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cd67e-139">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="cd67e-139">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="cd67e-140">CbaseDialog::OnCompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="cd67e-140">CbaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="cd67e-141">MFCMAPI usa el **método IMAPISession::CompareEntryIDs** para comparar dos identificadores de entrada que escribe un usuario.</span><span class="sxs-lookup"><span data-stu-id="cd67e-141">MFCMAPI uses the **IMAPISession::CompareEntryIDs** method to compare two entry IDs that a user enters.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cd67e-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd67e-142">See also</span></span>



[<span data-ttu-id="cd67e-143">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="cd67e-143">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="cd67e-144">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="cd67e-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="cd67e-145">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="cd67e-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

