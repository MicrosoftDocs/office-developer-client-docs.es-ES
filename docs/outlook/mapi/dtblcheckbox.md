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
ms.openlocfilehash: ed0bbe986f374648e2ee85f3a0d2dfe7bc392e0f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287272"
---
# <a name="dtblcheckbox"></a>DTBLCHECKBOX

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene información sobre una casilla de verificación que se utilizará en un cuadro de diálogo generado a partir de una tabla de presentación. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Macro relacionada:  <br/> |[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |
   
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
  
> Máscara de la máscara usada para designar el formato de la etiqueta de casilla de verificación. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> La etiqueta está en formato Unicode. Si no se establece la marca MAPI_UNICODE, la etiqueta está en formato ANSI.
    
 **ulPRPropertyName**
  
> Etiqueta de propiedad de una propiedad de tipo PT_BOOLEAN. El valor de esta propiedad se ve afectado por el estado de la casilla.
    
## <a name="remarks"></a>Comentarios

Una estructura **DTBLCHECKBOX** describe una casilla de verificación de un control que refleja uno de los dos Estados: habilitado (casilla activada) o deshabilitado (un cuadro vacío). 
  
El miembro **ulPRPropertyName** describe una propiedad booleana cuyo valor se manipula cambiando el estado de la casilla de verificación. Cuando la casilla aparece por primera vez, MAPI llama al método **GetProps** de la implementación de **IMAPIProp** asociada a la tabla de presentación para recuperar un conjunto de propiedades predeterminadas. Si una de las propiedades se asigna a la etiqueta de propiedad en la estructura **DTBLCHECKBOX** , el valor de esa propiedad se muestra como el valor inicial de la casilla de verificación. 
  
Los controles de casilla de verificación pueden poder modificarse. Esto permite a un usuario cambiar sus Estados. Las casillas de verificación modificables establecen la marca DT_EDITABLE en el miembro **ulCtlFlags** de su estructura [DTCTL](dtctl.md) y en su propiedad **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)). Cuando una casilla de verificación cambia su estado, MAPI llama a [IMAPIProp:: SetProps](imapiprop-setprops.md) para establecer la propiedad identificada en el miembro de etiqueta de propiedad de la estructura **DTBLCHECKBOX** en el nuevo estado. 
  
Por ejemplo, un proveedor de libreta de direcciones puede incluir un control de casilla de verificación modificable en su cuadro de diálogo de configuración para ajustar la configuración de la propiedad **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) de un destinatario. Cuando el usuario selecciona la casilla de verificación, MAPI establece esta propiedad en TRUE. Cuando no se selecciona la casilla de verificación, la propiedad se establece en FALSE.
  
Para obtener información general sobre las tablas de presentación, consulte [Display tables](display-tables.md). Para obtener información acerca de cómo implementar una tabla de visualización, consulte [Implementing a display Table](display-table-implementation.md). Para obtener información acerca de los tipos de propiedades, consulte [MAPI Property Type Overview](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Vea también



[DTCTL](dtctl.md)
  
[Propiedad canónica PidTagControlType](pidtagcontroltype-canonical-property.md)


[Estructuras MAPI](mapi-structures.md)

