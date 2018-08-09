---
title: IMSProviderCompareStoreIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.CompareStoreIDs
api_type:
- COM
ms.assetid: c3e3cfaa-9c4a-482a-9411-9c4ab01d312f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9905a4e972f0e599629aac74b6fbc8bae06c93b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817803"
---
# <a name="imsprovidercomparestoreids"></a><span data-ttu-id="53895-103">IMSProvider::CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="53895-103">IMSProvider::CompareStoreIDs</span></span>

  
  
<span data-ttu-id="53895-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="53895-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="53895-105">Compara dos mensajes almacén de los identificadores de entrada para determinar si hacen referencia al mismo objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="53895-105">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>
  
```cpp
HRESULT CompareStoreIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a><span data-ttu-id="53895-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53895-106">Parameters</span></span>

 <span data-ttu-id="53895-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="53895-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="53895-108">[entrada] El tamaño, en bytes, del identificador de entrada indicada por el parámetro _lpEntryID1_ _._</span><span class="sxs-lookup"><span data-stu-id="53895-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="53895-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="53895-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="53895-110">[entrada] Un puntero para el primer identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="53895-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="53895-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="53895-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="53895-112">[entrada] El tamaño, en bytes, del identificador de entrada indicada por el parámetro _lpEntryID2_ _._</span><span class="sxs-lookup"><span data-stu-id="53895-112">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="53895-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="53895-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="53895-114">[entrada] Un puntero para el segundo identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="53895-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="53895-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="53895-115">_ulFlags_</span></span>
  
> <span data-ttu-id="53895-116">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="53895-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="53895-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="53895-117">_lpulResult_</span></span>
  
> <span data-ttu-id="53895-118">[out] Un puntero al resultado devuelto de la comparación.</span><span class="sxs-lookup"><span data-stu-id="53895-118">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="53895-119">TRUE si los identificadores de dos entrada hacen referencia al mismo objeto; en caso contrario, es FALSE.</span><span class="sxs-lookup"><span data-stu-id="53895-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="53895-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53895-120">Return value</span></span>

<span data-ttu-id="53895-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="53895-121">S_OK</span></span> 
  
> <span data-ttu-id="53895-122">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="53895-122">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="53895-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="53895-123">Remarks</span></span>

<span data-ttu-id="53895-124">MAPI llama al método de **IMSProvider::CompareStoreIDs** cuando se procesa una llamada al método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) .</span><span class="sxs-lookup"><span data-stu-id="53895-124">MAPI calls the **IMSProvider::CompareStoreIDs** method when it processes a call to the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> <span data-ttu-id="53895-125">**CompareStoreIDs** se llama en este momento para determinar qué sección de perfil, si hay alguna, está asociado con el almacén de mensajes que se ha abierto.</span><span class="sxs-lookup"><span data-stu-id="53895-125">**CompareStoreIDs** is called at this point to determine which profile section, if any, is associated with the message store being opened.</span></span> <span data-ttu-id="53895-126">Puede realizar una llamada **CompareStoreIDs** cuando no hay almacenes de mensaje están abiertos para un proveedor de almacén determinado.</span><span class="sxs-lookup"><span data-stu-id="53895-126">A **CompareStoreIDs** call can be made when no message stores are open for a particular store provider.</span></span> <span data-ttu-id="53895-127">Además, también llamadas MAPI **CompareStoreIDs** cuando se procesa una llamada de proveedor de almacenamiento para el método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) .</span><span class="sxs-lookup"><span data-stu-id="53895-127">In addition, MAPI also calls **CompareStoreIDs** when it processes a store provider call to the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method.</span></span> 
  
<span data-ttu-id="53895-128">Los identificadores de entrada que se comparan por **CompareStoreIDs** son ambos para el actual almacenan la biblioteca de vínculos dinámicos (DLL) del proveedor y son ambos identificadores de entrada de almacén no ajustado.</span><span class="sxs-lookup"><span data-stu-id="53895-128">The entry identifiers compared by **CompareStoreIDs** are both for the current store provider's dynamic-link library (DLL) and are both unwrapped store entry identifiers.</span></span> <span data-ttu-id="53895-129">Para obtener más información acerca de los identificadores de almacén de entrada de ajuste, consulte [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).</span><span class="sxs-lookup"><span data-stu-id="53895-129">For more information about wrapping store entry identifiers, see [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).</span></span>
  
<span data-ttu-id="53895-130">Comparación de los identificadores de entrada es útil porque un objeto puede tener más de un identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="53895-130">Comparing entry identifiers is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="53895-131">Esto puede suceder, por ejemplo, después de instalar una nueva versión de un proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="53895-131">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="53895-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="53895-132">See also</span></span>



[<span data-ttu-id="53895-133">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="53895-133">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="53895-134">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="53895-134">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="53895-135">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="53895-135">IMAPISupport::WrapStoreEntryID</span></span>](imapisupport-wrapstoreentryid.md)
  
[<span data-ttu-id="53895-136">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="53895-136">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

