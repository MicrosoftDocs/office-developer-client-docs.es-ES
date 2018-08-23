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
ms.openlocfilehash: e84dbc0976f5c438a7e0b5fd7cddcbf1c0659f40
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574800"
---
# <a name="deinitmapiutil"></a>DeinitMapiUtil

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Libera las funciones de utilidad llamadas explícitamente por la función [ScInitMapiUtil](scinitmapiutil.md) o implícitamente por la función [MAPIInitialize](mapiinitialize.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a>Parámetros

Ninguna 
  
## <a name="return-value"></a>Valor devuelto

Ninguno 
  
## <a name="remarks"></a>Observaciones

Las funciones de versión de función de **DeinitMapiUtil** inicializadas con [ScInitMapiUtil](scinitmapiutil.md) o [MAPIInitialize](mapiinitialize.md). 
  
Una vez finalizada la utilización de las funciones llamado por **ScInitMapiUtil** , **DeinitMapiUtil** debe llamarse explícitamente para liberarlos. Por el contrario, [MAPIUninitialize](mapiuninitialize.md) implícitamente llama a **DeinitMapiUtil**. 
  

