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
ms.openlocfilehash: 750d8b8d50acb9cf7340e6553062412667398665
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820447"
---
# <a name="propcopymore"></a>PropCopyMore

  
  
**Hace referencia a**: Outlook 
  
Copia un valor de propiedad único desde una ubicación de origen a una ubicación de destino. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
SCODE PropCopyMore(
  LPSPropValue lpSPropValueDest,
  LPSPropValue lpSPropValueSrc,
  ALLOCATEMORE * lpfAllocMore,
  LPVOID lpvObject
);
```

## <a name="parameters"></a>Parámetros

 _lpSPropValueDest_
  
> [out] Puntero a la ubicación a la que esta función escribe una estructura de [SPropValue](spropvalue.md) define el valor de la propiedad copiados. 
    
 _lpSPropValueSrc_
  
> [entrada] Puntero a la estructura [SPropValue](spropvalue.md) que contiene el valor de la propiedad que se va a copiar. 
    
 _lpfAllocMore_
  
> [entrada] Puntero a la función [MAPIAllocateMore](mapiallocatemore.md) que se usará para asignar memoria adicional si la ubicación de destino no es lo suficientemente grande como para contener la propiedad que se va a copiar. 
    
 _lpvObject_
  
> [entrada] Puntero a un objeto para el que **MAPIAllocateMore** asignar espacio si es necesario. 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> El valor de propiedad único se ha copiado correctamente.
    
MAPI_E_NO_SUPPORT
  
> Se encontró un tipo de propiedad desconocido.
    
## <a name="remarks"></a>Comentarios

Una aplicación de cliente o un proveedor de servicios puede usar la función **PropCopyMore** para copiar una propiedad fuera de una tabla que se va a ser liberados para poder utilizarlo en otro lugar. 
  
 **PropCopyMore** no es necesario asignar memoria a menos que el valor de la propiedad copió es de un tipo, como PT_STRING8, que no cabe en una estructura [SPropValue](spropvalue.md) . Para estas propiedades de gran tamaño, la función asigna memoria mediante la función de [MAPIAllocateMore](mapiallocatemore.md) a la que se pasa un puntero en el parámetro _lpfAllocMore_ . 
  
Injudicious uso de memoria de fragmentos de **PropCopyMore** ; Considere la posibilidad de usar la función [ScCopyProps](sccopyprops.md) en su lugar. 
  

