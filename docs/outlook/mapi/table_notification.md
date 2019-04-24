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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6c35220529fb88b470c563a0b004bfcf7e63ef76
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345650"
---
# <a name="tablenotification"></a>TABLE_NOTIFICATION

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una fila de una tabla que se ha visto afectada por algún tipo de evento, como un cambio o un error. Esto hace que se genere una notificación de tabla. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
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

## <a name="members"></a>Members

**ulTableEvent**
  
> Máscara de las marcas usadas para representar el tipo de evento de tabla. Se pueden establecer los siguientes indicadores:
    
TABLE_CHANGED 
  
> Indica en un nivel alto que algo sobre la tabla ha cambiado. El estado de la tabla es como estaba antes del evento. Esto significa que todas las propiedades, marcadores, posicionamiento actual y selecciones de la interfaz de usuario de **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) siguen siendo válidos. Controle este evento volviendo a leer la tabla. Los proveedores de servicios que no desean implementar notificaciones de tablas enriquecidas envían eventos de TABLE_CHANGED en lugar de eventos más detallados para indicar un tipo de cambio determinado. 
    
TABLE_ERROR 
  
> Se ha producido un error, normalmente durante el procesamiento de una operación asincrónica. Los errores producidos durante el procesamiento de los métodos siguientes pueden generar este evento: 
    
   - [IMAPITable::SortTable](imapitable-sorttable.md)
    
   - [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
   - [IMAPITable::Restrict](imapitable-restrict.md)
    
   Después de recibir un evento TABLE_ERROR, un cliente no puede depender de la exactitud del contenido de la tabla. Además, es posible que se pierdan las notificaciones pendientes sobre otros cambios. Es posible que el método [IMAPITable:: GetLastError](imapitable-getlasterror.md) no proporcione información adicional sobre el error porque se generó en algún punto anterior, no necesariamente desde la última llamada al método. 
    
TABLE_RELOAD 
  
> Los datos de la tabla se deben volver a cargar. Los proveedores de servicios envían TABLE_RELOAD cuando, por ejemplo, los datos subyacentes se almacenan en una base de datos y se reemplaza la base de datos. Para controlar este evento, supongamos que no hay nada de la tabla que siga siendo válido y que relea la tabla. Todos los marcadores, claves de instancia, estado e información de posicionamiento no son válidos.
    
TABLE_RESTRICT_DONE 
  
> Se ha completado una operación de restricción iniciada con una llamada al método **IMAPITable:: Restrict** . 
    
TABLE_ROW_ADDED 
  
> Se ha agregado una fila nueva a la tabla y se ha guardado el objeto correspondiente. Los eventos TABLE_ROW_ADDED se generan después de una llamada al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . 
    
TABLE_ROW_DELETED 
  
> Se ha quitado una fila de la tabla. El miembro **propPrior** se establece en NULL. 
    
TABLE_ROW_MODIFIED 
  
> Se ha cambiado una fila. El miembro **Row** contiene las propiedades afectadas de la fila. Se envían varios eventos TABLE_ROW_MODIFIED en el orden en que aparecen en la vista de tabla. 
    
  Los eventos TABLE_ROW_MODIFIED se envían después de que los cambios realizados en el objeto correspondiente se hayan confirmado con una llamada al método **IMAPIProp:: SaveChanges** . Si la fila modificada es ahora la primera fila de la tabla, el valor de la etiqueta de propiedad en el miembro **propPrior** es **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).
    
TABLE_SETCOL_DONE 
  
> Se ha completado una operación de configuración de columna iniciada con una llamada al método **IMAPITable:: SetColumns** . 
    
TABLE_SORT_DONE 
  
> Se ha completado una operación de ordenación de tabla iniciada con una llamada al método **IMAPITable:: SortTable** . 
    
**Valores**
  
> Valor HRESULT del error que se ha producido, si el miembro **ulTableEvent** está establecido en TABLE_ERROR. 
    
**propIndex**
  
> Estructura [SPropValue](spropvalue.md) de la propiedad **PR_INSTANCE_KEY** de la fila afectada. 
    
**propPrior**
  
> Estructura **SPropValue** de la propiedad **PR_INSTANCE_KEY** de la fila antes de la afectada. Si la fila afectada es la primera fila de la tabla, **propPrior** debe establecerse en **PR_NULL** y no en cero. Cero no es una etiqueta de propiedad válida. 
    
**columna**
  
> Estructura [SRow](srow.md) que describe la fila afectada. Esta estructura se rellena para todos los eventos de notificación de tabla. Para los eventos de notificación de tabla que no pasan datos de fila, el miembro **cValues** de la estructura **SRow** se establece en cero y el miembro **lpProps** se establece en NULL. Porque esta estructura **SRow** es de solo lectura; los clientes deben realizar una copia de la misma si quieren realizar modificaciones. La función [ScDupPropset](scduppropset.md) se puede usar para realizar la copia. 
    
## <a name="remarks"></a>Comentarios

La estructura de **notificación de\_tabla** es uno de los miembros de la Unión de estructuras incluidas en el miembro de **información** de la estructura de [notificación](notification.md) . El miembro **info** incluye una estructura de **notificación de\_tabla** cuando el miembro **UlEventType** de la estructura se establece en _fnevTableModified_.
  
El orden y el tipo de las columnas del miembro de fila reflejan el orden y el tipo que estaban en vigor en el momento en que se generó la notificación. El orden y el tipo en el momento en que se generó la notificación no es necesariamente el mismo que cuando se entregó la notificación. 
  
Para obtener más información acerca de las notificaciones, vea los temas que se describen en la tabla siguiente.
  
|**Tema**|**Descripción**|
|:-----|:-----|
|[Notificación de eventos en MAPI](event-notification-in-mapi.md) <br/> |Información general sobre los eventos de notificación y notificación.  <br/> |
|[Control de notificaciones](handling-notifications.md) <br/> |Descripción de cómo deben administrar los clientes las notificaciones.  <br/> |
|[Admitir notificación de eventos](supporting-event-notification.md) <br/> |Explicación de cómo los proveedores de servicios pueden usar el método **IMAPISupport** para generar notificaciones.  <br/> |
   
Como las notificaciones de tabla son asincrónicas, los clientes pueden recibir una notificación de una fila agregada después de aprender sobre la adición a través de otros medios. Es posible recibir un evento TABLE_ERROR cuando hay un error en un método **IMAPITable:: Sort**, **IMAPITable:: Restrict**o **IMAPITable:: SetColumns** o cuando un proceso subyacente intenta actualizar una tabla con, por ejemplo, New o filas modificadas. 
  
## <a name="see-also"></a>Vea también

- [Notificaci�n](notification.md) 
- [ScDupPropset](scduppropset.md)
- [SRow](srow.md)
- [SPropValue](spropvalue.md)
- [Estructuras MAPI](mapi-structures.md)

