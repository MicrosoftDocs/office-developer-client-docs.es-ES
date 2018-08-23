---
title: Propiedad canónica PidTagLastVerbExecuted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLastVerbExecuted
api_type:
- HeaderDef
ms.assetid: 502f0261-697f-41bf-8530-75e1d0f503e5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fe75a242772441b23d3aaa87fc57486d1f074914
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581660"
---
# <a name="pidtaglastverbexecuted-canonical-property"></a>Propiedad canónica PidTagLastVerbExecuted

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el último verbo que se ejecuta.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_LAST_VERB_EXECUTED  <br/> |
|Identificador:  <br/> |0x1081  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Historial  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad puede tener uno de los siguientes valores:
  
|**Verbo**|**Valor de la propiedad**|
|:-----|:-----|
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
|Confirmación de entrega  <br/> |0x00000108  <br/> |
|Confirmación de lectura  <br/> |0x00000109  <br/> |
|Confirmación de no entrega  <br/> |0x0000010A  <br/> |
|Recepción nonread  <br/> |0x0000010B  <br/> |
|Correo Recall_S  <br/> |0x0000010C  <br/> |
|Correo Recall_F  <br/> |0x0000010D  <br/> |
|Seguimiento de correo  <br/> |0x0000010E  <br/> |
|Fuera del correo de Office  <br/> |0x0000011B  <br/> |
|Recuperar correo  <br/> |0x0000011C  <br/> |
|Marca de revisión de correo  <br/> |0x00000139  <br/> |
|Contacto  <br/> |0 x 00000200  <br/> |
|Lista de distribución  <br/> |0x00000201  <br/> |
|Nota rápida, azul  <br/> |0x00000300  <br/> |
|Nota rápida, verde  <br/> |0x00000301  <br/> |
|Nota rápida, rosa  <br/> |0x00000302  <br/> |
|Nota rápida, amarillo  <br/> |0x00000303  <br/> |
|Nota rápida, blanco  <br/> |0x00000304  <br/> |
|Cita de una sola instancia  <br/> |0 x 00000400  <br/> |
|Cita periódica  <br/> |0x00000401  <br/> |
|Reunión de instancia única  <br/> |0x00000402  <br/> |
|Reunión periódica  <br/> |0x00000403  <br/> |
|Solicitud de reunión / completo de la actualización  <br/> |0 x 00000404  <br/> |
|Aceptar  <br/> |0x00000405  <br/> |
|Rechazar  <br/> |0x00000406  <br/> |
|Aceptar provisionalmente  <br/> |0 x 00000407  <br/> |
|Cancelación  <br/> |0x00000408  <br/> |
|Información de la actualización  <br/> |0 x 00000409  <br/> |
|Actualización de la tarea o tareas  <br/> |0x00000500  <br/> |
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
|Tareas de diario  <br/> |0x0000060B  <br/> |
|Letra de diario  <br/> |0x0000060C  <br/> |
|Diario de Microsoft Office Word  <br/> |0x0000060D  <br/> |
|Diario de Microsoft Office Excel  <br/> |0x0000060E  <br/> |
|Diario de Microsoft Office PowerPoint  <br/> |0x0000060F  <br/> |
|Diario de Microsoft Office Access  <br/> |0x00000610  <br/> |
|Documento de diario  <br/> |0x00000612  <br/> |
|Reunión de diario  <br/> |0x00000613  <br/> |
|Cancelación de reunión de diario  <br/> |0x00000614  <br/> |
|Sesión remota de diario  <br/> |0x00000615  <br/> |
|Correo nuevo  <br/> |0xFFFFFFFF  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> 
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

