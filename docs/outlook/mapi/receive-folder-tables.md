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
# <a name="receive-folder-tables"></a>Tablas de la carpeta de recepción

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una tabla de carpetas de recepción contiene información de todas las carpetas designadas como carpetas de recepción de un almacén de mensajes. Una carpeta de recepción es una carpeta en la que se colocan los mensajes entrantes de una clase de mensaje determinada. Los proveedores de almacenamiento de mensajes implementan las tablas de la carpeta de recepción y las aplicaciones cliente las usan realizando una llamada al método [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) . 
  
Las siguientes propiedades componen el conjunto de columnas necesario en las tablas de la carpeta de recepción:
  
 **** Es ([PidTagEntryId](pidtagentryid-canonical-property.md)) 
  
 **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) 
  
 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
  
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

