---
title: IContabAdminRemoveStore
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IContabAdmin.RemoveStore
api_type:
- COM
ms.assetid: 2a5fcf5c-8a5a-4774-b8c9-1ac1ff27947d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4865c1c867dd73514ab22ac4e8da628caf154ee7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435421"
---
# <a name="icontabadminremovestore"></a><span data-ttu-id="f9f66-103">IContabAdmin::RemoveStore</span><span class="sxs-lookup"><span data-stu-id="f9f66-103">IContabAdmin::RemoveStore</span></span>

  
  
<span data-ttu-id="f9f66-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9f66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9f66-105">Quita la libreta de direcciones de contacto (CAB) especificada por el identificador de entrada especificado de la jerarquía de libretas de direcciones.</span><span class="sxs-lookup"><span data-stu-id="f9f66-105">Removes the Contact Address Book (CAB) specified by the given entry ID from the address book hierarchy.</span></span>
  
```cpp
HRESULT RemoveStore(
ULONG cbEntryID, 
LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="f9f66-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="f9f66-106">Parameters</span></span>

 <span data-ttu-id="f9f66-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f9f66-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="f9f66-108">a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="f9f66-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f9f66-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="f9f66-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="f9f66-110">a Un puntero al identificador de entrada del objeto que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="f9f66-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    

