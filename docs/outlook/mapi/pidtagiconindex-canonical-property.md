---
title: Propiedad canónica PidTagIconIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIconIndex
api_type:
- HeaderDef
ms.assetid: 35bb0d6d-41d4-47d6-b161-be3721894201
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 83ab01363d478d197286bfa8f7b5b092a7ffd5a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819588"
---
# <a name="pidtagiconindex-canonical-property"></a>Propiedad canónica PidTagIconIndex

  
  
**Hace referencia a**: Outlook 
  
Contiene un número que indica qué icono que se utilizará al mostrar un grupo de objetos de correo electrónico.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ICON_INDEX  <br/> |
|Identificador:  <br/> |0x1080  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |General de mensajería  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad, si existe, es una sugerencia para el cliente. El cliente puede pasar por alto el valor de esta propiedad. 
  
|**Estado de elemento de correo**|**Índice de icono**|
|:-----|:-----|
|Correo nuevo  <br/> |0xFFFFFFFF  <br/> |
|Publicación  <br/> |0x00000001  <br/> |
|Otro  <br/> |0 x 00000003  <br/> |
|Leer correo  <br/> |0 x 00000100  <br/> |
|Correo no leído  <br/> |0x00000101  <br/> |
|Correo enviado  <br/> |0x00000102  <br/> |
|Correo no enviado  <br/> |0x00000103  <br/> |
|Correo de recepción  <br/> |0x00000104  <br/> |
|Correo respondido  <br/> |0x00000105  <br/> |
|Correo reenviado  <br/> |0x00000106  <br/> |
|Correo remoto  <br/> |0x00000107  <br/> |
|Correo de entrega  <br/> |0x00000108  <br/> |
|Leer correo  <br/> |0x00000109  <br/> |
|Correo de no entrega  <br/> |0x0000010A  <br/> |
|Correo nonread  <br/> |0x0000010B  <br/> |
|Correo Recall_S  <br/> |0x0000010C  <br/> |
|Correo Recall_F  <br/> |0x0000010D  <br/> |
|Seguimiento de correo  <br/> |0x0000010E  <br/> |
|Fuera del correo de office  <br/> |0x0000011B  <br/> |
|Recuperar correo  <br/> |0x0000011C  <br/> |
|Marca de revisión de correo  <br/> |0x00000130  <br/> |
|Contacto  <br/> |0 x 00000200  <br/> |
|Lista de distribución  <br/> |0x00000202  <br/> |
|Azul de nota rápida  <br/> |0x00000300  <br/> |
|Verde de nota rápida  <br/> |0x00000301  <br/> |
|Rosa de nota rápida  <br/> |0x00000302  <br/> |
|Amarillo de nota rápida  <br/> |0x00000303  <br/> |
|Notas de nota rápida  <br/> |0x00000304  <br/> |
|Cita de una sola instancia  <br/> |0 x 00000400  <br/> |
|Cita periódica  <br/> |0x00000401  <br/> |
|Reunión de instancia única  <br/> |0x00000402  <br/> |
|Reunión periódica  <br/> |0x00000403  <br/> |
|Convocatoria de reunión  <br/> |0 x 00000404  <br/> |
|Accept  <br/> |0x00000405  <br/> |
|Rechazar  <br/> |0x00000406  <br/> |
|Tentativly  <br/> |0 x 00000407  <br/> |
|Cancelación  <br/> |0x00000408  <br/> |
|Información de la actualización  <br/> |0 x 00000409  <br/> |
|Tarea o tareas  <br/> |0x00000500  <br/> |
|Sin asignar tarea periódica  <br/> |0x00000501  <br/> |
|Tareas de la persona asignada  <br/> |0x00000502  <br/> |
|Tarea del asignador  <br/> |0x00000503  <br/> |
|Solicitud de tarea  <br/> |0x00000504  <br/> |
|Aceptación de la tarea  <br/> |0x00000505  <br/> |
|Rechazo de tareas  <br/> |0x00000506  <br/> |
|Conversación de diario  <br/> |0x00000601  <br/> |
|Mensaje de correo electrónico de diario  <br/> |0x00000602  <br/> |
|Convocatoria de reunión de diario  <br/> |0x00000603  <br/> |
|Respuesta a la reunión diario  <br/> |0x00000604  <br/> |
|Solicitud de tarea de diario  <br/> |0x00000606  <br/> |
|Respuesta de tarea de diario  <br/> |0x00000607  <br/> |
|Nota de Journal  <br/> |0x00000608  <br/> |
|Fax de diario  <br/> |0x00000609  <br/> |
|Llamada de teléfono de diario  <br/> |0x0000060A  <br/> |
|Letra de diario  <br/> |0x0000060C  <br/> |
|Diario de Microsoft Office Word  <br/> |0x0000060D  <br/> |
|Diario de Microsoft Office Excel  <br/> |0x0000060E  <br/> |
|Diario de Microsoft Office PowerPoint  <br/> |0x0000060F  <br/> |
|Diario de Microsoft Office Access  <br/> |0x00000610  <br/> |
|Documento de diario  <br/> |0x00000612  <br/> |
|Reunión de diario  <br/> |0x00000613  <br/> |
|Cancelación de reunión de diario  <br/> |0x00000614  <br/> |
|Sesión remota de diario  <br/> |0x00000615  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten en los contactos y las listas de distribución personal.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

