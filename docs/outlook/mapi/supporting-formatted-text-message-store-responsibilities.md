---
title: Compatibilidad con las responsabilidades del almacén de mensajes con formato de texto
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a97993c2-52e4-4b71-ac03-2c02d82447d8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 301ebbf8e7a3e2a2deb303af5b198fd11511d495
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820780"
---
# <a name="supporting-formatted-text-message-store-responsibilities"></a>Admitir texto con formato: responsabilidades de almacenamiento de mensajes

  
  
**Hace referencia a**: Outlook 
  
Los proveedores de almacén de mensajes usar la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) para publicar o no puede controlar el formato de texto enriquecido (RTF), texto HTML y, si son compatible con RTF, si se almacenan el texto con formato en un formato comprimido o sin comprimir. Los proveedores de almacén de mensajes indican que son conscientes de RTF estableciendo el bit STORE_RTF_OK y que contienen el texto con formato en un formulario sin comprimir estableciendo el bit STORE_UNCOMPRESSED_RTF. Los proveedores de almacén de mensajes indican que son compatibles con HTML estableciendo el bit STORE_HTML_OK.
  
Aunque es importante para un cliente compatible con RTF comprobar si la STORE_RTF_OK de bit para determinar si admite o no un almacén de mensajes RTF, no es necesario para que un cliente afectados con el formato de texto con formato de un almacén de tener en cuenta RTF. 
  
Todos los almacenes de mensaje deben admitir a clientes ajenos a RTF. Un almacén de mensajes RTF reconozca debe eliminar la propiedad **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) durante una llamada al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del mensaje, si un cliente ha cambiado **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) sin actualización de **PR_RTF_IN_SYNC** o **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). Eliminación de **PR_RTF_IN_SYNC** hace que la propiedad **PR_RTF_COMPRESSED** que volver a calcularse la próxima vez que llama a un cliente compatible con RTF [RTFSync](rtfsync.md)desde la propiedad **PR_BODY** . 
  
Almacenes de mensaje compatibles con RTF mayoría no se le proporciona el texto del mensaje por los clientes; se debe calcular en la solicitud. Dado que este cálculo es largo y costoso, los clientes deben usar **PR_RTF_COMPRESSED** siempre que sea posible. Para calcular la propiedad **PR_BODY** , el proveedor de almacén de mensajes debe descomprimir el contenido de la propiedad **PR_RTF_COMPRESSED** y quitar el formato de texto enriquecido. Los clientes que no admiten la propiedad **PR_RTF_COMPRESSED** requieren este cálculo tengan lugar para todos los mensajes. 
  
Cuando se copian los mensajes, los proveedores que no usan los métodos **IMAPISupport::DoCopyProps** o **IMAPISupport::DoCopyTo** , corre el riesgo de la creación de un mensaje sin contenido si su implementación excluye la **PR_BODY** del almacén de mensajes propiedad y se basa en **PR_RTF_COMPRESSED**. Es posible que los datos de la propiedad **PR_RTF_COMPRESSED** esté dañado. Antes de exclusión de cualquiera de estas propiedades de contenido de mensaje en la operación de copia, compruebe daños en la siguiente manera: 
  
1. Si el valor de **PR_RTF_COMPRESSED** no es mayor que el comprimido RTF, la propiedad está dañada. 
    
2. Si el valor de magia en el encabezado RTF no es _dwMagicCompressedRTF_ o _dwMagicUncompressedRTF_, la propiedad está dañado.
    
Mediante los métodos necesitan a no ser que se trate con la implementación de una comprobación de posibles daños **PR_RTF_COMPRESSED** ; la compatibilidad con los proveedores del almacén de mensajes MAPI se asegura de que las propiedades adecuadas existen y son válidas. 
  
Hay tres niveles diferentes de compatibilidad RTF que se pueden implementar los proveedores de almacén de mensajes; MAPI, se recomienda que los proveedores de almacén de mensajes RTF para implementan su compatibilidad en el nivel intermedio o más alto. Todos los compatible con RTF almacén de mensajes proveedores se encargan de generar **PR_BODY** a partir de los datos incluidos en **PR_RTF_COMPRESSED** en los mensajes salientes y realizar una llamada a **RTFSync** para sincronizar el formato de texto y en los mensajes entrantes. 
  
Las diferencias entre estos tres niveles se describen en la siguiente tabla. 
  
|**Nivel de compatibilidad**|**Descripción**|
|:-----|:-----|
|Low  <br/> |Mensaje de almacenar las llamadas de proveedor **RTFSync** cada vez que se guardan los cambios en un mensaje y extrae los datos para la propiedad **PR_BODY** **PR_RTF_COMPRESSED** en lugar de los clientes que requieren para establecerla. **PR_BODY** y **PR_RTF_COMPRESSED** se almacenan.  <br/> |
|En medio  <br/> |Almacén de mensajes almacenes proveedor sólo la propiedad **PR_RTF_COMPRESSED** , los sistemas **PR_BODY** cuando sea necesario.  <br/> |
|High  <br/> |Almacenes de proveedor de almacén de mensajes ni **PR_BODY** o las propiedades RTF auxiliares. **RTFSync** se llama cuando se ha cambiado el texto del mensaje y el formato permanece inalterado o cuando se descarga un nuevo mensaje de un proveedor de transporte.  <br/> |
   

