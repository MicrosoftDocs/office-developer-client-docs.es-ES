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
ms.openlocfilehash: 8f71b30bd02af8f768da86218456feadda8ea1b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414805"
---
# <a name="fequalnames"></a>FEqualNames

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Determina si dos propiedades con nombre de MAPI son iguales. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a>Parameters

 _lpName1_
  
> a Puntero a una estructura [MAPINAMEID](mapinameid.md) que describe la primera propiedad con nombre. 
    
 _lpName2_
  
> a Puntero a una estructura **MAPINAMEID** que describe la segunda propiedad con nombre. 
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> Los dos nombres de propiedad son iguales. 
    
FALSE 
  
> Los dos nombres de propiedad no son iguales.
    
## <a name="remarks"></a>Comentarios

La función **FEqualNames** es útil porque la estructura **MAPINAMEID** contiene un [GUID](guid.md) y puede representar el propio nombre de la propiedad de más de una forma. Esto significa que las dos estructuras no se pueden comparar por los métodos binarios simples. 
  
El proceso de prueba distingue entre mayúsculas y minúsculas para las cadenas de nombres de propiedades. 
  

