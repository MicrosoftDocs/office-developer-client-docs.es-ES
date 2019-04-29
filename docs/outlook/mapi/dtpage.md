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
  
Describe el cuadro de diálogo que se genera a partir de una tabla de presentación por la función [BuildDisplayTable](builddisplaytable.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
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

 **CCTL**
  
> Número de controles a los que apunta el miembro **lpctl** . 
    
 **lpszResourceName**
  
> Puntero al nombre o al identificador entero del recurso de cuadro de diálogo. 
    
 **lpszComponent**
  
> Puntero a la cadena que aparece en la sección **[file mappings de la ayuda]** en MAPISVC. inf. Como **lpszComponent** está en una unión con el miembro **ulItemID** , solo uno de estos miembros tiene datos válidos. 
    
 **ulItemID**
  
> Identificador de recursos entero con un valor inferior o igual a 65535 desde el que se puede leer el nombre del archivo de ayuda. Como **ulItemID** está en una unión con el miembro **lpszComponent** , solo uno de estos miembros tiene datos válidos. 
    
 **lpctl**
  
> Puntero a una matriz de estructuras [DTCTL](dtctl.md) , una para cada control de la página. 
    
## <a name="remarks"></a>Comentarios

Para identificar el archivo de ayuda de la página con fichas, establezca el miembro **lpszComponent** en una cadena codificada de forma rígida, o bien el miembro **ulItemID** en un identificador de recursos entero. 
  
Cada entrada de la sección **[file mappings de la ayuda]** de MAPISVC. INF consta de una cadena de componente, de no más de 30 caracteres, en el lado izquierdo y de una ruta de acceso del archivo de ayuda a la derecha. Tanto **ulItemID** como **lpszResourceName** se encuentran en el parámetro _hInstance_ de **BuildDisplayTable**. Para obtener más información, vea [MAPISVC. Sección INF [asignaciones de archivos de ayuda]](mapisvc-inf-help-file-mappings-section.md).
  
Aunque **BuildDisplayTable** usa esta estructura para compilar la tabla de presentación a partir de los recursos de control, la estructura **DTPAGE** nunca aparece en la propia tabla de presentación. 
  
Para obtener información general sobre las tablas de presentación, consulte [Display tables](display-tables.md). Para obtener información acerca de cómo implementar una tabla de visualización, consulte [Implementing a display Table](display-table-implementation.md).
  
## <a name="see-also"></a>Ver también



[BuildDisplayTable](builddisplaytable.md)
  
[DTBLPAGE](dtblpage.md)
  
[DTCTL](dtctl.md)


[Estructuras MAPI](mapi-structures.md)

