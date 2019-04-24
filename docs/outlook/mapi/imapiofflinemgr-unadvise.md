---
title: IMAPIOfflineMgrUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Unadvise
api_type:
- COM
ms.assetid: 250b9137-facb-81a2-41b1-96a57366c04e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 800f79179f999ba193d4177abb7341095b8b896d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321220"
---
# <a name="imapiofflinemgrunadvise"></a><span data-ttu-id="0dd69-103">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="0dd69-103">IMAPIOfflineMgr::Unadvise</span></span>

  
  
<span data-ttu-id="0dd69-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0dd69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0dd69-105">Cancela las devoluciones de llamada para un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="0dd69-105">Cancels callbacks for an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="0dd69-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="0dd69-106">Parameters</span></span>

 <span data-ttu-id="0dd69-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0dd69-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0dd69-108">a Marcas para cancelar la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="0dd69-108">[in] Flags for canceling callback.</span></span> <span data-ttu-id="0dd69-109">Solo se admite el valor MAPIOFFLINE_UNADVISE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="0dd69-109">Only the value MAPIOFFLINE_UNADVISE_DEFAULT is supported.</span></span>
    
 <span data-ttu-id="0dd69-110">_ulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="0dd69-110">_ulAdviseToken_</span></span>
  
> <span data-ttu-id="0dd69-111">a Un token de notificación que identifica el registro de devolución de llamada que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="0dd69-111">[in] An advise token that identifies the callback registration that is to be canceled.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0dd69-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0dd69-112">Return value</span></span>

<span data-ttu-id="0dd69-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="0dd69-113">S_OK</span></span>
  
> <span data-ttu-id="0dd69-114">La llamada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0dd69-114">The call was successful.</span></span> <span data-ttu-id="0dd69-115">Esta llamada debe devolver S_OK.</span><span class="sxs-lookup"><span data-stu-id="0dd69-115">This call must return S_OK.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0dd69-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0dd69-116">Remarks</span></span>

<span data-ttu-id="0dd69-117">Quita el registro de la devolución de llamada asociada con *ulAdviseToken* devueltos de una llamada anterior a **[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="0dd69-117">Removes the registration for the callback that was associated with  *ulAdviseToken*  returned from a prior call to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="0dd69-118">Hace que el objeto **IMAPIOfflineMgr** libere su referencia en el objeto **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** asociado a *ulAdviseToken* .</span><span class="sxs-lookup"><span data-stu-id="0dd69-118">Causes the **IMAPIOfflineMgr** object to release its reference on the **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** object associated with  *ulAdviseToken*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0dd69-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="0dd69-119">See also</span></span>



[<span data-ttu-id="0dd69-120">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="0dd69-120">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="0dd69-121">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="0dd69-121">MAPI Constants</span></span>](mapi-constants.md)

