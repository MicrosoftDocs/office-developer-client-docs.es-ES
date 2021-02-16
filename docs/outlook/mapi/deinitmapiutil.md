---
title: DeinitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeinitMapiUtil
api_type:
- HeaderDef
ms.assetid: e0b8dc9c-cc46-4d27-9497-7a55a0bfdff5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a9654efc34280941cdbc727bce9912a0a39d0fb9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427349"
---
# <a name="deinitmapiutil"></a>DeinitMapiUtil

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Libera funciones de utilidad llamadas explícitamente por [la función ScInitMapiUtil](scinitmapiutil.md) o implícitamente por [la función MAPIInitialize.](mapiinitialize.md) 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a>Parámetros

Ninguno 
  
## <a name="return-value"></a>Valor devuelto

Ninguno 
  
## <a name="remarks"></a>Comentarios

Las **funciones de lanzamiento de la función DeinitMapiUtil** inicializadas con [ScInitMapiUtil](scinitmapiutil.md) o [MAPIInitialize](mapiinitialize.md). 
  
Cuando se complete el uso de las funciones llamadas por **ScInitMapiUtil,** se debe llamar explícitamente **a DeinitMapiUtil** para liberarlas. Por el contrario, [MAPIUninitialize](mapiuninitialize.md) llama implícitamente **a DeinitMapiUtil**. 
  

