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
ms.openlocfilehash: 745c1b10cbbb24389cace7911d7c5fd37fe09472
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586854"
---
# <a name="imapisessioncompareentryids"></a><span data-ttu-id="dfcb6-103">IMAPISession::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="dfcb6-103">IMAPISession::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="dfcb6-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dfcb6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dfcb6-105">Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="dfcb6-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="dfcb6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dfcb6-106">Parameters</span></span>

 <span data-ttu-id="dfcb6-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="dfcb6-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="dfcb6-108">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="dfcb6-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="dfcb6-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="dfcb6-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="dfcb6-110">[entrada] Un puntero para el primer identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="dfcb6-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="dfcb6-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="dfcb6-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="dfcb6-112">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="dfcb6-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="dfcb6-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="dfcb6-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="dfcb6-114">[entrada] Un puntero para el segundo identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="dfcb6-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="dfcb6-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dfcb6-115">_ulFlags_</span></span>
  
> <span data-ttu-id="dfcb6-116">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="dfcb6-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="dfcb6-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="dfcb6-117">_lpulResult_</span></span>
  
> <span data-ttu-id="dfcb6-118">[out] Un puntero al resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="dfcb6-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="dfcb6-119">TRUE si los identificadores de dos entrada hacen referencia al mismo objeto; en caso contrario, es FALSE.</span><span class="sxs-lookup"><span data-stu-id="dfcb6-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dfcb6-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dfcb6-120">Return value</span></span>

<span data-ttu-id="dfcb6-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="dfcb6-121">S_OK</span></span> 
  
> <span data-ttu-id="dfcb6-122">La comparación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="dfcb6-122">The comparison was successful.</span></span>
    
<span data-ttu-id="dfcb6-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="dfcb6-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="dfcb6-124">Uno o ambos de los identificadores de entrada especificados como parámetros no hacen referencia a objetos, posiblemente debido a que estos objetos están actualmente sin abrir y no está disponible.</span><span class="sxs-lookup"><span data-stu-id="dfcb6-124">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because these objects are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dfcb6-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dfcb6-125">Remarks</span></span>

<span data-ttu-id="dfcb6-126">El método **IMAPISession::CompareEntryIDs** compara dos identificadores de entrada que pertenecen a un proveedor de servicio único para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="dfcb6-126">The **IMAPISession::CompareEntryIDs** method compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="dfcb6-127">MAPI extrae la parte [MAPIUID](mapiuid.md) de los identificadores de entrada para determinar el proveedor de servicio responsable de los objetos y, a continuación, llama a **CompareEntryIDs** (método) del objeto de su inicio de sesión para llevar a cabo la comparación.</span><span class="sxs-lookup"><span data-stu-id="dfcb6-127">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects and then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="dfcb6-128">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="dfcb6-128">Notes to callers</span></span>

<span data-ttu-id="dfcb6-129">El método **CompareEntryIDs** es útil porque un objeto puede tener más de un identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="dfcb6-129">The **CompareEntryIDs** method is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="dfcb6-130">Esta situación puede suceder, por ejemplo, después de instalar una nueva versión de un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="dfcb6-130">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="dfcb6-131">Si **CompareEntryIDs** devuelve un error, no realice ninguna acción en función del resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="dfcb6-131">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="dfcb6-132">En su lugar, tomar el enfoque más conservador posible.</span><span class="sxs-lookup"><span data-stu-id="dfcb6-132">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="dfcb6-133">**CompareEntryIDs** puede producirse un error si, por ejemplo, uno o ambos de los identificadores de entrada contienen un **MAPIUID**de no válido.</span><span class="sxs-lookup"><span data-stu-id="dfcb6-133">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="dfcb6-134">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="dfcb6-134">MFCMAPI reference</span></span>

<span data-ttu-id="dfcb6-135">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="dfcb6-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dfcb6-136">**File**</span><span class="sxs-lookup"><span data-stu-id="dfcb6-136">**File**</span></span>|<span data-ttu-id="dfcb6-137">**Función**</span><span class="sxs-lookup"><span data-stu-id="dfcb6-137">**Function**</span></span>|<span data-ttu-id="dfcb6-138">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="dfcb6-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dfcb6-139">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="dfcb6-139">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="dfcb6-140">CbaseDialog::OnCompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="dfcb6-140">CbaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="dfcb6-141">MFCMAPI usa el método **IMAPISession::CompareEntryIDs** para comparar dos identificadores de entrada que un usuario escribe.</span><span class="sxs-lookup"><span data-stu-id="dfcb6-141">MFCMAPI uses the **IMAPISession::CompareEntryIDs** method to compare two entry IDs that a user enters.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dfcb6-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="dfcb6-142">See also</span></span>



[<span data-ttu-id="dfcb6-143">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="dfcb6-143">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="dfcb6-144">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="dfcb6-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="dfcb6-145">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="dfcb6-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

