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
ms.openlocfilehash: 00355546717ca61492750cb1dd113d20114b0695
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334814"
---
# <a name="filetime"></a>FILETIME

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un valor de fecha y hora sin firmar de 64 bits para un archivo. Este valor representa el número de unidades de 100-nanosegundos desde el inicio del 1 de enero de 1601. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a>Members

 **dwLowDateTime**
  
> Valores de 32 bits de orden inferior del valor de hora del archivo. 
    
 **dwHighDateTime**
  
> 32 bits de orden superior del valor hora del archivo.
    
## <a name="remarks"></a>Comentarios

Una propiedad de tipo PT_SYSTIME tiene una estructura **FILETIME** para su valor. Dicha propiedad tiene un tipo de datos **FILETIME** para el miembro de **valor** en su definición en una estructura [SPropValue](spropvalue.md) . 
  
La definición de la estructura **FILETIME** se encuentra en la _Referencia del programador de Win32_ y en el archivo de encabezado MAPI Mapidefs. h. MAPI define la estructura de forma condicional para asegurarse de que se define cuando la definición de Win32 no está disponible. 
  
## <a name="see-also"></a>Vea también



[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

