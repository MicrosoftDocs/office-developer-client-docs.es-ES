---
title: DTBLPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLPAGE
api_type:
- COM
ms.assetid: f899f434-a5d7-4b4f-98f9-c14c9f21b24b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6f3d98a3133d79f78f4eb676d49ec85ef5a359f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424003"
---
# <a name="dtblpage"></a>DTBLPAGE

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una página con fichas que se utilizará en un cuadro de diálogo que se genera a partir de una tabla de presentación. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Macro relacionada:  <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
   
```cpp
typedef struct _DTBLPAGE
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulbLpszComponent;
  ULONG ulContext;
} DTBLPAGE, FAR *LPDTBLPAGE;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Posición en la memoria de la etiqueta de la cadena de caracteres para la ficha de página.
    
 **ulFlags**
  
> Máscara de la máscara usada para designar el formato de la etiqueta a la que señala el miembro **ulbLpszLabelName** . Se puede establecer la siguiente marca: 
    
MAPI_UNICODE 
  
> La etiqueta está en formato Unicode. Si no se establece la marca MAPI_UNICODE, la etiqueta está en formato ANSI.
    
 **ulbLpszComponent**
  
> Posición en la memoria de una cadena de caracteres que identifica la sección **[asignaciones de archivos de ayuda] del archivo** MAPISVC. Archivo de configuración INF o 0. Nombre de archivo que aparece en el archivo MAPISVC. INF puede ser usada por un usuario para tener acceso a la ayuda ampliada de la página con fichas haciendo clic en el botón **ayuda** en el cuadro de diálogo. Para obtener más información acerca de las entradas de MAPISVC. INF, vea el [formato de archivo de MAPISVC. INF](file-format-of-mapisvc-inf.md).
    
 **ulContext**
  
> Un identificador único para la página con fichas en la cadena definida por el miembro **ulbLpszComponent** . El miembro **ulbLpszComponent** y el miembro **ulContext** deben ser distintos de cero para que funcione el botón **ayuda** . Si este identificador es cero y la cadena del componente es NULL, no hay ayuda asociada a la página. 
    
## <a name="remarks"></a>Comentarios

Una estructura **DTBLPAGE** describe una página con fichas un control que se usa para separar varios cuadros de diálogo relacionados. Normalmente, estos cuadros de diálogo son hojas de propiedades para mostrar opciones de configuración, mensajes o destinatarios. Al hacer clic en la pestaña, el usuario puede cambiar de una hoja a otra. 
  
El identificador de contexto y la cadena de componentes proporcionan información sobre si la ayuda ampliada está disponible para la página con fichas. Si hay disponible ayuda ampliada, el identificador de contexto y la cadena de componentes proporcionarán información sobre cómo obtener acceso a ella. La cadena de componente se asigna al archivo de ayuda; el identificador de contexto se asigna al tema de ayuda inicial. Si el identificador de contexto es cero y la cadena del componente es NULL, la ayuda extendida no está disponible.
  
Para obtener información general sobre las tablas de presentación, consulte [Display tables](display-tables.md). Para obtener información acerca de cómo implementar una tabla de visualización, consulte [Implementing a display Table](display-table-implementation.md).
  
## <a name="see-also"></a>Ver también



[DTCTL](dtctl.md)


[Estructuras MAPI](mapi-structures.md)

