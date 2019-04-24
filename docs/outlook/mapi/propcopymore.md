---
title: PropCopyMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PropCopyMore
api_type:
- HeaderDef
ms.assetid: 133d47cf-3592-44f3-8cdd-be402d160ee4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 827cdb919499a068f7932d8f1f7ec264ddc5b47c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328556"
---
# <a name="propcopymore"></a>PropCopyMore

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Copia un único valor de propiedad desde una ubicación de origen a una ubicación de destino. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
SCODE PropCopyMore(
  LPSPropValue lpSPropValueDest,
  LPSPropValue lpSPropValueSrc,
  ALLOCATEMORE * lpfAllocMore,
  LPVOID lpvObject
);
```

## <a name="parameters"></a>Parameters

 _lpSPropValueDest_
  
> contempla Puntero a la ubicación a la que esta función escribe una estructura [SPropValue](spropvalue.md) que define el valor de la propiedad copiada. 
    
 _lpSPropValueSrc_
  
> a Puntero a la estructura [SPropValue](spropvalue.md) que contiene el valor de la propiedad que se va a copiar. 
    
 _lpfAllocMore_
  
> a Puntero a la función [MAPIAllocateMore](mapiallocatemore.md) que se va a usar para asignar memoria adicional si la ubicación de destino no es lo suficientemente grande como para contener la propiedad que se va a copiar. 
    
 _lpvObject_
  
> a Puntero a un objeto para el que **MAPIAllocateMore** asignará espacio si es necesario. 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> El valor de la propiedad única se ha copiado correctamente.
    
MAPI_E_NO_SUPPORT
  
> Se encontró un tipo de propiedad desconocido.
    
## <a name="remarks"></a>Comentarios

Una aplicación cliente o un proveedor de servicios puede usar la función **PropCopyMore** para copiar una propiedad de una tabla que está a punto de liberarse para poder usarla en otro lugar. 
  
 **PropCopyMore** no necesita asignar memoria a menos que el valor de la propiedad copiado sea de un tipo, como PT_STRING8, que no quepa en una estructura [SPropValue](spropvalue.md) . Para estas propiedades de gran tamaño, la función asigna memoria mediante la función [MAPIAllocateMore](mapiallocatemore.md) a la que se pasa un puntero en el parámetro _lpfAllocMore_ . 
  
Uso inrazonable de la memoria de los fragmentos de **PropCopyMore** ; considere la posibilidad de usar la función [ScCopyProps](sccopyprops.md) en su lugar. 
  

