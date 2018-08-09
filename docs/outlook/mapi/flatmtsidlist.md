---
title: FLATMTSIDLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATMTSIDLIST
api_type:
- COM
ms.assetid: b66c2815-72bc-4535-b34c-899bb830f29e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ea841ef4bc551581fb2d9ca90201b4615e67f134
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816829"
---
# <a name="flatmtsidlist"></a>FLATMTSIDLIST

  
  
**Hace referencia a**: Outlook 
  
Contiene una matriz de estructuras [MTSID](mtsid.md) , cada uno de los cuales contiene un identificador de entrada del sistema (MTS) de transporte de mensaje X.400. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Macros relacionadas:  <br/> |[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMTSIDs;
  ULONG cbMTSIDs;
  BYTE abMTSIDs[MAPI_DIM];
} FLATMTSIDLIST, FAR *LPFLATMTSIDLIST;

```

## <a name="members"></a>Members

 **cMTSIDs**
  
> Recuento de estructuras **MTSID** en la matriz descritos por el miembro **abMTSIDs** . 
    
 **cbMTSIDs**
  
> Número de bytes de la matriz descritos por **abMTSIDs**.
    
 **abMTSIDs**
  
> Matriz de bytes que contiene una o más estructuras **MTSID** . 
    
## <a name="remarks"></a>Comentarios

Uso de la estructura **FLATMTSIDLIST** en mensajería X.400 corresponde al uso de la estructura [FLATENTRYLIST](flatentrylist.md) de mensajería MAPI. MAPI utiliza estructuras **FLATMTSIDLIST** para mantener las propiedades de X.400 durante el control de mensaje. Proveedores de servicios utilizan estructuras **FLATMTSIDLIST** al tratamiento de mensajes X.400 entrantes y salientes. 
  
En la matriz **abMTSIDs** , cada estructura **MTSID** se alinea en un límite alineado con naturalidad. Bytes adicionales se incluyen como relleno para realizar la alineación natural seguro entre los dos estructuras **MTSID** . La primera estructura **MTSID** en la matriz siempre se alinea correctamente debido a que el desplazamiento del miembro **abMTSIDs** es 8. Para calcular el desplazamiento de la estructura siguiente, utilice el tamaño de la primera entrada que se redondea hacia arriba hasta el próximo múltiplo de 4. Utilice la macro [CbNewMTSID](cbnewmtsid.md) para calcular el tamaño de una estructura **MTSID** . 
  
## <a name="see-also"></a>Vea también



[CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)
  
[FLATENTRYLIST](flatentrylist.md)
  
[MTSID](mtsid.md)


[Estructuras MAPI](mapi-structures.md)

