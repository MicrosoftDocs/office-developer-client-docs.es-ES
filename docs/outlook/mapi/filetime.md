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
ms.openlocfilehash: a5f950907e2b14cb4101a094715c24b25beb2016
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816817"
---
# <a name="filetime"></a>FILETIME

  
  
**Hace referencia a**: Outlook 
  
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
  
## <a name="see-also"></a>Vea también



[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

