---
title: Admitir texto RTF para proveedores de almacenamiento de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0022fe70-cf11-49a5-9c97-a6bc5b5b13aa
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3e65ebd3ea485ca54978d622e8aaf093dc5eff74
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594071"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a>Admitir texto RTF para proveedores de almacenamiento de mensajes

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Algunas aplicaciones de cliente permiten a los usuarios usar formato de texto enriquecido (RTF) texto en sus mensajes. Si el mensaje almacena las necesidades de proveedor para admitir texto RTF en los mensajes, necesita controlar la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), además de la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)). Principalmente, esto significa que almacenar las dos propiedades y asegurándose de que **PR_BODY** contiene una versión de texto sin formato del texto en **PR_RTF_COMPRESSED**. La función [RTFSync](rtfsync.md) es útil para este propósito. 
  
Hay dos indicadores que se pueden establecer en la propiedad de **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) del objeto de almacén de mensajes que indican a los clientes lo que pueden esperar desde el proveedor de almacén de mensajes con respecto a la **PR_BODY** y **PR_ RTF_COMPRESSED** las propiedades de los mensajes en el almacén de mensajes. El indicador STORE_RTF_OK indica que el almacén puede generar el valor de la propiedad **PR_BODY** de la propiedad **PR_RTF_COMPRESSED** dinámicamente, lo que evita que los clientes de la carga de sincronización de forma explícita. El indicador STORE_UNCOMPRESSED_RTF indica que el proveedor de almacenamiento de mensajes puede admitir datos sin comprimir en **PR_RTF_COMPRESSED**.
  
Los proveedores de almacén de mensajes que no admiten texto RTF necesitan eliminar la propiedad **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) cuando la propiedad **PR_BODY** cambia para que interopere correctamente con las aplicaciones cliente que admiten texto RTF . 
  
## <a name="see-also"></a>Vea también



[Caracter�sticas de almac�n de mensajes](message-store-features.md)

