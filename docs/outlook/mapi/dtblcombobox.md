---
title: DTBLCOMBOBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLCOMBOBOX
api_type:
- COM
ms.assetid: 73b68614-6aca-4669-b879-5631c5d6483c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3a5188ea9f83d05722c6b5ab81d9e796b33ef254
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816723"
---
# <a name="dtblcombobox"></a>DTBLCOMBOBOX

  
  
**Hace referencia a**: Outlook 
  
Describe un control de cuadro combinado que se usará en un cuadro de diálogo creado a partir de una tabla para mostrar.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Macro relacionado:  <br/> |[SizedDtblComboBox](sizeddtblcombobox.md) <br/> |
   
```cpp
typedef struct _DTBLCOMBOBOX
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPRPropertyName;
  ULONG ulPRTableName;
} DTBLCOMBOBOX, FAR *LPDTBLCOMBOBOX;

```

## <a name="members"></a>Members

 **ulbLpszCharsAllowed**
  
> Un desplazamiento desde el comienzo de la estructura **DTBLCOMBOBOX** a un filtro de cadena de caracteres que se describe las restricciones, si lo hay, para los caracteres que se pueden escribir en el cuadro combinado control de edición. El filtro no se interpreta como una expresión regular y el mismo filtro se aplica a todos los caracteres que ha escrito. El formato del filtro es como sigue: 
    
|**Carácter**|**Descripción**|
|:-----|:-----|
| `*` <br/> |Se permite cualquier carácter (por ejemplo, `"*"`).  <br/> |
| `[ ]` <br/> |Define un conjunto de caracteres (por ejemplo, `"[0123456789]"`).  <br/> |
| `-` <br/> |Indica un intervalo de caracteres (por ejemplo, `"[a-z]"`).  <br/> |
| `~` <br/> |Indica que no se permiten estos caracteres. (por ejemplo, `"[~0-9]"`).  <br/> |
| `\` <br/> |Utilizada para entrecomillar cualquiera de los símbolos anteriores (por ejemplo, `"[\-\\\[\]]"` significa-, \, [, y] se permiten caracteres).  <br/> |
   
 **ulFlags**
  
> Máscara de bits de indicadores que se utilizan para designar el formato del filtro de cadena de caracteres. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> El filtro está en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., el filtro está en formato ANSI.
    
 **ulNumCharsAllowed**
  
> Número máximo de caracteres que se puede escribir en el cuadro de texto del cuadro combinado.
    
 **ulPRPropertyName**
  
> Etiqueta de propiedad de una propiedad de tipo PT_TSTRING. 
    
 **ulPRTableName**
  
> Etiqueta de propiedad de una propiedad de PT Object de tipo en el que se puede abrir una interfaz **IMAPITable** mediante una llamada **OpenProperty** . La tabla debe tener una columna con una propiedad que es el mismo tipo que la propiedad identificada por el miembro **ulPRPropertyName** . Las filas de la tabla se usan para rellenar la lista. 
    
## <a name="remarks"></a>Comentarios

Una estructura **DTBLCOMBOBOX** describe un cuadro combinado un control que consta de una lista y un campo de la selección. La lista presenta la información desde la que puede seleccionar un usuario y el campo de selección muestra la selección actual. El campo de selección es un control de edición que también puede usarse para escribir texto no está ya en la lista. 
  
Los miembros de la etiqueta de dos propiedad funcionan conjuntamente para coordinar la visualización de la lista con el control de edición. Cuando MAPI en primer lugar muestra el cuadro combinado, llama al método **OpenProperty** de la implementación de **IMAPIProp** que está asociado a la tabla para mostrar que se va a recuperar la tabla representada por el miembro **ulPRTableName** . Esta tabla tiene una columna de una columna que contiene los valores de la propiedad representada por el miembro **ulPRPropertyName** . Por lo tanto, esta columna debe ser del mismo tipo que la propiedad **ulPRPropertyName** y ambas columnas deben ser cadenas de caracteres. 
  
Los valores para la columna se muestran en la sección de la lista del cuadro combinado. Por lo tanto, **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) no es una etiqueta de propiedad válido para **ulPRPropertyName**. Cuando un usuario selecciona una de las filas o escribe nuevos datos en el cuadro de texto, la propiedad **ulPRPropertyName** se establece en el valor introducido o seleccionado. 
  
Para mostrar un valor inicial para el control de edición, MAPI llama a [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar los valores de propiedad para la tabla para mostrar. Si una de las propiedades devueltas coincide con la propiedad representada por el miembro **ulPRPropertyName** , su valor se convierte en el valor inicial. 
  
Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md). Para obtener información acerca de cómo implementar una tabla para mostrar, vea [implementar una tabla mostrar](display-table-implementation.md).
  
## <a name="see-also"></a>Vea también



[DTCTL](dtctl.md)
  
[Propiedad canónica PidTagControlType](pidtagcontroltype-canonical-property.md)


[Estructuras MAPI](mapi-structures.md)

