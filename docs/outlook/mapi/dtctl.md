---
title: DTCTL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTCTL
api_type:
- COM
ms.assetid: 6d1589e9-b171-427a-9a3e-b4154ee8ceb6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2a2ca1fba5dceb45b41c2f25a96e163f02c41440
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421504"
---
# <a name="dtctl"></a>DTCTL

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe un control que se usará en un cuadro de diálogo creado a partir de una tabla para mostrar. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct
{
  ULONG ulCtlType;
  ULONG ulCtlFlags;
  LPBYTE lpbNotif;
  ULONG cbNotif;
  LPSTR lpszFilter;
  ULONG ulItemID;
  union
  {
    LPVOID lpv;
    LPDTBLLABEL lplabel;
    LPDTBLEDIT lpedit;
    LPDTBLLBX lplbx;
    LPDTBLCOMBOBOX lpcombobox;
    LPDTBLDDLBX lpddlbx;
    LPDTBLCHECKBOX lpcheckbox;
    LPDTBLGROUPBOX lpgroupbox;
    LPDTBLBUTTON lpbutton;
    LPDTBLRADIOBUTTON lpradiobutton;
    LPDTBLMVLISTBOX lpmvlbx;
    LPDTBLMVDDLBX lpmvddlbx;
    LPDTBLPAGE lppage;
  } ctl;
} DTCTL, FAR *LPDTCTL;

```

## <a name="members"></a>Members

**ulCtlType**
  
> Tipo de control que se incluye en el miembro **ctl** y corresponde a la propiedad PR_CONTROL_TYPE **(** [PidTagControlType](pidtagcontroltype-canonical-property.md)). Los valores posibles son los siguientes:
    
DTCT_LABEL 
  
> Control Etiqueta
    
DTCT_EDIT 
  
> Control de edición.
    
DTCT_LBX 
  
> Control cuadro de lista.
    
DTCT_COMBOBOX 
  
> Control de cuadro combinado.
    
DTCT_DDLBX 
  
> Control de lista desplegable.
    
DTCT_CHECKBOX 
  
> Control de casilla.
    
DTCT_GROUPBOX 
  
> Control de cuadro de grupo.
    
DTCT_BUTTON 
  
> Control de botón.
    
DTCT_PAGE 
  
> Control de página con pestañas.
    
DTCT_RADIOBUTTON 
  
> Control de botón de radio.
    
DTCT_MVLISTBOX 
  
> Control de lista de varios valores.
    
DTCT_MVDDLBX 
  
> Control de lista desplegable de varios valores.
    
**ulCtlFlags**
  
> Máscara de bits de marcas que describe las características del control y corresponde a la propiedad PR_CONTROL_FLAGS **(** [PidTagControlFlags](pidtagcontrolflags-canonical-property.md)). Estas marcas solo se pueden establecer para casillas, cuadros combinados, cuadros de lista y controles de edición. Los valores posibles son los siguientes:
    
DT_ACCEPT_DBCS 
  
> Se acepta el formato ANSI o DBCS. Esta marca solo es válida para los controles de edición.
    
DT_EDITABLE 
  
> Un usuario puede modificar el texto del control. 
    
DT_MULTILINE 
  
> El control puede contener varias líneas de texto. Esta marca solo es válida para los controles de edición.
    
DT_PASSWORD_EDIT 
  
> El control contiene una contraseña; por lo tanto, el contenido del control no debe mostrarse al usuario. Esta marca solo es válida para los controles de edición.
    
DT_REQUIRED 
  
> Se requiere el control de cuadro de diálogo. Esta marca solo es válida para controles de edición y cuadro combinado.
    
DT_SET_IMMEDIATE 
  
> Habilita el resultado inmediato de un valor tras un cambio en el control. Esto permite establecer una relación de dependencia entre dos controles. 
    
**lpbNotif**
  
> Puntero a una estructura que consta de una [estructura GUID,](guid.md) para representar el proveedor de servicios y un identificador para el control. Los **miembros lpbNotif** y **cbNotif** corresponden a la propiedad **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) del control y se usan para notificar a la interfaz de usuario cuándo debe actualizarse el control.
    
**cbNotif**
  
> Recuento de bytes en la estructura a la que apunta el **miembro lpbNotif.** 
    
**lpszFilter**
  
> Puntero a una cadena de caracteres que describe qué caracteres se pueden especificar en un control de edición o cuadro combinado. Para otros tipos de controles, el **miembro lpszFilter** puede ser NULL. Para los controles de edición y cuadro combinado, debe ser una expresión regular que se aplique a un solo carácter a la vez. El mismo filtro se aplica a todos los caracteres del control. El formato de la cadena de filtro es el siguiente: 
    
|**Carácter**|**Descripción**|
|:-----|:-----|
| `*` <br/> | Se permite cualquier carácter (por ejemplo, `"*"` ).  <br/> |
| `[ ]` <br/> |Define un conjunto de caracteres (por ejemplo, `"[0123456789]"` .)  <br/> |
| `-` <br/> |Indica un intervalo de caracteres (por ejemplo, `"[a-z]"` ).  <br/> |
| `~` <br/> |Indica que estos caracteres no están permitidos (por ejemplo, `"[~0-9]")` . <br/>|   
| `\` <br/> |Se usa para citar cualquiera de los símbolos anteriores (por ejemplo, se permiten los caracteres `"[\-\\\[\]]"` -, \, [y ] ).  <br/> |
   
**ulItemID**
  
> Valor que identifica el control en el recurso de cuadro de diálogo. Para los controles de páginas con pestañas de tipo DTCT_PAGE el **miembro ulItemID** se usa opcionalmente para cargar el nombre del componente de la página desde un recurso de cadena. La información de posición y etiqueta se lee en el recurso del cuadro de diálogo. 
    
**ctl**
  
> Estructura que contiene los datos del control y corresponde a la propiedad PR_CONTROL_STRUCTURE **(** [PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)). Cada tipo de control tiene una estructura diferente.
    
## <a name="remarks"></a>Comentarios

La **estructura DTCTL** describe un control de cualquier tipo. La mayoría de sus miembros se usan para establecer propiedades en el control. 
  
El **miembro ctl** es una unión de estructuras que se relacionan con un tipo determinado de control. Si la **estructura DTCTL** describe un control de edición, por ejemplo, el miembro **ctl** apuntará a una [estructura DTBLEDIT.](dtbledit.md) Esta estructura corresponde a la propiedad PR_CONTROL_STRUCTURE **control.** La unión tiene como primer miembro una variable de tipo LPVOID para permitir la inicialización en tiempo de compilación de la **estructura DTCTL.** 
  
Aunque la [función BuildDisplayTable](builddisplaytable.md) usa la estructura **DTCTL** para crear la tabla para mostrar a partir de recursos de control, la estructura **DTCTL** nunca aparece en la propia tabla para mostrar. Esta estructura solo proporciona información a **BuildDisplayTable**.
  
En el **miembro ulCtlFlags,** cuatro DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT solo afectan a los controles de edición. Otros dos DT_REQUIRED y DT_SET_IMMEDIATE afectan a cualquier control editable. 
  
Los controles disponibles para un cuadro de diálogo son etiqueta, cuadro de texto, cuadro de texto con entrada de lápiz, lista, lista desplegable, cuadro combinado, casilla de verificación, cuadro de grupo, botón, botón de radio y página con pestañas.
  
Para obtener información general sobre las tablas para mostrar, vea [Tablas para mostrar.](display-tables.md) Para obtener información sobre cómo implementar una tabla para mostrar, vea [Implementing a Display Table](display-table-implementation.md).
  
## <a name="see-also"></a>Vea también

- [BuildDisplayTable](builddisplaytable.md)
- [DTBLBUTTON](dtblbutton.md)
- [DTBLCHECKBOX](dtblcheckbox.md)
- [DTBLCOMBOBOX](dtblcombobox.md)
- [DTBLDDLBX](dtblddlbx.md)
- [DTBLEDIT](dtbledit.md)
- [DTBLGROUPBOX](dtblgroupbox.md)
- [DTBLLABEL](dtbllabel.md)
- [DTBLLBX](dtbllbx.md)
- [DTBLMVDDLBOX](dtblmvddlbox.md)
- [DTBLMVLISTBOX](dtblmvlistbox.md)
- [DTBLPAGE](dtblpage.md)
- [DTBLRADIOBUTTON](dtblradiobutton.md)
- [Estructuras MAPI](mapi-structures.md)

