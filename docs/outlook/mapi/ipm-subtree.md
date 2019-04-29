---
title: Subárbol IPM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b5fc6084-722d-44e8-8637-f4160a4fb19b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 92c7a09d9d608ac31920d49b20f78bedd26f5fcd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421224"
---
# <a name="ipm-subtree"></a>Subárbol IPM

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI crea un árbol de carpetas debajo de la carpeta raíz de un almacén de mensajes para todos los clientes que envían y reciben mensajes de los destinatarios humanos, no de los equipos. Los mensajes intercambiados entre destinatarios humanos se denominan mensajes interpersonales y este árbol se conoce como mensaje interpersonal, o subárbol IPM. 
  
Un subárbol IPM para un almacén de entrega consta de al menos las siguientes carpetas:
  
- Bandeja de entrada
    
- Bandeja de salida
    
- Elementos enviados
    
- Elementos eliminados
    
Estos son los nombres y los roles predeterminados de cada una de estas carpetas; un cliente puede especificar sus propios nombres si los nombres predeterminados no son apropiados. MAPI asigna nombres y asociaciones predeterminados para estas carpetas para evitar que los mensajes desaparezcan de forma inadvertida si un cliente no establece carpetas de recepción para los mensajes. 
  
En un contexto de Microsoft Office Outlook, un subárbol IPM consta de carpetas predeterminadas adicionales para calendario, contactos, tareas, notas y diario.
  
Normalmente, la bandeja de entrada retiene los mensajes entrantes y la bandeja de salida retiene los mensajes salientes (es decir, mensajes en espera de enviarse). La carpeta elementos enviados contiene una copia de cada mensaje enviado si el cliente ha establecido la propiedad **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) en el identificador de entrada de esta carpeta. La carpeta elementos eliminados contiene mensajes marcados para su eliminación. 
  
## <a name="see-also"></a>Ver también



[Carpetas de MAPI](mapi-folders.md)

