---
title: Compatibilidad con responsabilidades del almacén de mensajes de texto con formato
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
  
Los proveedores de almacenamiento de mensajes usan la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) para publicar si pueden administrar o no el formato de texto enriquecido (RTF), el texto HTML y, si son compatibles con RTF, si almacenan el texto con formato en un formato comprimido o sin comprimir. Los proveedores de almacenamiento de mensajes indican que son compatibles con RTF mediante la configuración del bit STORE_RTF_OK y que almacenan el texto con formato en un formulario descomprimido mediante la configuración del bit STORE_UNCOMPRESSED_RTF. Los proveedores de almacenamiento de mensajes indican que son compatibles con HTML mediante la configuración del bit STORE_HTML_OK.
  
Aunque es importante que un cliente compatible con RTF Compruebe el bit STORE_RTF_OK para determinar si un almacén de mensajes admite RTF o no, no es necesario que un cliente se preocupe por el formato de un texto formateado de un almacén con reconocimiento RTF. 
  
Todos los almacenes de mensajes deben admitir clientes no compatibles con RTF. Un almacén de mensajes no compatible con RTF debe eliminar la propiedad **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) durante una llamada al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) de mensaje si un cliente ha cambiado **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) sin actualizar **PR_RTF_IN_SYNC** o **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). La eliminación de **PR_RTF_IN_SYNC** hace que la propiedad **PR_RTF_COMPRESSED** se vuelva a calcular desde la propiedad **PR_BODY** la próxima vez que un cliente compatible con rtf llame a [RTFSync](rtfsync.md). 
  
La mayoría de los almacenes de mensajes que reconocen el formato RTF no reciben el texto del mensaje por parte de los clientes; debe calcularse a petición. Como este cálculo es costoso y lento, los clientes deben usar **PR_RTF_COMPRESSED** siempre que sea posible. Para calcular la propiedad **PR_BODY** , el proveedor de almacén de mensajes debe descomprimir el contenido de la propiedad **PR_RTF_COMPRESSED** y quitar el formato de texto enriquecido. Los clientes que no admiten la propiedad **PR_RTF_COMPRESSED** requieren que este cálculo tenga lugar para cada mensaje. 
  
Al copiar mensajes, los proveedores de almacenamiento de mensajes que no usan los métodos **IMAPISupport::D ocopyprops** o **IMAPISupport::D ocopyto** ejecutan el riesgo de crear un mensaje sin contenido si su implementación excluye el **PR_BODY** y se basa en **PR_RTF_COMPRESSED**. Es posible que los datos de la propiedad **PR_RTF_COMPRESSED** estén dañados. Antes de excluir cualquiera de estas propiedades de contenido de mensaje en la operación de copia, compruebe si hay daños como se indica a continuación: 
  
1. Si el valor de **PR_RTF_COMPRESSED** no es mayor que el formato RTF comprimido, la propiedad está dañada. 
    
2. Si el valor mágico en el encabezado RTF no es _dwMagicCompressedRTF_ o _dwMagicUncompressedRTF_, la propiedad está dañada.
    
No es necesario que los proveedores de almacenamiento de mensajes que usan los métodos de soporte técnico implementen una comprobación de daños en la **PR_RTF_COMPRESSED** ; MAPI garantiza que las propiedades apropiadas existan y sean válidas. 
  
Hay tres niveles diferentes de compatibilidad con RTF que los proveedores de almacenamiento de mensajes pueden implementar; MAPI recomienda que los proveedores de almacenamiento de mensajes con formato RTF implementen la compatibilidad en el nivel intermedio o superior. Todos los proveedores de almacenamiento de mensajes que reconocen RTF se ocupan de generar **PR_BODY** a partir de los datos incluidos en **PR_RTF_COMPRESSED** en los mensajes salientes y realizar una llamada a **RTFSync** para sincronizar el texto y el formato de los mensajes entrantes. 
  
En la tabla siguiente se describen las diferencias entre estos tres niveles. 
  
|**Nivel de soporte**|**Descripción**|
|:-----|:-----|
|Bajo  <br/> |El proveedor de almacenamiento de mensajes llama a **RTFSync** siempre que los cambios se guardan en un mensaje y extraen los datos de la propiedad **PR_BODY** de **PR_RTF_COMPRESSED** en lugar de requerir a los clientes que lo establezcan. Se almacenan tanto **PR_BODY** como **PR_RTF_COMPRESSED** .  <br/> |
|Mediados  <br/> |El proveedor de almacenamiento de mensajes solo almacena la propiedad **PR_RTF_COMPRESSED** , calculando **PR_BODY** cuando sea necesario.  <br/> |
|Alto  <br/> |El proveedor de almacenamiento de mensajes no almacena ninguna **PR_BODY** o las propiedades de RTF auxiliares. Se llama a **RTFSync** cuando el texto del mensaje ha cambiado y el formato permanece inalterado o cuando un proveedor de transporte descarga un nuevo mensaje.  <br/> |
   

