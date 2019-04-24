---
title: SizedDtblGroupBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblGroupBox
api_type:
- COM
ms.assetid: 7ca01bf7-5185-41cc-907e-01f256345997
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0a9bda8831f4a38b62d71a54115c40bb3374d97d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282736"
---
# <a name="sizeddtblgroupbox"></a>SizedDtblGroupBox

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una estructura con nombre que incluye una estructura [DTBLGROUPBOX](dtblgroupbox.md) para describir un control de cuadro de grupo y una etiqueta de una longitud especificada. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Estructura relacionada:  <br/> |**DTBLGROUPBOX** <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a>Parameters

_n_
  
> Longitud de la etiqueta del cuadro de grupo. 
    
_u_
  
> Nombre de la nueva estructura.
    
## <a name="remarks"></a>Comentarios

La macro **SizedDtblGroupBox** permite definir un control de cuadro de grupo cuando se conoce la longitud de la etiqueta. La nueva estructura se crea con los siguientes miembros: 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

Para usar un puntero a la estructura resultante desde la macro **SizedDtblGroupBox** como un puntero de estructura **DTBLGROUPBOX** , realice la siguiente conversión: 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a>Vea también

- [DTBLGROUPBOX](dtblgroupbox.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

