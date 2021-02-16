---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: Realiza la categorización posterior al envío en un elemento de correo basado en su PidTagConversationId.
ms.openlocfilehash: 675f308093eea30084271abc66c1fa66e2ad6828
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318903"
---
# <a name="hrprocessconvactionforsentitem"></a><span data-ttu-id="fddda-103">HrProcessConvActionForSentItem</span><span class="sxs-lookup"><span data-stu-id="fddda-103">HrProcessConvActionForSentItem</span></span>

<span data-ttu-id="fddda-104">Realiza la categorización posterior al envío en un elemento de correo basado en [su PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="fddda-104">Performs post-send categorization on a mail item based on its [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fddda-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="fddda-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fddda-106">Exportado por:</span><span class="sxs-lookup"><span data-stu-id="fddda-106">Exported by:</span></span>  <br/> |<span data-ttu-id="fddda-107">Outlook.exe</span><span class="sxs-lookup"><span data-stu-id="fddda-107">Outlook.exe</span></span>  <br/> |
|<span data-ttu-id="fddda-108">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="fddda-108">Called by:</span></span>  <br/> |<span data-ttu-id="fddda-109">Cliente</span><span class="sxs-lookup"><span data-stu-id="fddda-109">Client</span></span>  <br/> |
|<span data-ttu-id="fddda-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="fddda-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="fddda-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="fddda-111">Outlook</span></span>  <br/> |
   
```cpp
HRESULT WINAPI HrProcessConvActionForSentItem( 
    SBinary const *pmbinStoreEid, 
    SBinary const *pmbinMsgEid, 
    SBinary const *pmbinConvID, 
    DWORD dwFlags)
```

## <a name="parameters"></a><span data-ttu-id="fddda-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fddda-112">Parameters</span></span>

<span data-ttu-id="fddda-113">_pmbinStoreEid_</span><span class="sxs-lookup"><span data-stu-id="fddda-113">_pmbinStoreEid_</span></span>
  
> <span data-ttu-id="fddda-114">[entrada] [PidTagEntryId del](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) almacén o [PidTagStoreEntryId](https://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) del elemento de correo.</span><span class="sxs-lookup"><span data-stu-id="fddda-114">[in] The [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) of the store, or the [PidTagStoreEntryId](https://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="fddda-115">No puede ser NULL o no válido.</span><span class="sxs-lookup"><span data-stu-id="fddda-115">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="fddda-116">_pmbinMsgEid_</span><span class="sxs-lookup"><span data-stu-id="fddda-116">_pmbinMsgEid_</span></span>
  
> <span data-ttu-id="fddda-117">[entrada] [PidTagEntryId del](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) elemento de correo.</span><span class="sxs-lookup"><span data-stu-id="fddda-117">[in] The [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="fddda-118">No puede ser NULL o no válido.</span><span class="sxs-lookup"><span data-stu-id="fddda-118">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="fddda-119">_pmbinConvID_</span><span class="sxs-lookup"><span data-stu-id="fddda-119">_pmbinConvID_</span></span>
  
> <span data-ttu-id="fddda-120">[entrada] [PidTagConversationId del](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) elemento de correo.</span><span class="sxs-lookup"><span data-stu-id="fddda-120">[in] The [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="fddda-121">No puede ser NULL o no válido.</span><span class="sxs-lookup"><span data-stu-id="fddda-121">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="fddda-122">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="fddda-122">_dwFlags_</span></span>
  
> <span data-ttu-id="fddda-123">[entrada] Máscara de bits que especifica información adicional sobre la llamada al método.</span><span class="sxs-lookup"><span data-stu-id="fddda-123">[in] A bitmask that specifies additional information about the method call.</span></span>
    
   - <span data-ttu-id="fddda-124">0: no se usan opciones adicionales en esta llamada de método.</span><span class="sxs-lookup"><span data-stu-id="fddda-124">0—No additional options are used in this method call.</span></span> <span data-ttu-id="fddda-125">Este es el valor recomendado.</span><span class="sxs-lookup"><span data-stu-id="fddda-125">This is the recommended value.</span></span> 
    
   - <span data-ttu-id="fddda-126">**PCAFSIF_MSGEID_IS_SEARCH_KEY:** _pmbinMsgEid_ es en realidad [pidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="fddda-126">**PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ is actually the [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) of the message.</span></span> <span data-ttu-id="fddda-127">El uso **de PidTagSearchKey** consume muchos recursos y debe evitarse si un [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) está disponible.</span><span class="sxs-lookup"><span data-stu-id="fddda-127">Using a **PidTagSearchKey** is resource intensive, and should be avoided if a [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) is available.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="fddda-128">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="fddda-128">Return values</span></span>

|<span data-ttu-id="fddda-129">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="fddda-129">**HRESULT**</span></span>|<span data-ttu-id="fddda-130">**Description**</span><span class="sxs-lookup"><span data-stu-id="fddda-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fddda-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="fddda-131">S_OK</span></span>  <br/> |<span data-ttu-id="fddda-132">La llamada se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="fddda-132">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="fddda-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="fddda-133">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="fddda-134">_dwFlags_ contiene una marca desconocida.</span><span class="sxs-lookup"><span data-stu-id="fddda-134">_dwFlags_ contains an unknown flag.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fddda-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fddda-135">Remarks</span></span>

<span data-ttu-id="fddda-136">Las categorías se consideran información personal y no deben transmitirse fuera del buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="fddda-136">Categories are considered personal information and should not be transmitted outside the mailbox of the user.</span></span> <span data-ttu-id="fddda-137">Por lo tanto, no llame **a HrProcessConvActionForSentItem** en un elemento de correo no enviado.</span><span class="sxs-lookup"><span data-stu-id="fddda-137">Therefore, do not call **HrProcessConvActionForSentItem** on an unsent mail item.</span></span> <span data-ttu-id="fddda-138">En su lugar, envíe el elemento y, a continuación, llame a **HrProcessConvActionForSentItem** en la copia archivada.</span><span class="sxs-lookup"><span data-stu-id="fddda-138">Instead, send the item, and then call **HrProcessConvActionForSentItem** on the archived copy.</span></span> <span data-ttu-id="fddda-139">La copia archivada puede almacenarse en la carpeta Elementos enviados o en una ubicación equivalente.</span><span class="sxs-lookup"><span data-stu-id="fddda-139">The archived copy may be stored in the Sent Items folder, or an equivalent location.</span></span> 
  
<span data-ttu-id="fddda-140">La aplicación debe estar en proceso con Outlook.exe, como desde un complemento COM, para llamar a **HrProcessConvActionForSentItem**.</span><span class="sxs-lookup"><span data-stu-id="fddda-140">Your application must be in-process with Outlook.exe, such as from a COM add-in, to call **HrProcessConvActionForSentItem**.</span></span> <span data-ttu-id="fddda-141">Si intenta llamar a **HrProcessConvActionForSentItem** fuera de proceso, **HrProcessConvActionForSentItem** producirá una excepción de infracción de acceso.</span><span class="sxs-lookup"><span data-stu-id="fddda-141">If you attempt to call **HrProcessConvActionForSentItem** out-of-process, **HrProcessConvActionForSentItem** will throw an access-violation exception.</span></span> 
  

