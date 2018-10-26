---
title: Carpetas especiales en los almacenes de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9462070e-1472-4e12-ba4e-e4ac60022892
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: a5446ce30812b30b193e87484a7322d9ddf7d781
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572714"
---
# <a name="special-folders-in-message-stores"></a>Carpetas especiales en los almacenes de mensajes

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Special folders such as the Inbox, Outbox, and search-results folder may be created in advance and protected by the message store provider. If the folders do not exist, MAPI will attempt to create them in the message store by calling the [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function. For more information, see [Carpetas especiales de MAPI](mapi-special-folders.md).
  
## <a name="see-also"></a>Vea también



[Implementar carpetas en los almacenes de mensajes](implementing-folders-in-message-stores.md)

