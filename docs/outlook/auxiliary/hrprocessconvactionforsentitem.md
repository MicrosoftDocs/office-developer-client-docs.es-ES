---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: Realiza la categorización de envío posterior a la en un elemento de correo en función de su PidTagConversationId.
ms.openlocfilehash: efecfc2d0d865428cb958fc15a858bbc7807c5d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816085"
---
# <a name="hrprocessconvactionforsentitem"></a><span data-ttu-id="61158-103">HrProcessConvActionForSentItem</span><span class="sxs-lookup"><span data-stu-id="61158-103">HrProcessConvActionForSentItem</span></span>

<span data-ttu-id="61158-104">Realiza la categorización de envío posterior a la en un elemento de correo en función de su [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="61158-104">Performs post-send categorization on a mail item based on its [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="61158-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="61158-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61158-106">Exportada por:</span><span class="sxs-lookup"><span data-stu-id="61158-106">Exported by:</span></span>  <br/> |<span data-ttu-id="61158-107">Outlook.exe</span><span class="sxs-lookup"><span data-stu-id="61158-107">Outlook.exe</span></span>  <br/> |
|<span data-ttu-id="61158-108">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="61158-108">Called by:</span></span>  <br/> |<span data-ttu-id="61158-109">Cliente</span><span class="sxs-lookup"><span data-stu-id="61158-109">Client</span></span>  <br/> |
|<span data-ttu-id="61158-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="61158-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="61158-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="61158-111">Outlook</span></span>  <br/> |
   
```cpp
HRESULT WINAPI HrProcessConvActionForSentItem( 
    SBinary const *pmbinStoreEid, 
    SBinary const *pmbinMsgEid, 
    SBinary const *pmbinConvID, 
    DWORD dwFlags)
```

## <a name="parameters"></a><span data-ttu-id="61158-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61158-112">Parameters</span></span>

<span data-ttu-id="61158-113">_pmbinStoreEid_</span><span class="sxs-lookup"><span data-stu-id="61158-113">_pmbinStoreEid_</span></span>
  
> <span data-ttu-id="61158-114">[entrada] [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) de la tienda o el [PidTagStoreEntryId](http://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) del elemento de correo.</span><span class="sxs-lookup"><span data-stu-id="61158-114">[in] The [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) of the store, or the [PidTagStoreEntryId](http://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="61158-115">No puede ser NULL o no es válido.</span><span class="sxs-lookup"><span data-stu-id="61158-115">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="61158-116">_pmbinMsgEid_</span><span class="sxs-lookup"><span data-stu-id="61158-116">_pmbinMsgEid_</span></span>
  
> <span data-ttu-id="61158-117">[entrada] [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) del elemento de correo.</span><span class="sxs-lookup"><span data-stu-id="61158-117">[in] The [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="61158-118">No puede ser NULL o no es válido.</span><span class="sxs-lookup"><span data-stu-id="61158-118">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="61158-119">_pmbinConvID_</span><span class="sxs-lookup"><span data-stu-id="61158-119">_pmbinConvID_</span></span>
  
> <span data-ttu-id="61158-120">[entrada] [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) del elemento de correo.</span><span class="sxs-lookup"><span data-stu-id="61158-120">[in] The [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="61158-121">No puede ser NULL o no es válido.</span><span class="sxs-lookup"><span data-stu-id="61158-121">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="61158-122">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="61158-122">_dwFlags_</span></span>
  
> <span data-ttu-id="61158-123">[entrada] Una máscara de bits que especifica información adicional acerca de la llamada al método.</span><span class="sxs-lookup"><span data-stu-id="61158-123">[in] A bitmask that specifies additional information about the method call.</span></span>
    
   - <span data-ttu-id="61158-124">0: no hay opciones adicionales que se usan en esta llamada al método.</span><span class="sxs-lookup"><span data-stu-id="61158-124">0—No additional options are used in this method call.</span></span> <span data-ttu-id="61158-125">Éste es el valor recomendado.</span><span class="sxs-lookup"><span data-stu-id="61158-125">This is the recommended value.</span></span> 
    
   - <span data-ttu-id="61158-126">**PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ es realmente el [PidTagSearchKey](http://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="61158-126">**PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ is actually the [PidTagSearchKey](http://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) of the message.</span></span> <span data-ttu-id="61158-127">Uso de un **PidTagSearchKey** es muchos recursos y se debe evitar si está disponible un [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="61158-127">Using a **PidTagSearchKey** is resource intensive, and should be avoided if a [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) is available.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="61158-128">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="61158-128">Return values</span></span>

|<span data-ttu-id="61158-129">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="61158-129">**HRESULT**</span></span>|<span data-ttu-id="61158-130">**Description**</span><span class="sxs-lookup"><span data-stu-id="61158-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="61158-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="61158-131">S_OK</span></span>  <br/> |<span data-ttu-id="61158-132">La llamada tuvo éxito.</span><span class="sxs-lookup"><span data-stu-id="61158-132">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="61158-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="61158-133">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="61158-134">_dwFlags_ contiene un indicador desconocido.</span><span class="sxs-lookup"><span data-stu-id="61158-134">_dwFlags_ contains an unknown flag.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61158-135">Notas</span><span class="sxs-lookup"><span data-stu-id="61158-135">Remarks</span></span>

<span data-ttu-id="61158-136">Las categorías se consideran información personal y no deberían ser transmitidas fuera del buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="61158-136">Categories are considered personal information and should not be transmitted outside the mailbox of the user.</span></span> <span data-ttu-id="61158-137">Por lo tanto, no llame a **HrProcessConvActionForSentItem** en un elemento de correo no enviados.</span><span class="sxs-lookup"><span data-stu-id="61158-137">Therefore, do not call **HrProcessConvActionForSentItem** on an unsent mail item.</span></span> <span data-ttu-id="61158-138">En su lugar, enviar el elemento y, a continuación, llamar a **HrProcessConvActionForSentItem** en la copia archivada.</span><span class="sxs-lookup"><span data-stu-id="61158-138">Instead, send the item, and then call **HrProcessConvActionForSentItem** on the archived copy.</span></span> <span data-ttu-id="61158-139">La copia archivada puede almacenarse en la carpeta Elementos enviados, o en una ubicación equivalente.</span><span class="sxs-lookup"><span data-stu-id="61158-139">The archived copy may be stored in the Sent Items folder, or an equivalent location.</span></span> 
  
<span data-ttu-id="61158-140">La aplicación debe ser en proceso con Outlook.exe, por ejemplo, desde un complemento COM, llamar a **HrProcessConvActionForSentItem**.</span><span class="sxs-lookup"><span data-stu-id="61158-140">Your application must be in-process with Outlook.exe, such as from a COM add-in, to call **HrProcessConvActionForSentItem**.</span></span> <span data-ttu-id="61158-141">Si intenta llamar a **HrProcessConvActionForSentItem** fuera de proceso, **HrProcessConvActionForSentItem** producirá una excepción de infracción de acceso.</span><span class="sxs-lookup"><span data-stu-id="61158-141">If you attempt to call **HrProcessConvActionForSentItem** out-of-process, **HrProcessConvActionForSentItem** will throw an access-violation exception.</span></span> 
  

