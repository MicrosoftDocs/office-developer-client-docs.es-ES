---
title: Propiedad canónica PidTagMessageEditorFormat
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageEditorFormat
api_type:
- HeaderDef
ms.assetid: 197b21ed-9f2f-425f-a6ed-cae1208fa2ca
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 029df4397f4d24c7c111d2017d34e6403df367d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325637"
---
# <a name="pidtagmessageeditorformat-canonical-property"></a>Propiedad canónica PidTagMessageEditorFormat

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica el formato de un editor que se usará para mostrar un mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MSG_EDITOR_FORMAT  <br/> |
|Identificador:  <br/> |0x5909  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Varios  <br/> |
   
## <a name="remarks"></a>Comentarios

Los valores posibles **para PR_MSG_EDITOR_FORMAT** pueden ser uno de los siguientes: 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|**EDITOR_FORMAT_DONTKNOW** <br/> |El formato para el editor que se va a usar es desconocido.  <br/> |
|**EDITOR_FORMAT_PLAINTEXT** <br/> |El editor debe mostrar el mensaje en formato de texto sin formato.  <br/> |
|**EDITOR_FORMAT_HTML** <br/> |El editor debe mostrar el mensaje en formato HTML.  <br/> |
|**EDITOR_FORMAT_RTF** <br/> |El editor debe mostrar el mensaje en formato de texto enriquecido.  <br/> |
   
De forma predeterminada, los mensajes de correo (con la clase de **mensaje IPM. Nota** o con una clase de mensaje personalizada derivada de **IPM. Nota)** Los envíos desde una cuenta de correo POP3/SMTP se envían en el formato de encapsulación neutro para el transporte (TNEF). La **PR_MSG_EDITOR_FORMAT** puede usarse para aplicar solo texto sin formato, y no TNEF, al enviar un mensaje. Si **PR_MSG_EDITOR_FORMAT** se establece **en EDITOR_FORMAT_PLAINTEXT**, el mensaje se envía como texto sin formato sin TNEF. Si **PR_MSG_EDITOR_FORMAT** se establece en **EDITOR_FORMAT_RTF,** la codificación TNEF está habilitada implícitamente y el mensaje se envía mediante el formato predeterminado de Internet especificado en el cliente de Outlook.
  
Existen otras dos formas de exigir el uso de TNEF al enviar un mensaje.
  
- Establecer la propiedad con nombre **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) en True en un mensaje indica que se debe incluir TNEF al convertir el mensaje de MAPI a MIME/SMTP. Tenga en cuenta que **dispidUseTNEF** solo se aplica cuando el mensaje se envía desde una cuenta de correo POP3/SMTP y no se aplica cuando otros proveedores envían el mensaje, como Microsoft Exchange Server. **dispidUseTNEF** invalida la configuración en **PR_MSG_EDITOR_FORMAT**.
    
- El uso **CCSF_USE_TNEF** marca al llamar a [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) para convertir un mensaje MAPI saliente en una secuencia MIME también puede exigir TNEF. Esto se aplica incluso si **dispidUseTNEF** no está establecido. 
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Define las estructuras de datos básicas que se usan en operaciones remotas.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones permitidas para los objetos de mensaje de correo electrónico.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

