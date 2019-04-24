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
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: d255d7b6e80fe0c080fa0a27a7976db758a8c2ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350851"
---
# <a name="iattachmentsecurityisattachmentblocked"></a><span data-ttu-id="7c27a-103">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="7c27a-103">IAttachmentSecurity::IsAttachmentBlocked</span></span>

  
  
<span data-ttu-id="7c27a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c27a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c27a-105">Comprueba si Microsoft Outlook 2010 o Microsoft Outlook 2013 han bloqueado los datos adjuntos especificados para la visualización y la indización.</span><span class="sxs-lookup"><span data-stu-id="7c27a-105">Checks if a specified attachment is blocked by Microsoft Outlook 2010 or Microsoft Outlook 2013 for viewing and indexing.</span></span>
  
```cpp
HRESULT IAttachmentSecurity::IsAttachmentBlocked( 
    LPCWSTR pwszFileName,  
    BOOL *pfBlocked 
);
```

## <a name="parameters"></a><span data-ttu-id="7c27a-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="7c27a-106">Parameters</span></span>

 <span data-ttu-id="7c27a-107">_pwszFileName_</span><span class="sxs-lookup"><span data-stu-id="7c27a-107">_pwszFileName_</span></span>
  
> <span data-ttu-id="7c27a-108">a Puntero al nombre del archivo de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="7c27a-108">[in] Pointer to the filename of an attachment.</span></span>
    
 <span data-ttu-id="7c27a-109">_pfBlocked_</span><span class="sxs-lookup"><span data-stu-id="7c27a-109">_pfBlocked_</span></span>
  
> <span data-ttu-id="7c27a-110">contempla Puntero a un valor que indica **true** si se bloquean los datos adjuntos especificados; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="7c27a-110">[out] Pointer to a value indicating **true** if the specified attachment is blocked; otherwise, **false**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7c27a-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c27a-111">See also</span></span>



[<span data-ttu-id="7c27a-112">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="7c27a-112">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="7c27a-113">Comprobar que los datos adJuntos están bloqueados</span><span class="sxs-lookup"><span data-stu-id="7c27a-113">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

