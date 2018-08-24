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
ms.openlocfilehash: 03917ad52f1dc1ce4d0b59cd54fe33f58f352061
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582948"
---
# <a name="deleting-a-recipient"></a><span data-ttu-id="4249b-103">Eliminar un destinatario</span><span class="sxs-lookup"><span data-stu-id="4249b-103">Deleting a Recipient</span></span>

  
  
<span data-ttu-id="4249b-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4249b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="4249b-105">**Para quitar entradas de la libreta de direcciones de uno o más de un contenedor modificable**</span><span class="sxs-lookup"><span data-stu-id="4249b-105">**To remove one or more address book entries from a modifiable container**</span></span>
  
- <span data-ttu-id="4249b-106">Llame al método [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) , pasando una matriz de identificadores de entrada que representan las entradas de la libreta de direcciones que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="4249b-106">Call the [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method, passing an array of entry identifiers that represent the address book entries to be deleted.</span></span> <span data-ttu-id="4249b-107">**DeleteEntries** puede devolver una advertencia, MAPI_W_PARTIAL_COMPLETION, para indicar que no se pudo eliminar una o varias de las entradas.</span><span class="sxs-lookup"><span data-stu-id="4249b-107">**DeleteEntries** can return a warning, MAPI_W_PARTIAL_COMPLETION, to indicate that it couldn't delete one or more of the entries.</span></span> <span data-ttu-id="4249b-108">Pruebe para este valor devuelto a la macro **HR_FAILED** y llamar al método [IMAPIProp::GetLastError](imapiprop-getlasterror.md) del contenedor si se necesita más información acerca del problema.</span><span class="sxs-lookup"><span data-stu-id="4249b-108">Test for this return value with the **HR_FAILED** macro and call the container's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if more information about the problem is needed.</span></span> 
    
<span data-ttu-id="4249b-109">Cuando se mantiene un puntero a la estructura [ADRENTRY](adrentry.md) de una entrada eliminada en la memoria caché, podrá recuperar propiedades mediante su identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="4249b-109">When you hold a pointer to a deleted entry's [ADRENTRY](adrentry.md) structure in your cache, you will still be able to retrieve properties using its entry identifier.</span></span> <span data-ttu-id="4249b-110">Esto es debido a que la entrada sólo se marca para su eliminación.</span><span class="sxs-lookup"><span data-stu-id="4249b-110">This is because the entry is only marked for deletion.</span></span> <span data-ttu-id="4249b-111">MAPI mantiene un nivel de acceso a estas entradas marcadas por diseño.</span><span class="sxs-lookup"><span data-stu-id="4249b-111">MAPI maintains a level of access to these marked entries by design.</span></span> 
  

