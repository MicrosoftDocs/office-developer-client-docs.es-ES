---
title: Buscar el icono de un mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80a97c3d-4bca-4819-9da4-ca0fbf3a686f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b73545585d3279bc290524c7ccb26c14c2977fe4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816803"
---
# <a name="finding-the-icon-for-a-message"></a><span data-ttu-id="59508-103">Buscar el icono de un mensaje</span><span class="sxs-lookup"><span data-stu-id="59508-103">Finding the Icon for a Message</span></span>

  
  
<span data-ttu-id="59508-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="59508-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="59508-105">**Para buscar el icono asociado a un mensaje**</span><span class="sxs-lookup"><span data-stu-id="59508-105">**To find the icon associated with a message**</span></span>
  
1. <span data-ttu-id="59508-106">Llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) del mensaje para recuperar su propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="59508-106">Call the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="59508-107">Llame a [MAPIOpenFormMgr](mapiopenformmgr.md) para recuperar un puntero de interfaz **IMAPIFormMgr** .</span><span class="sxs-lookup"><span data-stu-id="59508-107">Call [MAPIOpenFormMgr](mapiopenformmgr.md) to retrieve an **IMAPIFormMgr** interface pointer.</span></span> <span data-ttu-id="59508-108">Pase el puntero **IMAPISession** en el parámetro _pSession_ .</span><span class="sxs-lookup"><span data-stu-id="59508-108">Pass your **IMAPISession** pointer in the  _pSession_ parameter.</span></span> 
    
3. <span data-ttu-id="59508-109">Llame a [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) para recuperar un puntero de interfaz **IMAPIFormInfo** .</span><span class="sxs-lookup"><span data-stu-id="59508-109">Call [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) to retrieve an **IMAPIFormInfo** interface pointer.</span></span> 
    
4. <span data-ttu-id="59508-110">Use el puntero **IMAPIFormInfo** para llamar a [IMAPIProp::GetProps](imapiprop-getprops.md) y recuperar el **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) y las propiedades de **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="59508-110">Use the **IMAPIFormInfo** pointer to call [IMAPIProp::GetProps](imapiprop-getprops.md) and retrieve the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) and/or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) properties.</span></span> 
    

