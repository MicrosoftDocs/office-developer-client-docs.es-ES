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
ms.openlocfilehash: 1d5ae33b08c85c9ee93764d762c2ec251fddd265
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425263"
---
# <a name="removing-address-book-entries"></a><span data-ttu-id="182a0-103">Quitar entradas de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="182a0-103">Removing address book entries</span></span>
  
<span data-ttu-id="182a0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="182a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="182a0-105">Se llama al método [IABContainer::D eleteentries](iabcontainer-deleteentries.md) del contenedor para quitar uno o más destinatarios.</span><span class="sxs-lookup"><span data-stu-id="182a0-105">Your container's [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method is called to remove one or more recipients.</span></span> <span data-ttu-id="182a0-106">**DeleteEntries** tiene dos parámetros: una matriz de identificadores de entrada que representan los destinatarios que se van a eliminar y un valor de indicadores reservados.</span><span class="sxs-lookup"><span data-stu-id="182a0-106">**DeleteEntries** has two parameters: an array of entry identifiers representing the recipients to be deleted and a reserved flags value.</span></span> <span data-ttu-id="182a0-107">La eliminación de un destinatario afecta a la tabla de contenido del contenedor; Además de eliminar el destinatario, el contenedor debe eliminar la fila de la tabla de contenido que representa al destinatario.</span><span class="sxs-lookup"><span data-stu-id="182a0-107">Deleting a recipient affects the contents table of your container; in addition to deleting the recipient, your container must delete the contents table row that represents the recipient.</span></span> <span data-ttu-id="182a0-108">Cuando se ha quitado la fila de la tabla, el contenedor debe emitir una notificación de tabla para cada cliente registrado.</span><span class="sxs-lookup"><span data-stu-id="182a0-108">When the row has been removed from the table, your container must issue a table notification to each registered client.</span></span> 
  
### <a name="to-implement-iabcontainerdeleteentries"></a><span data-ttu-id="182a0-109">Para implementar IABContainer::D eleteEntries</span><span class="sxs-lookup"><span data-stu-id="182a0-109">To implement IABContainer::DeleteEntries</span></span>
  
1. <span data-ttu-id="182a0-110">Elimine del contenedor todos los destinatarios que representa el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="182a0-110">Delete each recipient represented by the entry identifier from your container.</span></span>
    
2. <span data-ttu-id="182a0-111">Si la tabla de contenido del contenedor está abierta:</span><span class="sxs-lookup"><span data-stu-id="182a0-111">If your container's contents table is open:</span></span>
    
   - <span data-ttu-id="182a0-112">Envíe una notificación _fnevTableModified_ con el miembro **ULTABLEEVENT** establecido en TABLE_ROW_DELETED a los clientes registrados para cada fila de tabla de contenido eliminada.</span><span class="sxs-lookup"><span data-stu-id="182a0-112">Send an  _fnevTableModified_ notification with the **ulTableEvent** member set to TABLE_ROW_DELETED to registered clients for each deleted contents table row.</span></span> <span data-ttu-id="182a0-113">Si su proveedor usa la utilidad de notificación, llame a [IMAPISupport:: Notify](imapisupport-notify.md) para enviar estas notificaciones.</span><span class="sxs-lookup"><span data-stu-id="182a0-113">If your provider uses the notification utility, call [IMAPISupport::Notify](imapisupport-notify.md) to send these notifications.</span></span> 
    
   - <span data-ttu-id="182a0-114">Si el proveedor admite notificaciones de objeto, también puede enviar una notificación _fnevObjectDeleted_ .</span><span class="sxs-lookup"><span data-stu-id="182a0-114">If your provider supports object notifications, also send an  _fnevObjectDeleted_ notification.</span></span> 
    

