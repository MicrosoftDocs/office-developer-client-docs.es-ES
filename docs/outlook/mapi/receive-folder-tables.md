---
title: Tablas de carpetas de recepción
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b291167a0457eaaf4f3bcb48ab36d6c6e6512fcc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417353"
---
# <a name="receive-folder-tables"></a>Tablas de carpetas de recepción

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una tabla de carpetas de recepción contiene información de todas las carpetas designadas como carpetas de recepción para un almacén de mensajes. Una carpeta de recepción es una carpeta donde se colocan los mensajes entrantes de una clase de mensaje determinada. Los proveedores de almacén de mensajes implementan tablas de carpetas de recepción y las aplicaciones cliente las usan mediante una llamada al método [IMsgStore::GetReceiveFolderTable.](imsgstore-getreceivefoldertable.md) 
  
Las siguientes propiedades son la columna necesaria establecida en las tablas de carpetas de recepción:
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 
  
 **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) 
  
 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
  
## <a name="see-also"></a>Consulte también



[Tablas MAPI](mapi-tables.md)

