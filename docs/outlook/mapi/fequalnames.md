---
title: FEqualNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FEqualNames
api_type:
- COM
ms.assetid: 4dd58b0b-dc39-4782-a9ec-05e353c90927
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0d8d1b8509f699b20f6e436d8af2c1d0d97cf4ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816802"
---
# <a name="fequalnames"></a>FEqualNames

  
  
**Hace referencia a**: Outlook 
  
Determina si dos MAPI con nombre de las propiedades son los mismos. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a>Parámetros

 _lpName1_
  
> [entrada] Puntero a una estructura [MAPINAMEID](mapinameid.md) que describe la primera propiedad con nombre. 
    
 _lpName2_
  
> [entrada] Puntero a una estructura **MAPINAMEID** que describe la segunda propiedad con nombre. 
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> Los nombres de dos propiedades son iguales. 
    
FALSE 
  
> Los nombres de dos propiedades no son iguales.
    
## <a name="remarks"></a>Comentarios

La función **FEqualNames** es útil debido a que la estructura **MAPINAMEID** contiene un [GUID](guid.md) y puede representar el nombre de propiedad en más de una forma. Esto significa que no se pueden comparar las estructuras de dos métodos binario simple. 
  
El proceso de pruebas distingue mayúsculas de minúsculas para las cadenas de nombre de propiedad. 
  

