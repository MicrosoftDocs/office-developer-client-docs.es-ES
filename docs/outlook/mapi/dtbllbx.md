---
title: DTBLLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLLBX
api_type:
- COM
ms.assetid: 971b4837-6823-4f28-9803-3c22b2ec091f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 04fbfb2e6938c1ae5971e90b30f5ef749e7963e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816735"
---
# <a name="dtbllbx"></a>DTBLLBX

  
  
**Hace referencia a**: Outlook 
  
Describe una lista que se usará en un cuadro de diálogo que se genera a partir de una tabla para mostrar.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLLBX
{
  ULONG ulFlags;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLLBX, FAR *LPDTBLLBX

```

## <a name="members"></a>Members

 **ulFlags**
  
> Máscara de bits de marcas que se usan para eliminar una barra de desplazamiento horizontal o vertical de la lista. Se pueden establecer los siguientes indicadores:
    
MAPI_NO_HBAR 
  
> No debe ser se muestra ninguna barra de desplazamiento horizontal con la lista.
    
MAPI_NO_VBAR 
  
> No debe ser se muestra ninguna barra de desplazamiento vertical con la lista.
    
 **ulPRSetProperty**
  
> Etiqueta de propiedad de una propiedad de cualquier tipo. Esta propiedad es una de las columnas en la tabla identificada por el miembro **ulPRTableTable** . 
    
 **ulPRTableName**
  
> Etiqueta de la propiedad para una propiedad de tabla de tipo pt Object que se pueden abrir mediante el uso de un **OpenProperty** llamar. El número de columnas que debería tener la tabla depende de si la lista es una lista de selección múltiple o simple. Si se establece el miembro **ulPRSetProperty** en **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), la lista permite la selección múltiple.
    
## <a name="remarks"></a>Comentarios

Una estructura **DTBLLBX** describe un un control que se usa para mostrar varios elementos y permitir que un usuario seleccione uno o varios de los elementos de lista. 
  
El miembro **ulPRSetProperty** y **ulPRTableName** miembro funcionan conjuntamente; Cuando se elige un valor de la tabla, está escrito volver a **ulPRSetProperty** cuando se cierra el cuadro de diálogo. 
  
El valor de flags indica si se debe mostrar una barra de desplazamiento horizontal o vertical con la lista. El valor predeterminado es a tener tipos de muestran barras de desplazamiento si es necesario. Proveedores de servicios pueden establecer MAPI_NO_HBAR para suprimir una barra de desplazamiento horizontal y MAPI_NO_VBAR para suprimir una barra de desplazamiento vertical. 
  
Los miembros de la etiqueta de dos propiedad funcionan conjuntamente para mostrar los valores en la lista y establecer las propiedades correspondientes cuando se selecciona un elemento en la lista. Cuando MAPI en primer lugar muestra la lista, se llama el **IMAPIProp** **OpenProperty** método de la implementación para recuperar la tabla identificada en el miembro **ulPRTableName** . El número de columnas de la tabla depende del valor del miembro **ulPRSetProperty** . Si **ulPRSetProperty** se establece en **PR_NULL**, la lista es una lista de selección de varios basándose en un objeto que contiene a los destinatarios, como un contenedor de la libreta de direcciones, una tabla de destinatarios para un mensaje o una tabla de contenido de lista de distribución. 
  
Una tabla para una lista de selección múltiple debe incluir las siguientes columnas:
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
 **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
  
 **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) y también se puede mostrar un máximo de cinco otras propiedades de cadena multivalor con las tres columnas necesarias. 
  
Si el miembro **ulPRSetProperty** no está establecido en **PR_NULL**, la lista es una lista de selección única. El valor inicial de **ulPRSetProperty** determina la primera fila seleccionada. Cuando un usuario selecciona una de las filas, el miembro **ulPRSetProperty** se establece en el valor seleccionado y este valor se vuelve a escribir la implementación de la interfaz de propiedad con una llamada a [IMAPIProp::SetProps](imapiprop-setprops.md). 
  
Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md). Para obtener información acerca de cómo implementar una tabla para mostrar, vea [implementar una tabla mostrar](display-table-implementation.md).
  
## <a name="see-also"></a>Vea también



[DTCTL](dtctl.md)


[Estructuras MAPI](mapi-structures.md)

