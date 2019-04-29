---
title: GetInstance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetInstance
api_type:
- COM
ms.assetid: cb432d52-6c96-45d2-bbde-45b0de3f915c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 936a20c4236ab76e5acdb178737c3044d3f53bfe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418725"
---
# <a name="getinstance"></a>GetInstance

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Copia un valor dentro de una propiedad con varios valores en una propiedad de un solo valor del mismo tipo. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIUTIL. H  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a>Parameters

 _pvalMv_
  
> a Puntero a una estructura [SPropValue](spropvalue.md) que define una propiedad con varios valores. 
    
 _pvalSv_
  
> a Puntero a una propiedad de un solo valor para recibir datos. 
    
 _uliInst_
  
> a El número de instancia, es decir, el elemento de la matriz, del valor que se va a copiar de la estructura indicada por el parámetro _pvalMv_ . 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Si el valor copiado es demasiado grande para la memoria asignada, la función **getInstance** solo copia punteros en lugar de asignar memoria nueva. 
  

