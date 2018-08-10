---
title: Quitar entradas de la libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 107ebcd7-b612-4139-b676-c3851f15bc74
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1fb7224e110bbee6844cf2820782aac8be213ba3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820487"
---
# <a name="removing-address-book-entries"></a><span data-ttu-id="7cd11-103">Quitar entradas de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="7cd11-103">Removing address book entries</span></span>
  
<span data-ttu-id="7cd11-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7cd11-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7cd11-105">Método de [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) de su contenedor se llama para quitar a uno o más destinatarios.</span><span class="sxs-lookup"><span data-stu-id="7cd11-105">Your container's [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method is called to remove one or more recipients.</span></span> <span data-ttu-id="7cd11-106">**DeleteEntries** tiene dos parámetros: una matriz de identificadores de entrada que representa los destinatarios que se eliminará y un valor de indicadores reservados.</span><span class="sxs-lookup"><span data-stu-id="7cd11-106">**DeleteEntries** has two parameters: an array of entry identifiers representing the recipients to be deleted and a reserved flags value.</span></span> <span data-ttu-id="7cd11-107">Eliminación de un destinatario afecta a la tabla de contenido de su contenedor. Además de eliminar al destinatario, el contenedor debe eliminar la fila de tabla de contenido que representa al destinatario.</span><span class="sxs-lookup"><span data-stu-id="7cd11-107">Deleting a recipient affects the contents table of your container; in addition to deleting the recipient, your container must delete the contents table row that represents the recipient.</span></span> <span data-ttu-id="7cd11-108">Cuando se ha quitado la fila de la tabla, el contenedor debe emitir una notificación de la tabla para cada cliente registrado.</span><span class="sxs-lookup"><span data-stu-id="7cd11-108">When the row has been removed from the table, your container must issue a table notification to each registered client.</span></span> 
  
### <a name="to-implement-iabcontainerdeleteentries"></a><span data-ttu-id="7cd11-109">Para implementar IABContainer::DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="7cd11-109">To implement IABContainer::DeleteEntries</span></span>
  
1. <span data-ttu-id="7cd11-110">Eliminación de cada destinatario representado por el identificador de entrada de su contenedor.</span><span class="sxs-lookup"><span data-stu-id="7cd11-110">Delete each recipient represented by the entry identifier from your container.</span></span>
    
2. <span data-ttu-id="7cd11-111">Si la tabla de contenido de su contenedor está abierto:</span><span class="sxs-lookup"><span data-stu-id="7cd11-111">If your container's contents table is open:</span></span>
    
   - <span data-ttu-id="7cd11-112">Enviar una notificación de _fnevTableModified_ con el **ulTableEvent** conjunto de miembros a TABLE_ROW_DELETED a los clientes registrados para cada fila de la tabla de contenido eliminado.</span><span class="sxs-lookup"><span data-stu-id="7cd11-112">Send an  _fnevTableModified_ notification with the **ulTableEvent** member set to TABLE_ROW_DELETED to registered clients for each deleted contents table row.</span></span> <span data-ttu-id="7cd11-113">Si su proveedor usa la utilidad de notificación, llame a [IMAPISupport::Notify](imapisupport-notify.md) para enviar estas notificaciones.</span><span class="sxs-lookup"><span data-stu-id="7cd11-113">If your provider uses the notification utility, call [IMAPISupport::Notify](imapisupport-notify.md) to send these notifications.</span></span> 
    
   - <span data-ttu-id="7cd11-114">Si el proveedor admite las notificaciones de objeto, también enviar una notificación de _fnevObjectDeleted_ .</span><span class="sxs-lookup"><span data-stu-id="7cd11-114">If your provider supports object notifications, also send an  _fnevObjectDeleted_ notification.</span></span> 
    

