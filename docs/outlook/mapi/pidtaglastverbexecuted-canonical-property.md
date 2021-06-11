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
ms.openlocfilehash: 9abd4eb955428595ebe41ab9b2c661303ee2779a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279618"
---
# <a name="pidtaglastverbexecuted-canonical-property"></a>Propiedad canónica PidTagLastVerbExecuted

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el último verbo ejecutado.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_LAST_VERB_EXECUTED  <br/> |
|Identificador:  <br/> |0x1081  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Historial  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad puede tener uno de los siguientes valores:
  
|**Verb**|**Valor de la propiedad**|
|:-----|:-----|
|Publicación  <br/> |0x00000001  <br/> |
|Otros  <br/> |0x00000003  <br/> |
|Leer correo  <br/> |0x00000100  <br/> |
|Correo no leído  <br/> |0x00000101  <br/> |
|Correo enviado  <br/> |0x00000102  <br/> |
|Correo no enviado  <br/> |0x00000103  <br/> |
|Correo de recibo  <br/> |0x00000104  <br/> |
|Correo contestado  <br/> |0x00000105  <br/> |
|Correo reenviado  <br/> |0x00000106  <br/> |
|Correo remoto  <br/> |0x00000107  <br/> |
|Recibo de entrega  <br/> |0x00000108  <br/> |
|Recibo de lectura  <br/> |0x00000109  <br/> |
|Nondelivery Receipt  <br/> |0x0000010A  <br/> |
|Recibo no leído  <br/> |0x0000010B  <br/> |
|Recall_S correo electrónico  <br/> |0x0000010C  <br/> |
|Recall_F correo electrónico  <br/> |0x0000010D  <br/> |
|Seguimiento del correo  <br/> |0x0000010E  <br/> |
|Correo no Office correo  <br/> |0x0000011B  <br/> |
|Recuperar correo  <br/> |0x0000011C  <br/> |
|Correo rastreado  <br/> |0x00000139  <br/> |
|Contacto  <br/> |0x00000200  <br/> |
|Lista de distribución  <br/> |0x00000201  <br/> |
|Nota pegajosa, azul  <br/> |0x00000300  <br/> |
|Nota pegajosa, Verde  <br/> |0x00000301  <br/> |
|Nota pegajosa, rosa  <br/> |0x00000302  <br/> |
|Nota pegajosa, amarilla  <br/> |0x00000303  <br/> |
|Nota pegajosa, Blanco  <br/> |0x00000304  <br/> |
|Cita de instancia única  <br/> |0x00000400  <br/> |
|Cita periódica  <br/> |0x00000401  <br/> |
|Reunión de instancia única  <br/> |0x00000402  <br/> |
|Reunión periódica  <br/> |0x00000403  <br/> |
|Solicitud de reunión /Actualización completa  <br/> |0x00000404  <br/> |
|Aceptar  <br/> |0x00000405  <br/> |
|Declinar  <br/> |0x00000406  <br/> |
|Aceptar provisionalmente  <br/> |0x00000407  <br/> |
|Cancelación  <br/> |0x00000408  <br/> |
|Actualización informativo  <br/> |0x00000409  <br/> |
|Actualización de tareas/tareas  <br/> |0x00000500  <br/> |
|Tarea periódica sinsignar  <br/> |0x00000501  <br/> |
|Tarea del usuario asignado  <br/> |0x00000502  <br/> |
|Tarea del asignador  <br/> |0x00000503  <br/> |
|Solicitud de tarea  <br/> |0x00000504  <br/> |
|Aceptación de tareas  <br/> |0x00000505  <br/> |
|Rechazo de tareas  <br/> |0x00000506  <br/> |
|Conversación en diario  <br/> |0x00000601  <br/> |
|Mensaje de correo electrónico del diario  <br/> |0x00000602  <br/> |
|Solicitud de reunión de diario  <br/> |0x00000603  <br/> |
|Respuesta de la reunión del diario  <br/> |0x00000604  <br/> |
|Solicitud de tarea de diario  <br/> |0x00000606  <br/> |
|Respuesta de tarea de diario  <br/> |0x00000607  <br/> |
|Nota del diario  <br/> |0x00000608  <br/> |
|Fax de diario  <br/> |0x00000609  <br/> |
|Llamada Teléfono diario  <br/> |0x0000060A  <br/> |
|Tarea Journal  <br/> |0x0000060B  <br/> |
|Carta del diario  <br/> |0x0000060C  <br/> |
|Journal Microsoft Office Word  <br/> |0x0000060D  <br/> |
|Registro de Microsoft Office Excel  <br/> |0x0000060E  <br/> |
|Registro Microsoft Office PowerPoint  <br/> |0x0000060F  <br/> |
|Acceso Microsoft Office diario  <br/> |0x00000610  <br/> |
|Documento de diario  <br/> |0x00000612  <br/> |
|Reunión del diario  <br/> |0x00000613  <br/> |
|Cancelación de reunión de diario  <br/> |0x00000614  <br/> |
|Sesión remota de diario  <br/> |0x00000615  <br/> |
|Nuevo correo  <br/> |0xFFFFFFFF  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> 
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

