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
ms.openlocfilehash: bd0caff8a6c7834bdd01ef4be64805bde66dd6d9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578825"
---
# <a name="dtblpage"></a>DTBLPAGE

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Describe una página con fichas que se usará en un cuadro de diálogo que se genera a partir de una tabla para mostrar. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Macro relacionado:  <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
   
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
  
> Posición en la memoria de la etiqueta de cadena de caracteres de la ficha página.
    
 **ulFlags**
  
> Máscara de bits de indicadores que se utilizan para designar el formato de la etiqueta que señala el miembro **ulbLpszLabelName** . Se puede establecer la marca siguiente: 
    
MAPI_UNICODE. 
  
> La etiqueta está en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., la etiqueta está en formato ANSI.
    
 **ulbLpszComponent**
  
> Posición en la memoria de una cadena de caracteres que identifica la sección **[Help File Mappings]** en el archivo MAPISVC. Archivo de configuración de INF o 0. El nombre de archivo que aparece en el archivo MAPISVC. Sección INF puede utilizarse por un usuario para tener acceso a información de ayuda sobre la página con fichas haciendo clic en el botón **Ayuda** en el cuadro de diálogo. Para obtener más información acerca de las entradas en MAPISVC. INF, vea [formato de archivo de MAPISVC. INF](file-format-of-mapisvc-inf.md).
    
 **ulContext**
  
> Un identificador único para la página con fichas en la cadena definida por el miembro **ulbLpszComponent** . El miembro **ulbLpszComponent** y el miembro **ulContext** deben ser distinto de cero para el botón de **Ayuda** para que funcione. Si este identificador es cero y la cadena de componente es NULL, no hay ninguna ayuda asociado a la página. 
    
## <a name="remarks"></a>Comentarios

Una estructura **DTBLPAGE** describe una página con fichas de un control que se usa para separar varios cuadros de diálogo relacionados. Normalmente, estos cuadros de diálogo son hojas de propiedades para mostrar la configuración, mensaje u opciones de destinatarios. Al hacer clic en la ficha, el usuario puede cambiar de una hoja a otra. 
  
El identificador de cadena y el contexto de componente proporcionan información sobre si la Ayuda extendida está disponible para la página con fichas. Si la Ayuda extendida está disponible, el identificador de cadena y el contexto de componente proporcionará información acerca de cómo tener acceso a él. La cadena del componente que se asigna al archivo de ayuda; el identificador de contexto que se asigna al tema de Ayuda inicial. Si el identificador de contexto es cero y la cadena de componente es NULL, la información de ayuda no está disponible.
  
Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md). Para obtener información acerca de cómo implementar una tabla para mostrar, vea [implementar una tabla mostrar](display-table-implementation.md).
  
## <a name="see-also"></a>Vea también



[DTCTL](dtctl.md)


[Estructuras MAPI](mapi-structures.md)

