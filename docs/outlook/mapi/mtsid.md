---
title: MTSID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MTSID
api_type:
- COM
ms.assetid: 3d9bc643-332f-4c8e-83e6-ce9b15711945
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 96da91acec741322e6c07c64555171d35f0f7e00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435176"
---
# <a name="mtsid"></a>MTSID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un identificador de entrada del sistema de transporte de mensajes (MTS) X. 400. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Macros relacionadas:  <br/> |[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a>Members

 **cb**
  
> Número de bytes en la matriz que describe el miembro **abEntry** . 
    
 **abEntry**
  
> Matriz de bytes que contiene los datos del identificador de entrada MTS.
    
## <a name="remarks"></a>Comentarios

La estructura **MTSID** se usa únicamente para las asignaciones X. 400 de los identificadores de entrada MAPI. Corresponde a la estructura [FLATENTRY](flatentry.md) de MAPI. 
  
Un identificador de MTS tiene el mismo formato que un identificador de entrada MAPI o un valor de propiedad binario. Los identificadores de MTS pueden ser particularmente útiles para cancelar mensajes aplazados. 
  
## <a name="see-also"></a>Ver también



[FLATENTRY](flatentry.md)
  
[FLATMTSIDLIST](flatmtsidlist.md)


[Estructuras MAPI](mapi-structures.md)

