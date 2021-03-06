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
ms.openlocfilehash: 2bff20af2b3e9ea4e203e38ae38a8bc19074a727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438571"
---
# <a name="dtbllbx"></a>DTBLLBX

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una lista que se usará en un cuadro de diálogo creado a partir de una tabla para mostrar.
  
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

## <a name="members"></a>Miembros

 **ulFlags**
  
> Máscara de bits de las marcas usadas para eliminar una barra de desplazamiento horizontal o vertical de la lista. Se pueden establecer las siguientes marcas:
    
MAPI_NO_HBAR 
  
> No se debe mostrar ninguna barra de desplazamiento horizontal con la lista.
    
MAPI_NO_VBAR 
  
> No se debe mostrar ninguna barra de desplazamiento vertical con la lista.
    
 **ulPRSetProperty**
  
> Etiqueta de propiedad para una propiedad de cualquier tipo. Esta propiedad es una de las columnas de la tabla identificadas por el **miembro ulPRTableTable.** 
    
 **ulPRTableName**
  
> Etiqueta de propiedad para una propiedad table de tipo PT_OBJECT que se puede abrir mediante una **llamada OpenProperty.** El número de columnas que debe tener la tabla depende de si la lista es una lista de selección única o múltiple. Si el **miembro ulPRSetProperty** está establecido en **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), la lista permite varias selecciones.
    
## <a name="remarks"></a>Comentarios

Una **estructura DTBLLBX** describe una lista de un control que se usa para mostrar varios elementos y permitir que un usuario seleccione uno o varios de los elementos. 
  
El **miembro ulPRSetProperty** y **el miembro ulPRTableName** funcionan juntos; cuando se elige un valor de la tabla, se vuelve a escribir en **ulPRSetProperty** cuando se descarta el cuadro de diálogo. 
  
El valor de las marcas indica si se debe mostrar una barra de desplazamiento horizontal o vertical con la lista. El valor predeterminado es que aparezcan tipos de barras de desplazamiento si es necesario. Los proveedores de servicios pueden MAPI_NO_HBAR para suprimir una barra de desplazamiento horizontal MAPI_NO_VBAR suprimir una barra de desplazamiento vertical. 
  
Los dos miembros de la etiqueta de propiedad trabajan juntos para mostrar valores en la lista y establecer las propiedades correspondientes cuando se selecciona un elemento de la lista. Cuando MAPI muestra la lista por primera vez, llama al método **OpenProperty** de la implementación **IMAPIProp** para recuperar la tabla identificada en el **miembro ulPRTableName.** El número de columnas de la tabla depende del valor del **miembro ulPRSetProperty.** Si **ulPRSetProperty** se establece en **PR_NULL**, la lista es una lista de selección múltiple basada en un objeto que contiene destinatarios, como un contenedor de libreta de direcciones, una tabla de destinatarios para un mensaje o una tabla de contenido de lista de distribución. 
  
Una tabla para una lista de selección múltiple debe incluir las siguientes columnas:
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
 **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
  
 **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) y un máximo de otras cinco propiedades de cadena multivalor también se pueden mostrar con las tres columnas necesarias. 
  
Si el **miembro ulPRSetProperty** no está establecido en **PR_NULL**, la lista es una lista de selección única. El valor inicial de **ulPRSetProperty** determina la primera fila seleccionada. Cuando un usuario selecciona una de las filas, el miembro **ulPRSetProperty** se establece en el valor seleccionado y este valor se escribe de nuevo en la implementación de la interfaz de propiedades con una llamada a [IMAPIProp::SetProps](imapiprop-setprops.md). 
  
Para obtener información general sobre las tablas para mostrar, vea [Tablas para mostrar.](display-tables.md) Para obtener información sobre cómo implementar una tabla para mostrar, vea [Implementing a Display Table](display-table-implementation.md).
  
## <a name="see-also"></a>Vea también



[DTCTL](dtctl.md)


[Estructuras MAPI](mapi-structures.md)

