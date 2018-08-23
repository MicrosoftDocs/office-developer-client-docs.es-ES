---
title: ScCountProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCountProps
api_type:
- COM
ms.assetid: 76e4cc52-e1a0-4e0b-a2a6-a17644f6b2e7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ee004bdfb8d13537fd8823225f155223ebc76ca7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583354"
---
# <a name="sccountprops"></a>ScCountProps

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Determina el tamaño, en bytes, de una matriz de valores de propiedad y valida la memoria asociada a la matriz. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parámetros

 _cprop_
  
> [entrada] Recuento de propiedades en la matriz indicada por el parámetro _rgprop_ . 
    
 _rgprop_
  
> [entrada] Puntero a un rango en una matriz de estructuras [SPropValue](spropvalue.md) que define las propiedades cuyo tamaño es que se determinará. Este intervalo no se inicia necesariamente al principio de la matriz. 
    
 _placa de circuitos impresos_
  
> [out] Puntero opcional para el tamaño, en bytes, de la matriz de propiedad.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores. 
    
MAPI_E_INVALID_PARAMETER 
  
> Al menos una propiedad en la matriz de valores de propiedad tiene un identificador de PROP_ID_NULL o PROP_ID_INVALID o la matriz de propiedad contiene una propiedad multivalor sin valores de propiedad.
    
## <a name="remarks"></a>Comentarios

Si se pasa NULL en el parámetro _pcb_ , la función **ScCountProps** valida la matriz de notificaciones, pero recuento no se realiza. Si se pasa un valor no nulo en _placa de circuitos impresos_, la función **ScCountNotifications** determina el tamaño de la matriz y almacena la causa _placa de circuitos impresos_. El parámetro _pcb_ debe ser lo suficientemente grande como para contener toda la matriz. 
  
Tal y como lo está contando, **ScCountProps** valida la memoria asociada a la matriz. **ScCountProps** sólo funciona con las propiedades MAPI sobre qué dispone de información. 
  
## <a name="see-also"></a>Recursos adicionales



[PropCopyMore](propcopymore.md)

