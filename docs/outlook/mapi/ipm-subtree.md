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
ms.openlocfilehash: eebc029d4ed72f355170710061c4d3717ed0aa1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817871"
---
# <a name="ipm-subtree"></a>Subárbol IPM

  
  
**Hace referencia a**: Outlook 
  
MAPI, crea un árbol de carpetas bajo la carpeta raíz de un almacén de mensajes para todos los clientes que envían y reciben mensajes desde humana, en lugar de equipo, los destinatarios. Mensajes que se intercambian entre destinatarios humanos se conocen como mensajes interpersonales y este árbol se conoce como mensajes interpersonales o IPM, del subárbol. 
  
Un subárbol IPM de un almacén de entrega consta de al menos las siguientes carpetas:
  
- Bandeja de entrada
    
- Bandeja de salida
    
- Elementos enviados
    
- Elementos eliminados
    
Estos son los nombres predeterminados y los roles para cada una de estas carpetas; un cliente puede especificar sus propio nombres si los nombres predeterminados no son adecuados. MAPI asigna nombres predeterminados y asociaciones para estas carpetas mantener los mensajes sin darse cuenta desaparece si un cliente no establecer carpetas receptora para los mensajes. 
  
En un contexto de Microsoft Office Outlook, un subárbol IPM consta de las carpetas predeterminadas adicionales para el calendario, contactos, tareas, notas y diario.
  
Normalmente, la Bandeja de entrada contiene los mensajes entrantes y la Bandeja de salida contiene los mensajes salientes (es decir, espera que se envíen mensajes). La carpeta Elementos enviados contiene una copia de cada mensaje enviado si el cliente ha establecido la propiedad **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) en el identificador de entrada de esta carpeta. La carpeta Elementos eliminados contiene mensajes marcados para eliminación. 
  
## <a name="see-also"></a>Vea también



[Carpetas de MAPI](mapi-folders.md)

