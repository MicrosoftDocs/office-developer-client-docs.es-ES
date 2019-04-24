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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282764"
---
# <a name="sizeddtblbutton"></a>SizedDtblButton

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una estructura con nombre que incluye una estructura [DTBLBUTTON](dtblbutton.md) para describir un botón y una etiqueta de una longitud determinada. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Estructura relacionada:  <br/> |**DTBLBUTTON** <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a>Parameters

 _n_
  
> Longitud de la etiqueta que se va a incluir en la nueva estructura.
    
 _u_
  
> Nombre de la nueva estructura.
    
## <a name="remarks"></a>Comentarios

La nueva estructura se crea con los siguientes miembros:
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a>Vea también



[DTBLBUTTON](dtblbutton.md)


[Macros relacionadas con estructuras](macros-related-to-structures.md)

