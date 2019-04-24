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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360693"
---
# <a name="screlocprops"></a>ScRelocProps

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Ajusta los punteros en una matriz [SPropValue](spropvalue.md) después de que la matriz y sus datos se hayan copiado o movido a una nueva ubicación. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
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
  
> a Número de propiedades de la matriz señalada por el parámetro _rgprop_ . 
    
 _rgprop_
  
> a Puntero a una matriz de estructuras [SPropValue](spropvalue.md) para las que se van a ajustar los punteros. 
    
 _pvBaseOld_
  
> a Puntero a la dirección base original de la matriz señalada por el parámetro _rgprop_ . 
    
 _pvBaseNew_
  
> a Puntero a la nueva dirección base de la matriz señalada por el parámetro _rgprop_ . 
    
 _impreso_
  
> [in, out] Puntero opcional al tamaño, en bytes, de la matriz indicada por el parámetro _pvBaseNew_ . Si no es NULL, el parámetro _PCB_ se establece en el número de bytes almacenados en el parámetro _pvD_ . 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> Los punteros se ajustaron correctamente.
    
MAPI_E_INVALID_PARAMETER
  
> Uno o ambos parámetros no son válidos o se encontró un tipo de propiedad desconocido.
    
## <a name="remarks"></a>Comentarios

La función **ScRelocProps** se supone por el hecho de que la matriz de valores de propiedad para la que se ajustan los punteros se asignó originalmente en una sola llamada similar a una llamada a la función **ScCopyProps** . Si una aplicación cliente o un proveedor de servicios está trabajando con un valor de propiedad que se genera desde bloques de memoria inconexos, debe usar [ScCopyProps](sccopyprops.md) para copiar las propiedades en su lugar. 
  
 **ScRelocProps** se usa para mantener la validez de los punteros en una matriz [SPropValue](spropvalue.md) . Para mantener la validez de los punteros al escribir dicha matriz en un disco y leerlo, realice las operaciones siguientes: 
  
1. Antes de escribir la matriz y los datos en un disco, llame a **ScRelocProps** en la matriz con el parámetro _pvBaseNew_ que apunta a un valor cero estándar, por ejemplo. 
    
2. Después de leer la matriz y los datos de un disco, llame a **ScRelocProps** en la matriz con el parámetro _pvBaseOld_ igual al mismo valor estándar usado en el paso 1. La matriz y los datos deben leerse en un búfer creado con una única asignación. 
    
3. El parámetro _PCB_ para **ScRelocProps** es opcional. 
    
## <a name="see-also"></a>Vea también



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ScCountProps](sccountprops.md)
  
[ScDupPropset](scduppropset.md)
  
[ScRelocNotifications](screlocnotifications.md)

