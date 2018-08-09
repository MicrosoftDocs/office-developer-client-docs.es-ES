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
ms.openlocfilehash: ae6f7d7066638ef1b149d3e411443384d531184d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816636"
---
# <a name="deinitmapiutil"></a>DeinitMapiUtil

  
  
**Hace referencia a**: Outlook 
  
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

Ninguno 
  
## <a name="return-value"></a>Valor devuelto

Ninguno 
  
## <a name="remarks"></a>Observaciones

Las funciones de versión de función de **DeinitMapiUtil** inicializadas con [ScInitMapiUtil](scinitmapiutil.md) o [MAPIInitialize](mapiinitialize.md). 
  
Una vez finalizada la utilización de las funciones llamado por **ScInitMapiUtil** , **DeinitMapiUtil** debe llamarse explícitamente para liberarlos. Por el contrario, [MAPIUninitialize](mapiuninitialize.md) implícitamente llama a **DeinitMapiUtil**. 
  

