---
title: Tablas de carpeta de recibidos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b88545ede6275bd834fad5869d972e2860a6c77e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573183"
---
# <a name="receive-folder-tables"></a><span data-ttu-id="2d77d-103">Tablas de carpeta de recibidos</span><span class="sxs-lookup"><span data-stu-id="2d77d-103">Receive Folder Tables</span></span>

  
  
<span data-ttu-id="2d77d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d77d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d77d-105">Una tabla de la carpeta de recepción contiene información para todas las carpetas que se designan como las carpetas de recepción para un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="2d77d-105">A receive folder table contains information for all the folders designated as receive folders for a message store.</span></span> <span data-ttu-id="2d77d-106">Una carpeta de recepción es una carpeta donde se colocan los mensajes entrantes de una clase de mensaje en particular.</span><span class="sxs-lookup"><span data-stu-id="2d77d-106">A receive folder is a folder where incoming messages of a particular message class are placed.</span></span> <span data-ttu-id="2d77d-107">Implementan los proveedores de almacén de mensajes reciben las tablas de la carpeta y las aplicaciones cliente usan ellos mediante la realización de una llamada al método [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) .</span><span class="sxs-lookup"><span data-stu-id="2d77d-107">Message store providers implement receive folder tables and client applications use them by making a call to the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="2d77d-108">Las siguientes propiedades componen la columna requiere establecer en recibir las tablas de carpeta:</span><span class="sxs-lookup"><span data-stu-id="2d77d-108">The following properties make up the required column set in receive folder tables:</span></span>
  
 <span data-ttu-id="2d77d-109">**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2d77d-109">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span> 
  
 <span data-ttu-id="2d77d-110">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2d77d-110">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span> 
  
 <span data-ttu-id="2d77d-111">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2d77d-111">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2d77d-112">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="2d77d-112">See also</span></span>



[<span data-ttu-id="2d77d-113">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="2d77d-113">MAPI Tables</span></span>](mapi-tables.md)

