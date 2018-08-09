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
ms.openlocfilehash: 68c621f5f73073ed127767cc1db189769dab227d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816766"
---
# <a name="dtctl"></a>DTCTL

**Hace referencia a**: Outlook 
  
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
  
> Tipo de control que se incluye en el miembro **ctl** y corresponde a la propiedad del control **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)). Los valores posibles son los siguientes:
    
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
  
> Control de casilla de verificación.
    
DTCT_GROUPBOX 
  
> Control de cuadro de grupo.
    
DTCT_BUTTON 
  
> Control de botón.
    
DTCT_PAGE 
  
> Control de la página con fichas.
    
DTCT_RADIOBUTTON 
  
> Control de botón de radio.
    
DTCT_MVLISTBOX 
  
> Control de lista con múltiples valores.
    
DTCT_MVDDLBX 
  
> Control de lista desplegable con múltiples valores.
    
**ulCtlFlags**
  
> Máscara de bits de indicadores que se describe las características del control y se corresponde con la propiedad del control **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)). Estas marcas se pueden establecer para las casillas de verificación, cuadros combinados, cuadros de lista y sólo controles de edición. Los valores posibles son los siguientes:
    
DT_ACCEPT_DBCS 
  
> Se acepta el formato ANSI o DBCS. Esta marca es válida para sólo controles de edición.
    
DT_EDITABLE 
  
> Un usuario puede modificar el texto en el control. 
    
DT_MULTILINE 
  
> El control puede contener varias líneas de texto. Esta marca es válida para sólo controles de edición.
    
DT_PASSWORD_EDIT 
  
> El control contiene una contraseña; por lo tanto, el contenido del control no debe mostrarse al usuario. Esta marca es válida para sólo controles de edición.
    
DT_REQUIRED 
  
> Se requiere el control de cuadro de diálogo. Esta marca sólo es válida para los controles de cuadro combinado y de edición.
    
DT_SET_IMMEDIATE 
  
> Habilita la salida inmediata de un valor tras un cambio en el control. Esto permite una relación de dependencia entre dos controles. 
    
**lpbNotif**
  
> Puntero a una estructura que consta de una estructura [GUID](guid.md) , para representar el proveedor de servicios y un identificador para el control. Los miembros de **lpbNotif** y **cbNotif** se corresponden con la propiedad del control **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) y se usan para notificar a la interfaz de usuario cuando el control tiene que actualizar.
    
**cbNotif**
  
> Recuento de bytes de la estructura que señala el miembro **lpbNotif** . 
    
**lpszFilter**
  
> Puntero a una cadena de caracteres que se describe los caracteres que se puede introducir en un control de cuadro combinado o de edición. Para otros tipos de controles, el miembro **lpszFilter** puede ser NULL. Para los controles de cuadro combinado y de edición, debe ser una expresión regular que se aplica a un solo carácter a la vez. El mismo filtro se aplica a todos los caracteres en el control. El formato de la cadena de filtro es como sigue: 
    
|**Carácter**|**Descripción**|
|:-----|:-----|
| `*` <br/> | Se permite cualquier carácter (por ejemplo, `"*"`).  <br/> |
| `[ ]` <br/> |Define un conjunto de caracteres (por ejemplo, `"[0123456789]"`.)  <br/> |
| `-` <br/> |Indica un intervalo de caracteres (por ejemplo, `"[a-z]"`).  <br/> |
| `~` <br/> |Indica que no se permiten estos caracteres (por ejemplo, `"[~0-9]")`. <br/>|   
| `\` <br/> |Utilizada para entrecomillar cualquiera de los símbolos anteriores (por ejemplo, `"[\-\\\[\]]"` significa-, \, [, y] se permiten caracteres).  <br/> |
   
**ulItemID**
  
> Valor que identifica el control en el recurso de cuadro de diálogo. Para controles de páginas con fichas del tipo DTCT_PAGE la **ulItemID** miembro, opcionalmente, se utiliza para cargar el nombre del componente de la página desde un recurso de cadena. Posición y la información de la etiqueta se leen desde el recurso de cuadro de diálogo. 
    
**CTL**
  
> Una estructura que contiene los datos para el control y se corresponde con la propiedad del control **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)). Cada tipo de control tiene una estructura diferente.
    
## <a name="remarks"></a>Comentarios

La estructura **DTCTL** describe un control de cualquier tipo. La mayoría de sus miembros se usa para establecer las propiedades en el control. 
  
El miembro **ctl** es la unión de las estructuras que se relacionan con un tipo concreto de control. Si la estructura **DTCTL** que describe un control de edición, por ejemplo, el miembro **ctl** señalará a una estructura [DTBLEDIT](dtbledit.md) . Esta estructura corresponde a la propiedad del control **PR_CONTROL_STRUCTURE** . La unión tiene como su primer miembro de una variable de tipo LPVOID para permitir la inicialización en tiempo de compilación de la estructura **DTCTL** . 
  
Aunque la función [BuildDisplayTable](builddisplaytable.md) utiliza la estructura **DTCTL** para la creación de la tabla para mostrar de los recursos de control, la estructura **DTCTL** nunca aparece en la propia tabla para mostrar. Esta estructura sólo suministra información a **BuildDisplayTable**.
  
En el miembro **ulCtlFlags** , cuatro indicadores DT_ACCEPT_DBCS, DT_EDITABLE, afectan al DT_MULTILINE_and DT_PASSWORD_EDIT de sólo controles de edición. Otros dos DT_REQUIRED y DT_SET_IMMEDIATE afecta a cualquier control modificable. 
  
Los controles disponibles para un cuadro de diálogo son etiqueta, cuadro de texto, cuadro de texto compatible con entrada de lápiz, lista, lista desplegable, cuadro combinado, casilla de verificación, cuadro de grupo, botón, botón de radio y página con fichas.
  
Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md). Para obtener información acerca de cómo implementar una tabla para mostrar, vea [implementar una tabla mostrar](display-table-implementation.md).
  
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

