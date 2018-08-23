---
title: ScCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyProps
api_type:
- COM
ms.assetid: 08bc256c-9706-4f3e-9a12-3e9cca5e4caa
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: eb3b3b3c9c2e9cffb77febf9c96baed40ce3f9e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566225"
---
# <a name="sccopyprops"></a>ScCopyProps

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Copias de las propiedades definidas por una matriz de estructuras [SPropValue](spropvalue.md) a un nuevo destino. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
SCODE ScCopyProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parámetros

 _cprop_
  
> [entrada] Recuento de propiedades que se va a copiar. 
    
 _rgprop_
  
> [entrada] Puntero a una matriz de estructuras [SPropValue](spropvalue.md) que definen las propiedades que se va a copiar. El parámetro _rgprop_ no tiene para que apunte al principio de la matriz, pero debe apuntar al principio de una de las estructuras de **SPropValue** en la matriz. 
    
 _pvDst_
  
> [entrada] Puntero a la posición inicial en la memoria a la que esta función copia las propiedades. 
    
 _placa de circuitos impresos_
  
> [out] Puntero opcional para el tamaño, en bytes, del bloque de memoria indicada por el parámetro _pvDst_ . 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> Las propiedades se han copiado correctamente.
    
MAPI_E_INVALID_PARAMETER
  
> Se encontró un tipo de propiedad desconocido.
    
## <a name="remarks"></a>Comentarios

La nueva matriz y sus datos residen en un búfer creado con una única asignación, y la función [ScRelocProps](screlocprops.md) puede usarse para ajustar los punteros en las estructuras de [SPropValue](spropvalue.md) individuales. Antes de este ajuste, los punteros son válidos. 
  
 **ScCopyProps** mantiene el orden de propiedad original de la matriz de propiedad copiados. 
  
El parámetro _pcb_ es opcional; Si no es NULL, se establece el número de bytes que se almacenan en el parámetro _pvDst_ . 
  
## <a name="see-also"></a>Recursos adicionales



[ScDupPropset](scduppropset.md)

