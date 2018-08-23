---
title: FILETIME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FILETIME
api_type:
- COM
ms.assetid: 4af8e79a-697e-44a1-8576-fdc57726e9ef
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d58a216a41ff8fe93387ce6d9d1d6aa16f36f224
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583256"
---
# <a name="filetime"></a>FILETIME

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una fecha de 64 bits sin signo y el valor de tiempo de un archivo. Este valor representa el número de unidades de 100 nanosegundos desde el inicio del 1 de enero de 1601. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a>Members

 **dwLowDateTime**
  
> Valor de tiempo de 32 bits de orden inferior del archivo. 
    
 **FILETIME**
  
> Valor de tiempo de 32 bits de orden superior del archivo.
    
## <a name="remarks"></a>Comentarios

Una propiedad de tipo PT_SYSTIME tiene una estructura **FILETIME** para su valor. Este tipo de propiedad tiene un tipo de datos **FILETIME** para el miembro de **valor** en su definición en una estructura [SPropValue](spropvalue.md) . 
  
La definición de la estructura **FILETIME** es en la _referencia del programador de Win32_ y en el archivo de encabezado Mapidefs.h MAPI. MAPI define la estructura de forma condicional para asegurarse de que se define cuando no está disponible la definición de Win32. 
  
## <a name="see-also"></a>Recursos adicionales



[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

