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
ms.openlocfilehash: 5256efbff734d4555ac263dd330e3349c789cd74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406979"
---
# <a name="dtblcombobox"></a>DTBLCOMBOBOX

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe un control de cuadro combinado que se usará en un cuadro de diálogo creado a partir de una tabla para mostrar.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Macro relacionada:  <br/> |[SizedDtblComboBox](sizeddtblcombobox.md) <br/> |
   
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

## <a name="members"></a>Miembros

 **ulbLpszCharsAllowed**
  
> Desplazamiento desde el inicio de la estructura **DTBLCOMBOBOX** a un filtro de cadena de caracteres que describe las restricciones, si las hay, a los caracteres que se pueden especificar en el control de edición del cuadro combinado. El filtro no se interpreta como una expresión regular y se aplica el mismo filtro a todos los caracteres especificados. El formato del filtro es el siguiente: 
    
|**Carácter**|**Descripción**|
|:-----|:-----|
| `*` <br/> |Se permite cualquier carácter (por ejemplo,  `"*"` ).  <br/> |
| `[ ]` <br/> |Define un conjunto de caracteres (por ejemplo,  `"[0123456789]"` ).  <br/> |
| `-` <br/> |Indica un intervalo de caracteres (por ejemplo,  `"[a-z]"` ).  <br/> |
| `~` <br/> |Indica que estos caracteres no están permitidos. (por ejemplo,  `"[~0-9]"` ).  <br/> |
| `\` <br/> |Se usa para citar cualquiera de los símbolos anteriores (por ejemplo, se permiten los caracteres  `"[\-\\\[\]]"` -, \, [y ]).  <br/> |
   
 **ulFlags**
  
> Máscara de bits de marcas usadas para designar el formato del filtro de cadena de caracteres. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> El filtro está en formato Unicode. Si no MAPI_UNICODE marca, el filtro está en formato ANSI.
    
 **ulNumCharsAllowed**
  
> Número máximo de caracteres que se pueden especificar en el cuadro de texto del cuadro combinado.
    
 **ulPRPropertyName**
  
> Etiqueta de propiedad para una propiedad de tipo PT_TSTRING. 
    
 **ulPRTableName**
  
> Etiqueta de propiedad de una propiedad de tipo PT_OBJECT en la que se puede abrir una interfaz **IMAPITable** mediante una **llamada a OpenProperty.** La tabla debe tener una columna con una propiedad que sea del mismo tipo que la propiedad identificada por el **miembro ulPRPropertyName.** Las filas de la tabla se usan para rellenar la lista. 
    
## <a name="remarks"></a>Comentarios

Una **estructura DTBLCOMBOBOX** describe un cuadro combinado que consta de una lista y un campo de selección. La lista presenta la información a partir de la cual un usuario puede seleccionar y el campo de selección muestra la selección actual. El campo de selección es un control de edición que también se puede usar para escribir texto que aún no está en la lista. 
  
Los dos miembros de la etiqueta de propiedad trabajan juntos para coordinar la presentación de la lista con el control de edición. Cuando MAPI muestra el cuadro combinado por primera vez, llama al método **OpenProperty** de la implementación **IMAPIProp** asociada a la tabla para mostrar para recuperar la tabla representada por el **miembro ulPRTableName.** Esta tabla tiene una columna que contiene valores para la propiedad representada por el **miembro ulPRPropertyName.** Por lo tanto, esta columna debe ser del mismo tipo que la propiedad **ulPRPropertyName** y ambas columnas deben ser cadenas de caracteres. 
  
Los valores de la columna se muestran en la sección de lista del cuadro combinado. Por lo **tanto, PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) no es una etiqueta de propiedad válida para **ulPRPropertyName**. Cuando un usuario selecciona una de las filas o escribe nuevos datos en el cuadro de texto, la propiedad **ulPRPropertyName** se establece en el valor seleccionado o especificado. 
  
Para mostrar un valor inicial para el control de edición, MAPI llama a [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar los valores de propiedad de la tabla para mostrar. Si una de las propiedades recuperadas coincide con la propiedad representada por el **miembro ulPRPropertyName,** su valor se convierte en el valor inicial. 
  
Para obtener información general sobre las tablas para mostrar, vea [Tablas para mostrar.](display-tables.md) Para obtener información acerca de cómo implementar una tabla para mostrar, vea [Implementar una tabla para mostrar.](display-table-implementation.md)
  
## <a name="see-also"></a>Consulte también



[DTCTL](dtctl.md)
  
[Propiedad canónica PidTagControlType](pidtagcontroltype-canonical-property.md)


[Estructuras MAPI](mapi-structures.md)

