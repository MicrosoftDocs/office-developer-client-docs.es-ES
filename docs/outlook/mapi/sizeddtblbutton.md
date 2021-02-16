---
title: SizedDtblButton
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblButton
api_type:
- COM
ms.assetid: ee73ced9-14d8-4a30-9b9f-d54ed9c3a454
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a7d62d29638ae234667eb33a8103fb3a716afc32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421917"
---
# <a name="sizeddtblbutton"></a>SizedDtblButton

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una estructura con nombre que incluye una [estructura DTBLBUTTON](dtblbutton.md) para describir un botón y una etiqueta de una longitud especificada. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionada:  <br/> |**DTBLBUTTON** <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a>Parámetros

 _n_
  
> Longitud de la etiqueta que se incluirá en la nueva estructura.
    
 _s_
  
> Nombre de la nueva estructura.
    
## <a name="remarks"></a>Comentarios

La nueva estructura se crea con los siguientes miembros:
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a>Consulte también



[DTBLBUTTON](dtblbutton.md)


[Macros relacionadas con estructuras](macros-related-to-structures.md)

