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
ms.openlocfilehash: 734e53c1e897c902c72319aa6f2d3d7af2d23fb6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431711"
---
# <a name="imsprovidercomparestoreids"></a><span data-ttu-id="b397f-103">IMSProvider::CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="b397f-103">IMSProvider::CompareStoreIDs</span></span>

  
  
<span data-ttu-id="b397f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b397f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b397f-105">Compara dos identificadores de entrada del almacén de mensajes para determinar si hacen referencia al mismo objeto de almacén.</span><span class="sxs-lookup"><span data-stu-id="b397f-105">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="b397f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="b397f-106">Parameters</span></span>

 <span data-ttu-id="b397f-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="b397f-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="b397f-108">[in] Tamaño, en bytes, del identificador de entrada al que apunta el  _parámetro lpEntryID1_  _._</span><span class="sxs-lookup"><span data-stu-id="b397f-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="b397f-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="b397f-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="b397f-110">[in] Puntero al primer identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="b397f-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="b397f-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="b397f-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="b397f-112">[in] Tamaño, en bytes, del identificador de entrada al que apunta el  _parámetro lpEntryID2_  _._</span><span class="sxs-lookup"><span data-stu-id="b397f-112">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="b397f-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="b397f-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="b397f-114">[in] Puntero al segundo identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="b397f-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="b397f-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b397f-115">_ulFlags_</span></span>
  
> <span data-ttu-id="b397f-116">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b397f-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="b397f-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="b397f-117">_lpulResult_</span></span>
  
> <span data-ttu-id="b397f-118">[salida] Puntero al resultado devuelto de la comparación.</span><span class="sxs-lookup"><span data-stu-id="b397f-118">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="b397f-119">TRUE si los dos identificadores de entrada hacen referencia al mismo objeto; en caso contrario, FALSE.</span><span class="sxs-lookup"><span data-stu-id="b397f-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b397f-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b397f-120">Return value</span></span>

<span data-ttu-id="b397f-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="b397f-121">S_OK</span></span> 
  
> <span data-ttu-id="b397f-122">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="b397f-122">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b397f-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b397f-123">Remarks</span></span>

<span data-ttu-id="b397f-124">MAPI llama al **método IMSProvider::CompareStoreIDs** cuando procesa una llamada al método [IMAPISession::OpenMsgStore.](imapisession-openmsgstore.md)</span><span class="sxs-lookup"><span data-stu-id="b397f-124">MAPI calls the **IMSProvider::CompareStoreIDs** method when it processes a call to the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> <span data-ttu-id="b397f-125">**Se llama a CompareStoreIDs** en este punto para determinar qué sección de perfil, si la hay, está asociada con el almacén de mensajes que se abre.</span><span class="sxs-lookup"><span data-stu-id="b397f-125">**CompareStoreIDs** is called at this point to determine which profile section, if any, is associated with the message store being opened.</span></span> <span data-ttu-id="b397f-126">Se puede realizar una llamada **CompareStoreIDs** cuando no hay ningún almacén de mensajes abierto para un proveedor de almacenamiento determinado.</span><span class="sxs-lookup"><span data-stu-id="b397f-126">A **CompareStoreIDs** call can be made when no message stores are open for a particular store provider.</span></span> <span data-ttu-id="b397f-127">Además, MAPI también llama a **CompareStoreIDs** cuando procesa una llamada de proveedor de almacén al [método IMAPISupport::OpenProfileSection.](imapisupport-openprofilesection.md)</span><span class="sxs-lookup"><span data-stu-id="b397f-127">In addition, MAPI also calls **CompareStoreIDs** when it processes a store provider call to the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method.</span></span> 
  
<span data-ttu-id="b397f-128">Los identificadores de entrada comparados por **CompareStoreID son** tanto para la biblioteca de vínculos dinámicos (DLL) del proveedor de almacenamiento actual como para los dos identificadores de entrada de almacén sin envolver.</span><span class="sxs-lookup"><span data-stu-id="b397f-128">The entry identifiers compared by **CompareStoreIDs** are both for the current store provider's dynamic-link library (DLL) and are both unwrapped store entry identifiers.</span></span> <span data-ttu-id="b397f-129">Para obtener más información acerca de cómo ajustar los identificadores de entrada del almacén, vea [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).</span><span class="sxs-lookup"><span data-stu-id="b397f-129">For more information about wrapping store entry identifiers, see [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).</span></span>
  
<span data-ttu-id="b397f-130">Comparar los identificadores de entrada es útil porque un objeto puede tener más de un identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="b397f-130">Comparing entry identifiers is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="b397f-131">Esto puede ocurrir, por ejemplo, después de instalar una nueva versión de un proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b397f-131">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b397f-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="b397f-132">See also</span></span>



[<span data-ttu-id="b397f-133">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="b397f-133">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="b397f-134">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="b397f-134">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="b397f-135">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="b397f-135">IMAPISupport::WrapStoreEntryID</span></span>](imapisupport-wrapstoreentryid.md)
  
[<span data-ttu-id="b397f-136">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b397f-136">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

