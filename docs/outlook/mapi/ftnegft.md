---
title: FtNegFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtNegFt
api_type:
- COM
ms.assetid: 639a408c-aed1-456b-9f75-9d6fb8dcb33b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: db208dad8697060e394b3ee037ea658cefbab669
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423387"
---
# <a name="ftnegft"></a>FtNegFt

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Calcula el complemento de los dos de un entero de 64 bits sin signo. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a>Parámetros

 _ft_
  
> [entrada] Estructura [FILETIME](filetime.md) que contiene el entero de 64 bits sin signo para el que se va a calcular el complemento de los dos. 
    
## <a name="return-value"></a>Valor devuelto

La **función FtNegFt** devuelve una **estructura FILETIME** que contiene el complemento de los dos enteros. El parámetro de entrada no cambia. 
  

