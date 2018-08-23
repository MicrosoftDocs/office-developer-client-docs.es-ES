---
title: DTBLCHECKBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLCHECKBOX
api_type:
- COM
ms.assetid: 0dd12990-5431-4768-9d64-27d4ef6b7b20
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fa7f6ac116bf5255d2598465085bab2695ae2c25
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564517"
---
# <a name="dtblcheckbox"></a>DTBLCHECKBOX

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene información acerca de una casilla de verificación que se usará en un cuadro de diálogo creado a partir de una tabla para mostrar. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Macro relacionado:  <br/> |[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |
   
```cpp
typedef struct _DTBLCHECKBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRPropertyName;
} DTBLCHECKBOX, FAR *LPDTBLCHECKBOX;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Posición en la memoria de la cadena de caracteres que se muestra con la casilla de verificación. 
    
 **ulFlags**
  
> Máscara de bits de indicadores que se utilizan para designar el formato de la etiqueta de la casilla de verificación. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> La etiqueta está en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., la etiqueta está en formato ANSI.
    
 **ulPRPropertyName**
  
> Etiqueta de propiedad de una propiedad de tipo PT_BOOLEAN. El valor de esta propiedad se ve afectado por el estado de la casilla de verificación.
    
## <a name="remarks"></a>Comentarios

Una estructura **DTBLCHECKBOX** describe una casilla de verificación un control que refleja uno de los dos estados: habilitado (un cuadro checked) o deshabilitado (un cuadro vacío). 
  
El miembro **ulPRPropertyName** describe una propiedad booleana cuyo valor se manipula cambiando el estado de la casilla de verificación. Cuando la casilla de verificación aparece por primera vez, MAPI llama al método **GetProps** de la implementación de **IMAPIProp** que está asociado a la tabla para mostrar que se va a recuperar un conjunto de propiedades predeterminadas. Si una de las propiedades se asigna a la etiqueta de propiedad de la estructura de **DTBLCHECKBOX** , se muestra el valor de esa propiedad como valor inicial de la casilla de verificación. 
  
Controles de casilla de verificación pueden ser modificables. Esto permite que un usuario cambiar su estado. Las casillas de verificación modificables establecer la marca DT_EDITABLE en el miembro **ulCtlFlags** de su estructura [DTCTL](dtctl.md) y en su propiedad **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)). Cuando una casilla de verificación cambia su estado, MAPI llama a [IMAPIProp::SetProps](imapiprop-setprops.md) para establecer la propiedad identificada en el miembro de la etiqueta de propiedad de la estructura **DTBLCHECKBOX** en el nuevo estado. 
  
Por ejemplo, un proveedor de la libreta de direcciones puede incluir un control de casilla de verificación modificable en su cuadro de diálogo de configuración para ajustar la configuración de propiedad de **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) de un destinatario. Cuando el usuario selecciona la casilla de verificación, MAPI establece esta propiedad en TRUE. Cuando la casilla de verificación está seleccionada, la propiedad se establece en FALSE.
  
Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md). Para obtener información acerca de cómo implementar una tabla para mostrar, vea [implementar una tabla mostrar](display-table-implementation.md). Para obtener información acerca de los tipos de propiedad, vea [Información general sobre el tipo de propiedad MAPI](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Recursos adicionales



[DTCTL](dtctl.md)
  
[Propiedad canónica PidTagControlType](pidtagcontroltype-canonical-property.md)


[Estructuras MAPI](mapi-structures.md)

