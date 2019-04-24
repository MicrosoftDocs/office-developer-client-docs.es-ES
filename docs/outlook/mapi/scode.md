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
ms.openlocfilehash: 4208f51af44055b03c65b51c9b3d94e947dc9b68
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351243"
---
# <a name="scode"></a>SCODE

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un valor de estado de 32 bits que se usa para describir un error o una advertencia. 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a>Comentarios

El tipo de datos **SCODE** es el mismo que el tipo de datos [HRESULT](hresult.md) . 
  
Un valor **SCODE** se divide en cuatro campos: 
  
- Un código de gravedad de un solo bit que se establece en 0 para indicar correcto y 1 para indicar un error.
    
- Un campo reservado de 11 bits
    
- Un código de instalación de 4 bits que indica el área responsable del error o advertencia.
    
- Un código de advertencia o error de 16 bits que describe el problema que está causando el error o la advertencia.
    
Muchas de las funciones y métodos de MAPI devuelven los valores de **SCODE** definidos como tipos de datos **HRESULT** como los métodos y funciones OLE. OLE define varias macros que se pueden usar para realizar la conversión entre **SCODE** y **HRESULT**.
  
> [!NOTE]
> En MAPI de 64 bits, **SCODE** sigue siendo un valor de 32 bits. 
  
Para obtener más información acerca de cómo MAPI usa el tipo de datos **SCODE** , consulte [control de errores](error-handling-in-mapi.md). Para obtener más información acerca de OLE y el tipo de datos **SCODE** , vea la *Referencia del programador de OLE* . 
  
## <a name="see-also"></a>Vea también



[[HRESULT]](hresult.md)


[Tipos de datos MAPI](mapi-data-types.md)

