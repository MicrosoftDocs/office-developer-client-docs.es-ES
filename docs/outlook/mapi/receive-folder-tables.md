---
title: Tablas de la carpeta de recepción
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b291167a0457eaaf4f3bcb48ab36d6c6e6512fcc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328479"
---
# <a name="receive-folder-tables"></a><span data-ttu-id="a36e3-103">Tablas de la carpeta de recepción</span><span class="sxs-lookup"><span data-stu-id="a36e3-103">Receive Folder Tables</span></span>

  
  
<span data-ttu-id="a36e3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a36e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a36e3-105">Una tabla de carpetas de recepción contiene información de todas las carpetas designadas como carpetas de recepción de un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a36e3-105">A receive folder table contains information for all the folders designated as receive folders for a message store.</span></span> <span data-ttu-id="a36e3-106">Una carpeta de recepción es una carpeta en la que se colocan los mensajes entrantes de una clase de mensaje determinada.</span><span class="sxs-lookup"><span data-stu-id="a36e3-106">A receive folder is a folder where incoming messages of a particular message class are placed.</span></span> <span data-ttu-id="a36e3-107">Los proveedores de almacenamiento de mensajes implementan las tablas de la carpeta de recepción y las aplicaciones cliente las usan realizando una llamada al método [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) .</span><span class="sxs-lookup"><span data-stu-id="a36e3-107">Message store providers implement receive folder tables and client applications use them by making a call to the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="a36e3-108">Las siguientes propiedades componen el conjunto de columnas necesario en las tablas de la carpeta de recepción:</span><span class="sxs-lookup"><span data-stu-id="a36e3-108">The following properties make up the required column set in receive folder tables:</span></span>
  
 <span data-ttu-id="a36e3-109">\*\*\*\* Es ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a36e3-109">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span> 
  
 <span data-ttu-id="a36e3-110">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a36e3-110">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span> 
  
 <span data-ttu-id="a36e3-111">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a36e3-111">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a36e3-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="a36e3-112">See also</span></span>



[<span data-ttu-id="a36e3-113">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="a36e3-113">MAPI Tables</span></span>](mapi-tables.md)

