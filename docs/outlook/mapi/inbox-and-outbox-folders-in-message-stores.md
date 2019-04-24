---
title: Bandejas de entrada y salida en los almacenes de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8e4ce129-137d-4618-80a6-88781a578d01
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 95a2b7b9bac11404817fb6848d58c45251c141f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309677"
---
# <a name="inbox-and-outbox-folders-in-message-stores"></a>Bandejas de entrada y salida en los almacenes de mensajes

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Para ser el almacén de mensajes predeterminado, el proveedor de almacén de mensajes debe implementar las carpetas Bandeja de entrada y Bandeja de salida. Normalmente se almacenan en el subárbol IPM de un almacén de mensajes. Estas carpetas tienen de especial el estar designadas como las carpetas a las que se entregan y desde las que se envían los mensajes, pero no necesitan ninguna funcionalidad especial. El envío y la recepción de mensajes ocurre por medio de secuencias de llamada definidas entre las aplicaciones cliente, la cola MAPI y el proveedor de almacén de mensajes. Las carpetas Bandeja de entrada y Bandeja de salida son simplemente carpetas que sirven para contener mensajes durante esas secuencias de llamada. Lo importante no es que las carpetas sean especiales, ni siquiera el que se denominen Bandeja de entrada y Bandeja de salida; lo importante es que el proveedor de almacén de mensajes las use como parte de su soporte para el envío y la recepción de mensajes.
  
Para permitir la recepción de mensajes, el proveedor de almacén de mensajes debe implementar los métodos [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) y [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md). Para más información, consulte [Recibir mensajes usando proveedores de almacenamiento de mensajes](receiving-messages-by-using-message-store-providers.md).
  
Para permitir el envío de mensajes, el proveedor de almacén de mensajes debe admitir el método [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md), además de los demás métodos usados por la cola MAPI durante el proceso de envío de mensajes. La cola de salida de un almacén de mensajes no necesita corresponder a una carpeta real del árbol de carpetas del almacén de mensajes. Pero es habitual que los proveedores de almacén de mensajes muestren el contenido de la cola de mensajes salientes en la carpeta Bandeja de salida, si esta existe. De esta forma, las aplicaciones cliente tienen una manera conveniente de indicar el estado de los mensajes que ha enviado el usuario, porque se puede mostrar una carpeta Bandeja de salida junto con las demás carpetas del almacén de mensajes. Para más información, consulte [Enviar mensajes usando proveedores de almacenamiento de mensajes](sending-messages-by-using-message-store-providers.md).
  
## <a name="see-also"></a>Vea también



[Implementar carpetas en los almacenes de mensajes](implementing-folders-in-message-stores.md)

