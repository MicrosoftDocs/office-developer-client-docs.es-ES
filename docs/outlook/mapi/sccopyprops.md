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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411011"
---
# <a name="sccopyprops"></a>ScCopyProps

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Copia las propiedades definidas por una matriz de [estructuras SPropValue](spropvalue.md) en un nuevo destino. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
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

## <a name="parameters"></a>Parámetros

 _cprop_
  
> [entrada] Número de propiedades que se van a copiar. 
    
 _rgprop_
  
> [entrada] Puntero a una matriz de [estructuras SPropValue](spropvalue.md) que definen las propiedades que se van a copiar. El  _parámetro rgprop_ no tiene que apuntar al principio de la matriz, pero debe apuntar al principio de una de las estructuras **SPropValue** de la matriz. 
    
 _pvDst_
  
> [entrada] Puntero a la posición inicial en la memoria en la que esta función copia las propiedades. 
    
 _indeste_
  
> [salida] Puntero opcional al tamaño, en bytes, del bloque de memoria al que apunta el _parámetro pvDst._ 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> Las propiedades se copiaron correctamente.
    
MAPI_E_INVALID_PARAMETER
  
> Se encontró un tipo de propiedad desconocido.
    
## <a name="remarks"></a>Comentarios

La nueva matriz y sus datos residen en un búfer creado con una única asignación, y la función [ScRelocProps](screlocprops.md) se puede usar para ajustar los punteros en las estructuras [SPropValue](spropvalue.md) individuales. Antes de este ajuste, los punteros son válidos. 
  
 **ScCopyProps** mantiene el orden de propiedad original de la matriz de propiedades copiada. 
  
El _parámetro pbc_ es opcional; si no es NULL, se establece en el número de bytes almacenados en el _parámetro pvDst._ 
  
## <a name="see-also"></a>Consulte también



[ScDupPropset](scduppropset.md)

