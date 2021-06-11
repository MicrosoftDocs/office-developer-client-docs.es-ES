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
ms.openlocfilehash: b07ea265b5dcc6b9a9abb15c6be7ac9e0f94e8ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404683"
---
# <a name="dtbledit"></a>DTBLEDIT

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe un control de edición que se usará en un cuadro de diálogo creado a partir de una tabla para mostrar.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Macro relacionada:  <br/> |[SizedDtblEdit](sizeddtbledit.md) <br/> |
   
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
  
> Desplazamiento desde el inicio de la estructura **DTBLEDIT** a un filtro de cadena de caracteres que describe restricciones, si las hubiera, a los caracteres que se pueden especificar en el control de edición. El filtro no se interpreta como una expresión regular y el mismo filtro se aplica a todos los caracteres especificados. El formato del filtro es el siguiente: 
    
|**Carácter**|**Descripción**|
|:-----|:-----|
| `*` <br/> |Se permite cualquier carácter (por ejemplo,  `"*"` ).  <br/> |
| `[ ]` <br/> |Define un conjunto de caracteres (por ejemplo,  `"[0123456789]".` )  <br/> |
| `-` <br/> |Indica un intervalo de caracteres (por ejemplo,  `"[a-z]"` ).  <br/> |
| `~` <br/> |Indica que estos caracteres no están permitidos (por ejemplo,  `"[~0-9]"` ).  <br/> |
| `\` <br/> |Se usa para citar cualquiera de los símbolos anteriores (por ejemplo, se permiten los caracteres  `"[\-\\\[\]]"` -, \, [y ] ).  <br/> |
   
 **ulFlags**
  
> Máscara de bits de marcas usadas para designar el formato del filtro de caracteres. Se puede establecer la siguiente marca:
    
MAPI_UNICODE
  
> El filtro está en formato Unicode. Si la MAPI_UNICODE no está establecida, el filtro está en formato ANSI.
    
 **ulNumCharsAllowed**
  
> Número máximo de caracteres que el usuario puede escribir en el cuadro de texto.
    
 **ulPropTag**
  
> Etiqueta de propiedad para una propiedad de tipo PT_TSTRING. El **miembro ulPropTag** identifica la propiedad string cuyos datos se muestran y editan en el control de edición. 
    
## <a name="remarks"></a>Comentarios

Una **estructura DTBLEDIT** describe un control de edición un área de un cuadro de diálogo que contiene información alfanumérica. Casi todos los cuadros de diálogo tienen al menos un control de edición. Los controles de edición pueden ser modificables por un usuario o de solo lectura. 
  
Los controles de edición también pueden ser de línea única o multilínea. Los controles de edición multilínea suelen tener asociada una barra de desplazamiento. 
  
Para obtener información general sobre las tablas para mostrar, vea [Tablas para mostrar.](display-tables.md) Para obtener información sobre cómo implementar una tabla para mostrar, vea [Implementing a Display Table](display-table-implementation.md).
  
## <a name="see-also"></a>Vea también



[DTCTL](dtctl.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[Propiedad canónica PidTagControlType](pidtagcontroltype-canonical-property.md)


[Estructuras MAPI](mapi-structures.md)

