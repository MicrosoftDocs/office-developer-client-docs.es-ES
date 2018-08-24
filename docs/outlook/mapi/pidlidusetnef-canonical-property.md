---
title: Propiedad canónica PidLidUseTnef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidUseTnef
api_type:
- COM
ms.assetid: 954048d6-e2eb-43e7-b52c-c2f047bb84a4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b0d5588218fd74f005de19daba002cd622c13a17
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587190"
---
# <a name="pidlidusetnef-canonical-property"></a>Propiedad canónica PidLidUseTnef

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Especifica si se deben incluir en un mensaje de formato de encapsulación neutro de transporte (TNEF) cuando ese mensaje se convierte de MAPI al formato de extensiones multipropósito de correo Internet (MIME) o Protocolo Simple de transferencia de correo (SMTP).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidUseTNEF  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008582  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Configuración de tiempo de ejecución  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad especifica si se debe incluir en un mensaje TNEF cuando ese mensaje se convierte de TNEF en formato MIME o SMTP. Esta propiedad puede estar ausente y, si es así, TNEF no debe estar incluido en el mensaje.
  
Esta propiedad sólo se aplica cuando el mensaje se envía desde una cuenta de correo POP3/SMTP y no se aplica cuando se envía el mensaje por otros proveedores, como Microsoft Exchange Server.
  
En determinadas circunstancias, como cuando se habilitan los botones o un OLE incrustados de votación objeto se adjunta a un mensaje, Outlook puede establecer esta propiedad para forzar el uso de TNEF.
  
La propiedad **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) puede utilizarse para exigir la aplicación de sólo texto sin formato y no TNEF, al enviar un mensaje. Debido a que **PidLidUseTNEF** reemplaza el valor de **PR_MSG_EDITOR_FORMAT**, una aplicación que desea forzar el texto sin formato en un mensaje saliente también debe buscar **PidLidUseTNEF** y restablecer a FALSE. Además, el complemento debe quitar las características de mensaje que necesitan TNEF evitar datos adjuntos no se puede utilizar en el mensaje que finalmente se envía. 
  
Uso de la marca **CCSF_USE_TNEF** al llamar a [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) para convertir un mensaje MAPI saliente a una secuencia MIME también puede aplicar TNEF. Esto se aplica incluso si no se ha establecido **PidLidUseTNEF** . 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.
    
[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

