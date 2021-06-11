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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c73fb96c9620a90ab0505b394fcb9853d02dcde5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421091"
---
# <a name="screlocprops"></a>ScRelocProps

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Ajusta los punteros de una matriz [SPropValue](spropvalue.md) después de que la matriz y sus datos se hayan copiado o movido a una nueva ubicación. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parameters

 _cprop_
  
> [in] Recuento de propiedades de la matriz apuntadas por el _parámetro rgprop._ 
    
 _rgprop_
  
> [in] Puntero a una matriz de [estructuras SPropValue](spropvalue.md) para las que se deben ajustar los punteros. 
    
 _pvBaseOld_
  
> [in] Puntero a la dirección base original de la matriz apuntada por el _parámetro rgprop._ 
    
 _pvBaseNew_
  
> [in] Puntero a la nueva dirección base de la matriz señalada por el _parámetro rgprop._ 
    
 _pcb_
  
> [in, out] Puntero opcional al tamaño, en bytes, de la matriz indicada por el _parámetro pvBaseNew._ Si no es NULL, el _parámetro pcb_ se establece en el número de bytes almacenados en el _parámetro pvD._ 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> Los punteros se ajustaron correctamente.
    
MAPI_E_INVALID_PARAMETER
  
> Uno o ambos parámetros no eran válidos o se encontró un tipo de propiedad desconocido.
    
## <a name="remarks"></a>Comentarios

La **función ScRelocProps** funciona con la suposición de que la matriz de valores de propiedad para la que se ajustan los punteros se asignó originalmente en una sola llamada similar a una llamada a la **función ScCopyProps.** Si una aplicación cliente o un proveedor de servicios trabaja con un valor de propiedad creado a partir de bloques de memoria diferentes, debe usar [ScCopyProps](sccopyprops.md) para copiar propiedades en su lugar. 
  
 **ScRelocProps** se usa para mantener la validez de los punteros en una matriz [SPropValue.](spropvalue.md) Para mantener la validez de los punteros al escribir dicha matriz y leerla desde un disco, realice las siguientes operaciones: 
  
1. Antes de escribir la matriz y los datos en un disco, llama a **ScRelocProps** en la matriz con el  _parámetro pvBaseNew_ que apunta a algún valor estándar cero, por ejemplo. 
    
2. Después de leer la matriz y los datos de un disco, llama a **ScRelocProps** en la matriz con el parámetro  _pvBaseOld_ igual al mismo valor estándar usado en el paso 1. La matriz y los datos deben leerse en un búfer creado con una sola asignación. 
    
3. El  _parámetro pcb_ de **ScRelocProps** es opcional. 
    
## <a name="see-also"></a>Vea también



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ScCountProps](sccountprops.md)
  
[ScDupPropset](scduppropset.md)
  
[ScRelocNotifications](screlocnotifications.md)

