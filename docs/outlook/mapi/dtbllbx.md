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
  
Describe una lista que se utilizará en un cuadro de diálogo que se genera a partir de una tabla de presentación.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
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
  
> Máscara de la lista de marcas usada para eliminar una barra de desplazamiento horizontal o vertical de la lista. Se pueden establecer los siguientes indicadores:
    
MAPI_NO_HBAR 
  
> No debe mostrarse ninguna barra de desplazamiento horizontal con la lista.
    
MAPI_NO_VBAR 
  
> No debe mostrarse ninguna barra de desplazamiento vertical con la lista.
    
 **ulPRSetProperty**
  
> Etiqueta de propiedad de una propiedad de cualquier tipo. Esta propiedad es una de las columnas de la tabla identificada por el miembro **ulPRTableTable** . 
    
 **ulPRTableName**
  
> Etiqueta de propiedad de una propiedad Table de tipo PT Object que se puede abrir mediante una llamada **OpenProperty** . El número de columnas que debe tener la tabla depende de si la lista es una sola o de varias selecciones. Si el miembro **ulPRSetProperty** se establece en **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), la lista permite la selección múltiple.
    
## <a name="remarks"></a>Comentarios

Una estructura **DTBLLBX** describe una lista que es un control que se usa para mostrar varios elementos y permitir al usuario seleccionar uno o más elementos. 
  
El miembro **ulPRSetProperty** y el miembro **ulPRTableName** trabajan juntos; Cuando se elige un valor de la tabla, se vuelve a escribir en **ulPRSetProperty** cuando se descarta el cuadro de diálogo. 
  
El valor de marcas indica si se debe mostrar una barra de desplazamiento horizontal o vertical con la lista. El valor predeterminado es que aparezcan tipos de barras de desplazamiento si es necesario. Los proveedores de servicios pueden establecer MAPI_NO_HBAR para suprimir una barra de desplazamiento horizontal y MAPI_NO_VBAR para suprimir una barra de desplazamiento vertical. 
  
Los dos miembros de la etiqueta de propiedad trabajan juntos para mostrar los valores de la lista y establecer las propiedades correspondientes cuando se selecciona un elemento de la lista. Cuando MAPI muestra la lista por primera vez, llama al método **OpenProperty** de la implementación de **IMAPIProp** para recuperar la tabla identificada en el miembro **ulPRTableName** . El número de columnas de la tabla depende del valor del miembro **ulPRSetProperty** . Si **ulPRSetProperty** se establece en **PR_NULL**, la lista es una lista de selección múltiple basada en un objeto que contiene destinatarios, como un contenedor de libreta de direcciones, una tabla de destinatarios para un mensaje o una tabla de contenido de lista de distribución. 
  
Una tabla de una lista de selección múltiple debe incluir las columnas siguientes:
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **** Es ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
 **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
  
 **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) y un máximo de cinco propiedades de cadena con varios valores, también se pueden mostrar con las tres columnas necesarias. 
  
Si el miembro **ulPRSetProperty** no está establecido en **PR_NULL**, la lista es una lista de selección única. El valor inicial de **ulPRSetProperty** determina la primera fila seleccionada. Cuando un usuario selecciona una de las filas, el miembro **ulPRSetProperty** se establece en el valor seleccionado y este valor se vuelve a escribir en la implementación de la interfaz de propiedades con una llamada a [IMAPIProp:: SetProps](imapiprop-setprops.md). 
  
Para obtener información general sobre las tablas de presentación, consulte [Display tables](display-tables.md). Para obtener información acerca de cómo implementar una tabla de visualización, consulte [Implementing a display Table](display-table-implementation.md).
  
## <a name="see-also"></a>Ver también



[DTCTL](dtctl.md)


[Estructuras MAPI](mapi-structures.md)

