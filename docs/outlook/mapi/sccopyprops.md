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
ms.openlocfilehash: 1afd922459be2ec4bbbd27a61fdf6fcb425548c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351334"
---
# <a name="sccopyprops"></a>ScCopyProps

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Copia las propiedades definidas por una matriz de estructuras [SPropValue](spropvalue.md) en un nuevo destino. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
SCODE ScCopyProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parameters

 _cprop_
  
> a Número de propiedades que se va a copiar. 
    
 _rgprop_
  
> a Puntero a una matriz de estructuras [SPropValue](spropvalue.md) que definen las propiedades que se van a copiar. El parámetro _rgprop_ no tiene que apuntar al principio de la matriz, pero debe apuntar al principio de una de las estructuras **SPropValue** de la matriz. 
    
 _pvDst_
  
> a Puntero a la posición inicial en la memoria a la que esta función copia las propiedades. 
    
 _impreso_
  
> contempla Puntero opcional al tamaño, en bytes, del bloque de memoria al que apunta el parámetro _pvDst_ . 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> Las propiedades se han copiado correctamente.
    
MAPI_E_INVALID_PARAMETER
  
> Se encontró un tipo de propiedad desconocido.
    
## <a name="remarks"></a>Comentarios

La nueva matriz y sus datos residen en un búfer creado con una única asignación, y la función [ScRelocProps](screlocprops.md) se puede usar para ajustar los punteros en las estructuras individuales de [SPropValue](spropvalue.md) . Antes de este ajuste, los punteros son válidos. 
  
 **ScCopyProps** mantiene el orden de propiedades original de la matriz de propiedades copiada. 
  
El parámetro _PCB_ es opcional; Si no es NULL, se establece en el número de bytes almacenados en el parámetro _pvDst_ . 
  
## <a name="see-also"></a>Vea también



[ScDupPropset](scduppropset.md)

