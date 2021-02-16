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
  
Describe una página con fichas que se usará en un cuadro de diálogo creado a partir de una tabla para mostrar. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
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

## <a name="members"></a>Miembros

 **ulbLpszLabel**
  
> Posición en la memoria de la etiqueta de cadena de caracteres de la ficha de página.
    
 **ulFlags**
  
> Máscara de bits de marcas usada para designar el formato de la etiqueta a la que apunta el **miembro ulbLpszLabelName.** Se puede establecer la siguiente marca: 
    
MAPI_UNICODE 
  
> La etiqueta está en formato Unicode. Si no MAPI_UNICODE marca, la etiqueta está en formato ANSI.
    
 **ulbLpszComponent**
  
> Posición en la memoria de una cadena de caracteres que identifica la **sección [Asignaciones** de archivo de ayuda] en MAPISVC. Archivo de configuración INF o 0. Nombre de archivo que aparece en MAPISVC. Un usuario puede usar la sección INF para obtener acceso a la Ayuda ampliada de la página con pestañas haciendo clic en el botón **Ayuda** del cuadro de diálogo. Para obtener más información acerca de las entradas de MAPISVC. INF, consulte [Formato de archivo de MAPISVC. INF](file-format-of-mapisvc-inf.md).
    
 **ulContext**
  
> Identificador único de la página con fichas en la cadena definida por el **miembro ulbLpszComponent.** Tanto **el miembro ulbLpszComponent** como el miembro **ulContext** deben ser distintos de cero para que **funcione** el botón Ayuda. Si este identificador es cero y la cadena de componente es NULL, no hay ninguna Ayuda asociada con la página. 
    
## <a name="remarks"></a>Comentarios

Una **estructura DTBLPAGE** describe una página con fichas, un control que se usa para separar varios cuadros de diálogo relacionados. Normalmente, estos cuadros de diálogo son hojas de propiedades para mostrar opciones de configuración, mensaje o destinatario. Al hacer clic en la pestaña, el usuario puede cambiar de una hoja a otra. 
  
La cadena de componente y el identificador de contexto proporcionan información sobre si la Ayuda extendida está disponible para la página con fichas. Si la Ayuda ampliada está disponible, la cadena de componente y el identificador de contexto proporcionarán información sobre cómo obtener acceso a ella. La cadena de componente se asigna al archivo de Ayuda; el identificador de contexto se asigna al tema de Ayuda inicial. Si el identificador de contexto es cero y la cadena de componente es NULL, la Ayuda extendida no está disponible.
  
Para obtener información general sobre las tablas para mostrar, vea [Tablas para mostrar.](display-tables.md) Para obtener información acerca de cómo implementar una tabla para mostrar, vea [Implementar una tabla para mostrar.](display-table-implementation.md)
  
## <a name="see-also"></a>Consulte también



[DTCTL](dtctl.md)


[Estructuras MAPI](mapi-structures.md)

