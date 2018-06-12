---
title: TABLE_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.TABLE_NOTIFICATION
api_type:
- COM
ms.assetid: 48e478c4-6e9a-40ab-a7bb-e6219b743b08
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: fd77473ce728a51220a4c039f1d12d03d90e7f36
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820848"
---
# <a name="tablenotification"></a>TABLE_NOTIFICATION

**Se aplica a**: Outlook 
  
Describe una fila en una tabla que se ha visto afectada por algún tipo de evento, como un cambio o un error. Esto hace que una notificación de la tabla que se genere. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _TABLE_NOTIFICATION
{
  ULONG ulTableEvent;
  HRESULT hResult;
  SPropValue propIndex;
  SPropValue propPrior;
  SRow row;
} TABLE_NOTIFICATION;

```

## <a name="members"></a>Miembros

**ulTableEvent**
  
> Máscara de bits de indicadores que se utilizan para representar el tipo de evento de la tabla. Se pueden establecer los siguientes indicadores:
    
TABLE_CHANGED 
  
> Indica a un nivel alto, que ha cambiado algo acerca de la tabla. Estado de la tabla es tal como estaba antes del evento. Esto significa que todas las propiedades **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), marcadores, la posición actual y las selecciones de interfaz de usuario siguen siendo válidas. Controlar este evento por volver a leer la tabla. Proveedores de servicios que no desea implementar notificaciones de tabla enriquecido envían eventos TABLE_CHANGED en lugar de eventos más detallados para indicar un determinado tipo de cambio. 
    
TABLE_ERROR 
  
> Se ha producido un error normalmente durante el procesamiento de una operación asincrónica. Errores durante el procesamiento de los métodos siguientes pueden generar este evento: 
    
   - [SortTable](imapitable-sorttable.md)
    
   - [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
   - [IMAPITable:: Restrict](imapitable-restrict.md)
    
   Después de recibir un evento TABLE_ERROR, un cliente no puede confiar en la precisión de la tabla de contenido. Además, las notificaciones sobre otros cambios pendientes se pueden perder. El método [IMAPITable::GetLastError](imapitable-getlasterror.md) no es posible que proporciona información adicional sobre el error ya que se generó en algún momento anterior, no necesariamente desde la última llamada al método. 
    
TABLE_RELOAD 
  
> Deben volver a cargar los datos en la tabla. Proveedores de servicios de envían TABLE_RELOAD cuando, por ejemplo, los datos subyacentes se almacenan en una base de datos y la base de datos se ha reemplazado. Controlar este evento por suponiendo que nada acerca de la tabla todavía es válido y volviendo a leerlo en la tabla. Todos los marcadores, las claves de la instancia, estado e información de posición no son válidos.
    
TABLE_RESTRICT_DONE 
  
> Ha finalizado una operación de restricción que se inició con una llamada al método **IMAPITable:: Restrict** . 
    
TABLE_ROW_ADDED 
  
> Se agregó una nueva fila a la tabla y el correspondiente objeto guardado. Eventos TABLE_ROW_ADDED se generan después de una llamada al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . 
    
TABLE_ROW_DELETED 
  
> Se ha quitado una fila de la tabla. El miembro **propPrior** se establece en NULL. 
    
TABLE_ROW_MODIFIED 
  
> Se ha modificado una fila. El miembro de **fila** contiene las propiedades afectadas para la fila. Varios eventos TABLE_ROW_MODIFIED se envían en el orden en que aparecen en la vista de tabla. 
    
  Eventos TABLE_ROW_MODIFIED se envían después de los cambios realizados en el objeto correspondiente se han confirmado con una llamada al método **IMAPIProp::SaveChanges** . Si la fila modificada ahora es la primera fila en la tabla, el valor de la etiqueta de propiedad en el miembro **propPrior** es **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).
    
TABLE_SETCOL_DONE 
  
> Ha finalizado una operación de configuración de columna iniciada con una llamada al método **IMAPITable::SetColumns** . 
    
TABLE_SORT_DONE 
  
> Se ha completado una operación iniciada con una llamada al método **SortTable** de ordenación de la tabla. 
    
**hResult**
  
> Valor HRESULT del error que se ha producido, si se establece el miembro **ulTableEvent** en TABLE_ERROR. 
    
**propIndex**
  
> Estructura de [SPropValue](spropvalue.md) para la propiedad **PR_INSTANCE_KEY** de la fila afectada. 
    
**propPrior**
  
> Estructura de **SPropValue** para la propiedad **PR_INSTANCE_KEY** de la fila antes de la afectados. Si la fila afectada es la primera fila en la tabla, se debe establecer **propPrior** a **PR_NULL** y no cero. Cero no es una etiqueta de propiedad válido. 
    
**fila**
  
> Estructura de [SRow](srow.md) que describe la fila afectada. Esta estructura se rellena para todos los eventos de notificación de la tabla. Para los eventos de notificación de tabla que no pasan la fila de datos, el miembro **cValues** de la estructura **SRow** se establece en cero y el miembro **lpProps** se establece en NULL. Debido a que esta estructura **SRow** es de sólo lectura; los clientes deben realizar una copia de la misma si desean hacer modificaciones. La función [ScDupPropset](scduppropset.md) puede utilizarse para realizar la copia. 
    
## <a name="remarks"></a>Notas

El **tabla\_notificación** estructura es uno de los miembros de la unión de estructuras incluidos en el miembro de la **información** de la estructura de [notificación](notification.md) . El miembro **info** incluye un **tabla\_notificación** estructurar cuando el miembro **ulEventType** de la estructura está establecido en _fnevTableModified_.
  
El orden y el tipo de columnas en el miembro de fila que refleje el orden y el tipo que estaba en efecto en el momento en que se generó la notificación. El orden y el tipo en el momento en que se generó la notificación no es necesariamente el mismo que cuando se entregó la notificación. 
  
Para obtener más información acerca de las notificaciones, vea los temas que se describen en la siguiente tabla.
  
|**Tema**|**Descripción**|
|:-----|:-----|
|[Notificación de eventos en MAPI](event-notification-in-mapi.md) <br/> |Descripción general de notificación y eventos de notificación.  <br/> |
|[Administrar notificaciones](handling-notifications.md) <br/> |Explicación de cómo los clientes deben controlar las notificaciones.  <br/> |
|[Compatibilidad con la notificación de eventos](supporting-event-notification.md) <br/> |Explicación de cómo los proveedores de servicios pueden usar el método **IMAPISupport** para generar notificaciones.  <br/> |
   
Debido a que las notificaciones de tabla son asincrónicas, los clientes pueden recibir notificaciones de una fila se ha agregado después de aprendizaje acerca de la adición a través de otro medio. Es posible recibir un evento TABLE_ERROR cuando se ha producido un error en un método **IMAPITable::Sort**, **IMAPITable:: Restrict**o **IMAPITable::SetColumns** o cuando subyacentes de un proceso intenta actualizar una tabla con, por ejemplo, la nueva funcionalidad o las filas modificadas. 
  
## <a name="see-also"></a>Ver también

- [Notificaci�n](notification.md) 
- [ScDupPropset](scduppropset.md)
- [SRow](srow.md)
- [SPropValue](spropvalue.md)
- [Estructuras MAPI](mapi-structures.md)

