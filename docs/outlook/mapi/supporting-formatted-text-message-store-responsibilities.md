---
title: Compatibilidad con las responsabilidades del almacén de mensajes de texto con formato
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a97993c2-52e4-4b71-ac03-2c02d82447d8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 502ba82279664638c8e7e4ae68f74df74758918d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435519"
---
# <a name="supporting-formatted-text-message-store-responsibilities"></a>Admitir texto con formato: responsabilidades del almacén de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de almacén de mensajes usan la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) para publicar si pueden controlar el formato de texto enriquecido (RTF), el texto HTML y, si son compatibles con RTF, si almacenan el texto con formato en un formato comprimido o sin comprimir. Los proveedores de almacén de mensajes indican que son compatible con RTF estableciendo el bit STORE_RTF_OK y que almacenan el texto con formato en un formulario sin comprimir estableciendo el STORE_UNCOMPRESSED_RTF bits. Los proveedores de almacén de mensajes indican que son conscientes de HTML estableciendo el STORE_HTML_OK bit.
  
Aunque es importante que un cliente compatible con RTF compruebe el bit STORE_RTF_OK para determinar si un almacén de mensajes admite RTF, no es necesario que un cliente se preocupa por el formato del texto con formato de un almacén compatible con RTF. 
  
Todos los almacenes de mensajes deben admitir clientes que no son compatibles con RTF. Un almacén de mensajes no compatible con RTF debe eliminar la propiedad **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) durante una llamada al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del mensaje si un cliente ha cambiado **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) sin actualizar **PR_RTF_IN_SYNC** o **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). Al eliminar **PR_RTF_IN_SYNC** hace **que la propiedad PR_RTF_COMPRESSED** se vuelva a compilar desde la propiedad **PR_BODY** la próxima vez que un cliente compatible con RTF llame a [RTFSync](rtfsync.md). 
  
La mayoría de los almacenes de mensajes compatible con RTF no reciben el texto del mensaje por parte de los clientes; debe calcularse a petición. Dado que este cálculo requiere mucho tiempo y es caro, los clientes **deben usar** PR_RTF_COMPRESSED siempre que sea posible. Para calcular la **PR_BODY,** el proveedor del almacén de mensajes debe descomprimir el contenido de la propiedad **PR_RTF_COMPRESSED** y quitar el formato de texto enriquecido. Los clientes que no admiten **la propiedad PR_RTF_COMPRESSED** requieren que este cálculo se realice para cada mensaje. 
  
Al copiar mensajes, los proveedores de almacenes de mensajes que no usan los métodos **IMAPISupport::D oCopyProps** o **IMAPISupport::D oCopyTo** corren el riesgo de crear un mensaje sin contenido si su implementación excluye la propiedad **PR_BODY** y se basa en **PR_RTF_COMPRESSED**. Es posible que los datos de la **propiedad PR_RTF_COMPRESSED** esté dañado. Antes de excluir cualquiera de estas propiedades de contenido de mensaje en la operación de copia, compruebe si hay daños de la siguiente manera: 
  
1. Si el valor de **PR_RTF_COMPRESSED** no es mayor que el RTF comprimido, la propiedad está dañada. 
    
2. Si el valor mágico del encabezado RTF no es  _dwMagicCompressedRTF_ o  _dwMagicUncompressedRTF,_ la propiedad está dañada.
    
Los proveedores de almacén de mensajes que usan los métodos de soporte técnico no necesitan preocuparse por implementar una comprobación de PR_RTF_COMPRESSED **daños;** MAPI garantiza que las propiedades adecuadas existen y son válidas. 
  
Hay tres niveles diferentes de compatibilidad rtf que los proveedores de almacenes de mensajes pueden implementar; MAPI recomienda que los proveedores de almacén de mensajes compatibles con RTF implementen su compatibilidad en el nivel medio o superior. Todos los proveedores de almacenes de  mensajes que admiten RTF se encargan de generar PR_BODY a partir de los datos incluidos en **PR_RTF_COMPRESSED** en los mensajes salientes y realizar una llamada a **RTFSync** para sincronizar el texto y el formato de los mensajes entrantes. 
  
Las diferencias entre estos tres niveles se describen en la tabla siguiente. 
  
|**Nivel de soporte**|**Descripción**|
|:-----|:-----|
|Bajo  <br/> |El proveedor del almacén de mensajes llama a **RTFSync** siempre que se guardan los cambios en un mensaje y extrae los datos de la propiedad **PR_BODY** de **PR_RTF_COMPRESSED** en lugar de requerir que los clientes la establezcan. Tanto **PR_BODY** como **PR_RTF_COMPRESSED** se almacenan.  <br/> |
|Middle  <br/> |El proveedor del almacén de mensajes almacena solo **la PR_RTF_COMPRESSED** propiedad, la información **PR_BODY** cuando sea necesario.  <br/> |
|Alto  <br/> |El proveedor del almacén de mensajes **no almacena PR_BODY** ni las propiedades RTF auxiliares. **RtfSync** se llama cuando el texto del mensaje ha cambiado y el formato permanece sin cambios o cuando un proveedor de transporte descarga un nuevo mensaje.  <br/> |
   

