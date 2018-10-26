---
title: IAttachmentSecurityIsAttachmentBlocked
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttachmentSecurity.IsAttachmentBlocked
api_type:
- COM
ms.assetid: 6986d27a-9602-e44a-0797-4c47f2184ef7
description: 'Última modificación: 25 de junio de 2012'
ms.openlocfilehash: ff13866139bf422f071eaba2c146aa1140ccd1ab
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565049"
---
# <a name="iattachmentsecurityisattachmentblocked"></a><span data-ttu-id="e523b-103">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="e523b-103">IAttachmentSecurity::IsAttachmentBlocked</span></span>

  
  
<span data-ttu-id="e523b-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e523b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e523b-105">Comprueba si los datos adjuntos especificados está bloqueado por Microsoft Outlook 2010 o Microsoft Outlook 2013 para su visualización e indización.</span><span class="sxs-lookup"><span data-stu-id="e523b-105">Checks if a specified attachment is blocked by Microsoft Outlook 2010 or Microsoft Outlook 2013 for viewing and indexing.</span></span>
  
```cpp
HRESULT IAttachmentSecurity::IsAttachmentBlocked( 
    LPCWSTR pwszFileName,  
    BOOL *pfBlocked 
);
```

## <a name="parameters"></a><span data-ttu-id="e523b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e523b-106">Parameters</span></span>

 <span data-ttu-id="e523b-107">_pwszFileName_</span><span class="sxs-lookup"><span data-stu-id="e523b-107">_pwszFileName_</span></span>
  
> <span data-ttu-id="e523b-108">[entrada] Puntero al nombre del archivo de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="e523b-108">[in] Pointer to the filename of an attachment.</span></span>
    
 <span data-ttu-id="e523b-109">_pfBlocked_</span><span class="sxs-lookup"><span data-stu-id="e523b-109">_pfBlocked_</span></span>
  
> <span data-ttu-id="e523b-110">[out] Puntero a un valor que indica **true** si está bloqueado el archivo adjunto especificado; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="e523b-110">[out] Pointer to a value indicating **true** if the specified attachment is blocked; otherwise, **false**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e523b-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="e523b-111">See also</span></span>



[<span data-ttu-id="e523b-112">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="e523b-112">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="e523b-113">Compruebe que se bloquea un dato adjunto</span><span class="sxs-lookup"><span data-stu-id="e523b-113">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

