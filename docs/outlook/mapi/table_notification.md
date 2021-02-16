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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415960"
---
# <a name="table_notification"></a>TABLE_NOTIFICATION

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una fila de una tabla que se ha visto afectada por algún tipo de evento, como un cambio o un error. Esto hace que se genere una notificación de tabla. 
  
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
  
> Máscara de bits de marcas usadas para representar el tipo de evento de tabla. Se pueden establecer las siguientes marcas:
    
TABLE_CHANGED 
  
> Indica en un nivel alto que algo de la tabla ha cambiado. El estado de la tabla es el mismo que antes del evento. Esto significa que todas **las PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), los marcadores, el posicionamiento actual y las selecciones de la interfaz de usuario siguen siendo válidos. Para controlar este evento, vuelva a leer la tabla. Los proveedores de servicios que no desean implementar notificaciones de tabla enriquecida envían TABLE_CHANGED eventos en lugar de eventos más detallados para indicar un tipo concreto de cambio. 
    
TABLE_ERROR 
  
> Se ha producido un error, normalmente durante el procesamiento de una operación asincrónica. Los errores durante el procesamiento de los métodos siguientes pueden generar este evento: 
    
   - [IMAPITable::SortTable](imapitable-sorttable.md)
    
   - [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
   - [IMAPITable::Restrict](imapitable-restrict.md)
    
   Después de recibir un TABLE_ERROR evento, un cliente no puede confiar en la precisión del contenido de la tabla. Además, es posible que se pierdan las notificaciones pendientes sobre otros cambios. Es posible que el método [IMAPITable::GetLastError](imapitable-getlasterror.md) no proporcione información adicional sobre el error porque se generó en algún punto anterior, no necesariamente a partir de la última llamada al método. 
    
TABLE_RELOAD 
  
> Los datos de la tabla deben volver a cargarse. Los proveedores de servicios TABLE_RELOAD cuando, por ejemplo, los datos subyacentes se almacenan en una base de datos y se reemplaza la base de datos. Controle este evento suponiendo que nada sobre la tabla sigue siendo válido y releciendo la tabla. Todos los marcadores, las claves de instancia, el estado y la información de posicionamiento no son válidos.
    
TABLE_RESTRICT_DONE 
  
> Se ha completado una operación de restricción iniciada con una llamada al método **IMAPITable::Restrict.** 
    
TABLE_ROW_ADDED 
  
> Se ha agregado una nueva fila a la tabla y se ha guardado el objeto correspondiente. TABLE_ROW_ADDED eventos se generan después de una llamada al método [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) 
    
TABLE_ROW_DELETED 
  
> Se ha quitado una fila de la tabla. El **miembro propPrior** se establece en NULL. 
    
TABLE_ROW_MODIFIED 
  
> Se ha cambiado una fila. El **miembro** de fila contiene las propiedades afectadas de la fila. Varios TABLE_ROW_MODIFIED eventos se envían en el orden en que aparecen en la vista de tabla. 
    
  TABLE_ROW_MODIFIED eventos se envían después de que se hayan confirmado los cambios realizados en el objeto correspondiente con una llamada al método **IMAPIProp::SaveChanges.** Si la fila modificada es ahora la primera fila de la tabla, el valor de la etiqueta de propiedad en el miembro **propPrior** **es PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).
    
TABLE_SETCOL_DONE 
  
> Se ha completado una operación de configuración de columna iniciada con una llamada al método **IMAPITable::SetColumns.** 
    
TABLE_SORT_DONE 
  
> Se ha completado una operación de ordenación de tabla iniciada con una llamada al método **IMAPITable::SortTable.** 
    
**hResult**
  
> Valor HRESULT del error que se ha producido, si el **miembro ulTableEvent** está establecido en TABLE_ERROR. 
    
**propIndex**
  
> [Estructura SPropValue](spropvalue.md) para la **PR_INSTANCE_KEY** propiedad de la fila afectada. 
    
**propPrior**
  
> **Estructura SPropValue** para la **PR_INSTANCE_KEY** propiedad de la fila antes de la afectada. Si la fila afectada es la primera fila de la tabla, **propPrior** debe establecerse en **PR_NULL** y no en cero. Cero no es una etiqueta de propiedad válida. 
    
**row**
  
> [Estructura SRow](srow.md) que describe la fila afectada. Esta estructura se rellena para todos los eventos de notificación de tabla. Para eventos de notificación de tabla que no pasan datos de fila, el miembro **cValues** de la estructura **SRow** se establece en cero y el miembro **lpProps** se establece en NULL. Dado que **esta estructura de SRow** es de solo lectura; los clientes deben hacer una copia de él si desean realizar modificaciones. La [función ScDupPropset](scduppropset.md) se puede usar para realizar la copia. 
    
## <a name="remarks"></a>Comentarios

La **estructura \_ TABLE NOTIFICATION** es uno de los miembros de la unión de estructuras incluidas en el miembro de **información** de la [estructura NOTIFICATION.](notification.md) El **miembro** de información incluye una **estructura TABLE \_ NOTIFICATION** cuando el **miembro ulEventType** de la estructura se establece en  _fnevTableModified_.
  
El orden y el tipo de columnas en el miembro de fila reflejan el orden y el tipo que estaba en vigor en el momento en que se generó la notificación. El pedido y el tipo en el momento en que se generó la notificación no es necesariamente el mismo que cuando se entregó la notificación. 
  
Para obtener más información acerca de la notificación, consulte los temas descritos en la tabla siguiente.
  
|**Tema**|**Descripción**|
|:-----|:-----|
|[Notificación de eventos en MAPI](event-notification-in-mapi.md) <br/> |Información general sobre los eventos de notificación y notificación.  <br/> |
|[Control de notificaciones](handling-notifications.md) <br/> |Discusión sobre cómo los clientes deben controlar las notificaciones.  <br/> |
|[Notificación de eventos de soporte técnico](supporting-event-notification.md) <br/> |Discusión sobre cómo los proveedores de servicios pueden usar **el método IMAPISupport** para generar notificaciones.  <br/> |
   
Dado que las notificaciones de tabla son asincrónicas, los clientes pueden recibir notificaciones de una fila agregada después de conocer la adición a través de otros medios. Es posible recibir un evento TABLE_ERROR cuando hay un error en un método **IMAPITable::Sort**, **IMAPITable::Restrict** o **IMAPITable::SetColumns** o cuando un proceso subyacente intenta actualizar una tabla con, por ejemplo, filas nuevas o modificadas. 
  
## <a name="see-also"></a>Consulte también

- [Notificaci�n](notification.md) 
- [ScDupPropset](scduppropset.md)
- [SRow](srow.md)
- [SPropValue](spropvalue.md)
- [Estructuras MAPI](mapi-structures.md)

