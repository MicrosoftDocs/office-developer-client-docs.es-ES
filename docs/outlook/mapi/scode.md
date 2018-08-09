---
title: SCODE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HRESULT
api_type:
- COM
ms.assetid: 2348cce1-07c3-49ed-ae03-79e477d3c6c2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6cd9dfe8fabd1ae7a4389550c628fb7ceff09ea8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820581"
---
# <a name="scode"></a>SCODE

**Hace referencia a**: Outlook 
  
Un valor de estado de 32 bits que se usa para describir un error o advertencia. 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a>Comentarios

El tipo de datos **SCODE** es el mismo que el tipo de datos [HRESULT](hresult.md) . 
  
Un valor **SCODE** se divide en cuatro campos: 
  
- Un código de gravedad de bit único que se establece en 0 para indicar éxito y 1 para indicar un error.
    
- Un campo reservado de 11 bits
    
- Un código de servicio de 4 bits que indica el área responsable del error o advertencia.
    
- Un error de 16 bits o código de advertencia que se describe el problema que es la causa del error o advertencia.
    
Muchas de las funciones MAPI y métodos devuelven valores **SCODE** definidos como tipos de datos **HRESULT** igual que las funciones y métodos OLE. OLE define varias macros que se pueden usar para convertir entre un **SCODE** y un **HRESULT**.
  
> [!NOTE]
> En MAPI de 64 bits, **SCODE** sigue siendo un valor de 32 bits. 
  
Para obtener más información acerca de cómo utiliza el tipo de datos **SCODE** MAPI, vea [Control de errores](error-handling-in-mapi.md). Para obtener más información acerca de OLE y el tipo de datos **SCODE** , vea la *referencia del programador de OLE* . 
  
## <a name="see-also"></a>Vea también



[[HRESULT]](hresult.md)


[Tipos de datos MAPI](mapi-data-types.md)

