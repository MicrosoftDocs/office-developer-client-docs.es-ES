---
title: Eliminar un destinatario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f7495030-e3b8-4c7c-9e19-284ba820e846
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bd01c66d9fff7c94ffb1ce9f956f1951bc482020
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421049"
---
# <a name="deleting-a-recipient"></a><span data-ttu-id="7394d-103">Eliminar un destinatario</span><span class="sxs-lookup"><span data-stu-id="7394d-103">Deleting a Recipient</span></span>

  
  
<span data-ttu-id="7394d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7394d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="7394d-105">**Para quitar una o varias entradas de la libreta de direcciones de un contenedor modificable**</span><span class="sxs-lookup"><span data-stu-id="7394d-105">**To remove one or more address book entries from a modifiable container**</span></span>
  
- <span data-ttu-id="7394d-106">Llama al [método IABContainer::D eleteEntries](iabcontainer-deleteentries.md) y pasa una matriz de identificadores de entrada que representan las entradas de la libreta de direcciones que se eliminarán.</span><span class="sxs-lookup"><span data-stu-id="7394d-106">Call the [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method, passing an array of entry identifiers that represent the address book entries to be deleted.</span></span> <span data-ttu-id="7394d-107">**DeleteEntries** puede devolver una advertencia, MAPI_W_PARTIAL_COMPLETION, para indicar que no pudo eliminar una o varias de las entradas.</span><span class="sxs-lookup"><span data-stu-id="7394d-107">**DeleteEntries** can return a warning, MAPI_W_PARTIAL_COMPLETION, to indicate that it couldn't delete one or more of the entries.</span></span> <span data-ttu-id="7394d-108">Pruebe este valor devuelto con la macro **HR_FAILED** y llame al método [IMAPIProp::GetLastError](imapiprop-getlasterror.md) del contenedor si se necesita más información sobre el problema.</span><span class="sxs-lookup"><span data-stu-id="7394d-108">Test for this return value with the **HR_FAILED** macro and call the container's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if more information about the problem is needed.</span></span> 
    
<span data-ttu-id="7394d-109">Cuando mantenga un puntero a la estructura [ADRENTRY](adrentry.md) de una entrada eliminada en la memoria caché, podrá recuperar propiedades mediante su identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="7394d-109">When you hold a pointer to a deleted entry's [ADRENTRY](adrentry.md) structure in your cache, you will still be able to retrieve properties using its entry identifier.</span></span> <span data-ttu-id="7394d-110">Esto se debe a que la entrada solo está marcada para su eliminación.</span><span class="sxs-lookup"><span data-stu-id="7394d-110">This is because the entry is only marked for deletion.</span></span> <span data-ttu-id="7394d-111">MAPI mantiene un nivel de acceso a estas entradas marcadas por diseño.</span><span class="sxs-lookup"><span data-stu-id="7394d-111">MAPI maintains a level of access to these marked entries by design.</span></span> 
  

