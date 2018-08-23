---
title: DTPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTPAGE
api_type:
- COM
ms.assetid: 500f60ed-fdec-4d70-8cf5-664c46643956
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 769ae984e4b6e8610ca7909ea2ac714d9d04d698
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589675"
---
# <a name="dtpage"></a>DTPAGE

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe el cuadro de diálogo que se genera a partir de una tabla para mostrar por la función [BuildDisplayTable](builddisplaytable.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct DTPAGE
{
  ULONG cctl;
  LPSTR lpszResourceName;
  union
  {
    LPSTR lpszComponent;
    ULONG ulItemID;
  }
  LPDTCTL lpctl;
} DTPAGE, FAR *LPDTPAGE;

```

## <a name="members"></a>Members

 **cctl**
  
> Recuento de controles que señala el miembro **lpctl** . 
    
 **lpszResourceName**
  
> Puntero al nombre o número entero identificador para el recurso de cuadro de diálogo. 
    
 **lpszComponent**
  
> Puntero a la cadena que aparece en la sección **[Help File Mappings]** en MAPISVC.INF. Debido a que **lpszComponent** se encuentra en una unión con el miembro **ulItemID** , solo uno de estos miembros tiene datos válidos. 
    
 **ulItemID**
  
> Identificador de recurso de entero con un valor menor o igual que 65535 desde la que se puede leer el nombre de archivo de ayuda. Debido a que **ulItemID** se encuentra en una unión con el miembro **lpszComponent** , solo uno de estos miembros tiene datos válidos. 
    
 **lpctl**
  
> Puntero a una matriz de estructuras [DTCTL](dtctl.md) , uno para cada control en la página. 
    
## <a name="remarks"></a>Comentarios

Para identificar el archivo de ayuda para la página con fichas, establezca el miembro **lpszComponent** en una cadena codificado de forma rígida o el miembro **ulItemID** en un identificador de recurso de entero. 
  
Cada entrada en la sección **[Help File Mappings]** en MAPISVC. INF consta de una cadena de componente, no más de 30 caracteres, en el lado izquierdo y una ruta de acceso del archivo de Ayuda de la derecha. **UlItemID** y **lpszResourceName** se encuentran en el parámetro _hInstance_ del **BuildDisplayTable**. Para obtener más información, vea [MAPISVC. INF [asignaciones de archivo de ayuda] sección](mapisvc-inf-help-file-mappings-section.md).
  
Aunque **BuildDisplayTable** usa esta estructura para crear la tabla para mostrar de los recursos de control, la estructura **DTPAGE** nunca aparece en la propia tabla para mostrar. 
  
Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md). Para obtener información acerca de cómo implementar una tabla para mostrar, vea [implementar una tabla mostrar](display-table-implementation.md).
  
## <a name="see-also"></a>Recursos adicionales



[BuildDisplayTable](builddisplaytable.md)
  
[DTBLPAGE](dtblpage.md)
  
[DTCTL](dtctl.md)


[Estructuras MAPI](mapi-structures.md)

