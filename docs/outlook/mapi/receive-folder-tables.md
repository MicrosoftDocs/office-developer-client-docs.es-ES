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
# <a name="receive-folder-tables"></a>Tablas de carpeta de recibidos

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una tabla de la carpeta de recepción contiene información para todas las carpetas que se designan como las carpetas de recepción para un almacén de mensajes. Una carpeta de recepción es una carpeta donde se colocan los mensajes entrantes de una clase de mensaje en particular. Implementan los proveedores de almacén de mensajes reciben las tablas de la carpeta y las aplicaciones cliente usan ellos mediante la realización de una llamada al método [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) . 
  
Las siguientes propiedades componen la columna requiere establecer en recibir las tablas de carpeta:
  
 **Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 
  
 **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) 
  
 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
  
## <a name="see-also"></a>Recursos adicionales



[Tablas MAPI](mapi-tables.md)

