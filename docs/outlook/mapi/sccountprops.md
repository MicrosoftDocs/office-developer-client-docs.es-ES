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
ms.openlocfilehash: 49634bda487143ddd8d8806b94f6c451ccf57b75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351320"
---
# <a name="sccountprops"></a>ScCountProps

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Determina el tamaño, en bytes, de una matriz de valores de propiedad y valida la memoria asociada a la matriz. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parameters

 _cprop_
  
> a Número de propiedades de la matriz indicada por el parámetro _rgprop_ . 
    
 _rgprop_
  
> a Puntero a un rango de una matriz de estructuras [SPropValue](spropvalue.md) que define las propiedades cuyo tamaño se va a determinar. Este intervalo no necesariamente comienza al principio de la matriz. 
    
 _impreso_
  
> contempla Puntero opcional al tamaño, en bytes, de la matriz de propiedades.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores. 
    
MAPI_E_INVALID_PARAMETER 
  
> Al menos una propiedad de la matriz de valores de propiedad tiene un identificador de PROP_ID_NULL o PROP_ID_INVALID, o bien la matriz de propiedades contiene una propiedad multivalor sin valores de propiedad.
    
## <a name="remarks"></a>Comentarios

Si se pasa NULL en el parámetro _PCB_ , la función **ScCountProps** valida la matriz de notificaciones, pero no se realiza ningún recuento. Si se pasa un valor no nulo en _PCB_, la función **ScCountNotifications** determina el tamaño de la matriz y almacena la causa _PCB_. El parámetro _PCB_ debe ser lo suficientemente grande como para contener toda la matriz. 
  
A medida que se recuento, **ScCountProps** valida la memoria asociada a la matriz. **ScCountProps** solo funciona con propiedades sobre las que MAPI tiene información. 
  
## <a name="see-also"></a>Vea también



[PropCopyMore](propcopymore.md)

