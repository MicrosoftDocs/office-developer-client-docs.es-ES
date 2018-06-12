---
title: ScRelocProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScRelocProps
api_type:
- COM
ms.assetid: 4aafb254-6074-4a7c-b915-d3d33304ac38
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 06590fe55cb02b1abf036156877fd308548436f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820618"
---
# <a name="screlocprops"></a>ScRelocProps

  
  
**Se aplica a**: Outlook 
  
Ajusta los punteros en una matriz de [SPropValue](spropvalue.md) después de que se han copiado o movido a una nueva ubicación de la matriz y sus datos. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Sintaxis

 _cprop_
  
> [entrada] Recuento de propiedades de la matriz indicada por el parámetro _rgprop_ . 
    
 _rgprop_
  
> [entrada] Puntero a una matriz de estructuras [SPropValue](spropvalue.md) para que los punteros son va a ajustar. 
    
 _pvBaseOld_
  
> [entrada] Puntero a la dirección base original de la matriz indicada por el parámetro _rgprop_ . 
    
 _pvBaseNew_
  
> [entrada] Puntero a la nueva dirección de base de la matriz indicada por el parámetro _rgprop_ . 
    
 _placa de circuitos impresos_
  
> [entrada, salida] Puntero opcional para el tamaño, en bytes, de la matriz indicada por el parámetro _pvBaseNew_ . Si no es NULL, el parámetro _pcb_ se establece en el número de bytes que se almacenan en el parámetro _pvD_ . 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> Punteros se ajustaron correctamente.
    
MAPI_E_INVALID_PARAMETER
  
> Uno o ambos parámetros no son válidos, o se encontró un tipo de propiedad desconocido.
    
## <a name="remarks"></a>Notas

La función **ScRelocProps** funciona en la suposición de que la matriz de valores de propiedad para la que se ajustan punteros se asignó originalmente en una sola llamada similar a una llamada a la función **ScCopyProps** . Si una aplicación de cliente o un proveedor de servicios está trabajando con un valor de la propiedad que se genera a partir de disjuntos bloques de memoria, que debe usar [ScCopyProps](sccopyprops.md) para copiar las propiedades en su lugar. 
  
 **ScRelocProps** se utiliza para mantener la validez de punteros en una matriz de [SPropValue](spropvalue.md) . Para mantener la validez de punteros cuando dicha matriz a escritura y lectura de un disco, realice las siguientes operaciones: 
  
1. Antes de escribir la matriz y los datos en un disco, llame a **ScRelocProps** en la matriz con el parámetro _pvBaseNew_ apuntar a algún valor estándar cero, por ejemplo. 
    
2. Después de leer la matriz y los datos de un disco, llame a **ScRelocProps** en la matriz con el parámetro _pvBaseOld_ igual que el mismo valor estándar utilizado en el paso 1. Deben leer la matriz y los datos en un búfer creado con una única asignación. 
    
3. El parámetro _pcb_ **ScRelocProps** es opcional. 
    
## <a name="see-also"></a>Ver también



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ScCountProps](sccountprops.md)
  
[ScDupPropset](scduppropset.md)
  
[ScRelocNotifications](screlocnotifications.md)

