---
title: Compatibilidad con texto RTF para proveedores de almacenamiento de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0022fe70-cf11-49a5-9c97-a6bc5b5b13aa
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: dc1d8a5e237b7b34f3a57e9789e03e2f16237764
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414217"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a>Compatibilidad con texto RTF para proveedores de almacenamiento de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Algunas aplicaciones cliente permiten a los usuarios usar el formato de texto enriquecido (RTF) en sus mensajes. Si su proveedor de almacenamiento de mensajes necesita admitir texto RTF en mensajes, necesita controlar la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), además de la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)). Principalmente, esto significa almacenar ambas propiedades y asegurarse de que **PR_BODY** contiene una versión de texto sin formato del texto en **PR_RTF_COMPRESSED**. La función [RTFSync](rtfsync.md) es útil para este propósito. 
  
Hay dos marcadores que se pueden establecer en la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) del objeto de almacén de mensajes que indican a los clientes lo que pueden esperar del proveedor de almacenamiento de mensajes con respecto a los **PR_BODY** y **PR_ **Propiedades de RTF_COMPRESSED en los mensajes del almacén de mensajes. La marca STORE_RTF_OK indica que el almacén puede generar dinámicamente el valor de la propiedad **PR_BODY** desde la propiedad **PR_RTF_COMPRESSED** , lo que libera a los clientes de la carga de sincronizarlos de forma explícita. La marca STORE_UNCOMPRESSED_RTF indica que el proveedor de almacén de mensajes puede admitir datos sin comprimir en **PR_RTF_COMPRESSED**.
  
Los proveedores de almacenamiento de mensajes que no admiten texto RTF necesitan eliminar la propiedad **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) cuando cambia la propiedad **PR_BODY** para interoperar correctamente con aplicaciones cliente que admiten texto RTF . 
  
## <a name="see-also"></a>Ver también



[Caracter�sticas de almac�n de mensajes](message-store-features.md)

