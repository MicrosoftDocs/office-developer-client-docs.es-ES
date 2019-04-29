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
ms.openlocfilehash: bd9bfe4d1411b84a7811235aa68728afaefe64ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439222"
---
# <a name="flatmtsidlist"></a>FLATMTSIDLIST

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de estructuras [MTSID](mtsid.md) , cada una de las cuales contiene un identificador de entrada del sistema de transporte de mensajes (mts) X. 400. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
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
  
> Número de estructuras **MTSID** en la matriz descrita por el miembro **abMTSIDs** . 
    
 **cbMTSIDs**
  
> Número de bytes de la matriz descrita por **abMTSIDs**.
    
 **abMTSIDs**
  
> Matriz de bytes que contiene una o varias estructuras **MTSID** . 
    
## <a name="remarks"></a>Comentarios

El uso de la estructura **FLATMTSIDLIST** en la mensajería X. 400 corresponde al uso de la estructura [FLATENTRYLIST](flatentrylist.md) en la mensajería MAPI. MAPI usa las estructuras **FLATMTSIDLIST** para mantener las propiedades X. 400 durante el tratamiento de mensajes. Los proveedores de servicios usan estructuras **FLATMTSIDLIST** al controlar mensajes X. 400 entrantes y salientes. 
  
En la matriz **abMTSIDs** , cada estructura **MTSID** está alineada en un límite naturalmente alineado. Los bytes adicionales se incluyen como relleno para garantizar la alineación natural entre dos estructuras **MTSID** . La primera estructura **MTSID** de la matriz siempre está alineada correctamente porque el desplazamiento del miembro **abMTSIDs** es 8. Para calcular el desplazamiento de la estructura siguiente, use el tamaño de la primera entrada redondeada hasta el siguiente múltiplo de 4. Use la macro [CbNewMTSID](cbnewmtsid.md) para calcular el tamaño de una estructura **MTSID** . 
  
## <a name="see-also"></a>Ver también



[CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)
  
[FLATENTRYLIST](flatentrylist.md)
  
[MTSID](mtsid.md)


[Estructuras MAPI](mapi-structures.md)

