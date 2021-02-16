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
ms.openlocfilehash: ad8aec8d015849965bea6ac011c8a45e75c69ca1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408225"
---
# <a name="dtpage"></a>DTPAGE

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe el cuadro de diálogo creado a partir de una tabla para mostrar mediante la [función BuildDisplayTable.](builddisplaytable.md) 
  
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

## <a name="members"></a>Miembros

 **cctl**
  
> Recuento de controles a los que apunta el **miembro lpctl.** 
    
 **lpszResourceName**
  
> Puntero al nombre o al identificador entero del recurso de cuadro de diálogo. 
    
 **lpszComponent**
  
> Puntero a la cadena que aparece en la **sección [Asignaciones** de archivos de Ayuda] en MAPISVC.INF. Dado **que lpszComponent** está en una unión con el **miembro ulItemID,** solo uno de estos miembros tiene datos válidos. 
    
 **ulItemID**
  
> Identificador de recurso entero con un valor menor o igual que 65535 desde el que se puede leer el nombre del archivo de Ayuda. Dado **que ulItemID** está en una unión con el **miembro lpszComponent,** solo uno de estos miembros tiene datos válidos. 
    
 **lpctl**
  
> Puntero a una matriz [de estructuras DTCTL,](dtctl.md) una para cada control de la página. 
    
## <a name="remarks"></a>Comentarios

Para identificar el archivo de Ayuda de la página con fichas, establezca el miembro **lpszComponent** en una cadena codificada de forma fija o el miembro **ulItemID** en un identificador de recurso entero. 
  
Cada entrada de la **sección [Asignaciones de** archivos de ayuda] en MAPISVC. INF consta de una cadena de componente, que no tiene más de 30 caracteres, en el lado izquierdo y una ruta de acceso del archivo de Ayuda a la derecha. Tanto **ulItemID** como **lpszResourceName** se encuentran en el parámetro  _hInstance_ de **BuildDisplayTable**. Para obtener más información, vea [MAPISVC. INF [Asignaciones de archivo de ayuda] Sección](mapisvc-inf-help-file-mappings-section.md).
  
Aunque **BuildDisplayTable** usa esta estructura para crear la tabla para mostrar a partir de recursos de control, la estructura **DTPAGE** nunca aparece en la propia tabla para mostrar. 
  
Para obtener información general sobre las tablas para mostrar, vea [Tablas para mostrar.](display-tables.md) Para obtener información acerca de cómo implementar una tabla para mostrar, vea [Implementar una tabla para mostrar.](display-table-implementation.md)
  
## <a name="see-also"></a>Consulte también



[BuildDisplayTable](builddisplaytable.md)
  
[DTBLPAGE](dtblpage.md)
  
[DTCTL](dtctl.md)


[Estructuras MAPI](mapi-structures.md)

