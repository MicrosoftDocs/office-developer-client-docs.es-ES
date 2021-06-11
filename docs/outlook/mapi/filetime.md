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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409506"
---
# <a name="filetime"></a>FILETIME

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un valor de fecha y hora de 64 bits sin signo para un archivo. Este valor representa el número de unidades de 100 nanosegundos desde el inicio del 1 de enero de 1601. 
  
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
  
> Orden bajo 32 bits del valor de tiempo del archivo. 
    
 **dwHighDateTime**
  
> Orden alto 32 bits del valor de tiempo del archivo.
    
## <a name="remarks"></a>Comentarios

Una propiedad de tipo PT_SYSTIME tiene una **estructura FILETIME** para su valor. Dicha propiedad tiene un tipo **de datos FILETIME** para el **miembro Value** en su definición en una [estructura SPropValue.](spropvalue.md) 
  
La definición de la **estructura FILETIME** se encuentra en la Referencia del programador de  _Win32_ y en el archivo de encabezado MAPI Mapidefs.h. MAPI define la estructura condicionalmente para asegurarse de que se define cuando la definición de Win32 no está disponible. 
  
## <a name="see-also"></a>Vea también



[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

