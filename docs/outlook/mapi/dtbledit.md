---
title: DTBLEDIT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLEDIT
api_type:
- COM
ms.assetid: ec3566a0-75ad-466d-a61e-f7d61ccb946d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d0418ac2ec5d01d58c63e4ad48a1066cc386e946
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816734"
---
# <a name="dtbledit"></a>DTBLEDIT

  
  
**Hace referencia a**: Outlook 
  
Describe un control de edición que se usará en un cuadro de diálogo creado a partir de una tabla para mostrar.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Macro relacionado:  <br/> |[SizedDtblEdit](sizeddtbledit.md) <br/> |
   
```cpp
typedef struct _DTBLEDIT
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPropTag;
} DTBLEDIT, FAR *LPDTBLEDIT;

```

## <a name="members"></a>Members

 **ulbLpszCharsAllowed**
  
> Un desplazamiento desde el comienzo de la estructura **DTBLEDIT** a un filtro de cadena de caracteres que se describe las restricciones, si hay alguno, para los caracteres que se pueden escribir en el control de edición. El filtro no se interpreta como una expresión regular y el mismo filtro se aplica a todos los caracteres que ha escrito. El formato del filtro es como sigue: 
    
|**Carácter**|**Descripción**|
|:-----|:-----|
| `*` <br/> |Se permite cualquier carácter (por ejemplo, `"*"`).  <br/> |
| `[ ]` <br/> |Define un conjunto de caracteres (por ejemplo, `"[0123456789]".`)  <br/> |
| `-` <br/> |Indica un intervalo de caracteres (por ejemplo, `"[a-z]"`).  <br/> |
| `~` <br/> |Indica que no se permiten estos caracteres (por ejemplo, `"[~0-9]"`).  <br/> |
| `\` <br/> |Utilizada para entrecomillar cualquiera de los símbolos anteriores (por ejemplo, `"[\-\\\[\]]"` significa-, \, [, y] se permiten caracteres).  <br/> |
   
 **ulFlags**
  
> Máscara de bits de indicadores que se utilizan para designar el formato del filtro de carácter. Se puede establecer la marca siguiente:
    
MAPI_UNICODE.
  
> El filtro está en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., el filtro está en formato ANSI.
    
 **ulNumCharsAllowed**
  
> Número máximo de caracteres que el usuario puede escribir en el cuadro de texto.
    
 **ulPropTag**
  
> Etiqueta de propiedad de una propiedad de tipo PT_TSTRING. El miembro **ulPropTag** identifica la propiedad de cadena cuyos datos se muestran y se modifica en el control de edición. 
    
## <a name="remarks"></a>Comentarios

Una estructura **DTBLEDIT** describe un control de edición en un cuadro de diálogo que contiene información alfanumérico un área. Casi todos los cuadros de diálogo tienen control de edición al menos uno. Controles de edición pueden ser modificable por un usuario o de sólo lectura. 
  
Controles de edición también pueden ser única línea o multiline. Controles de edición de múltiples líneas suelen tener una barra de desplazamiento asociada a ellos. 
  
Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md). Para obtener información acerca de cómo implementar una tabla para mostrar, vea [implementar una tabla mostrar](display-table-implementation.md).
  
## <a name="see-also"></a>Vea también



[DTCTL](dtctl.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[Propiedad canónica PidTagControlType](pidtagcontroltype-canonical-property.md)


[Estructuras MAPI](mapi-structures.md)

