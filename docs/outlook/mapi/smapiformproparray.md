---
title: SMAPIFormPropArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormPropArray
api_type:
- COM
ms.assetid: bb243bc4-4974-4ad6-aa76-2426c1ebe84b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 50b6581dec8211968a49b204c6d9b1ba1c65bb62
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420069"
---
# <a name="smapiformproparray"></a>SMAPIFormPropArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz [de estructuras SMAPIFormProp.](smapiformprop.md) 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiform.h  <br/> |
|Macro relacionada:  <br/> |[CbMAPIFormPropArray](cbmapiformproparray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cProps;
  ULONG ulPad;
  SMAPIFormProp aFormProp[MAPI_DIM];
} SMAPIFormPropArray, FAR * LPMAPIFORMPROPARRAY;

```

## <a name="members"></a>Miembros

 **cProps**
  
> Recuento de propiedades con nombre en la matriz en el **miembro aFormProp.** 
    
 **ulPad**
  
>  Ocho bytes de espaciado interno usados para garantizar una alineación correcta. 
    
 **aFormProp**
  
> Matriz de propiedades de formulario.
    
## <a name="remarks"></a>Comentarios

La **estructura SMAPIFormPropArray** se pasa como parámetro a los métodos siguientes: 
  
- [IMAPIFormInfo::CalcFormPropSet](imapiforminfo-calcformpropset.md)
    
- [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
    
- [IMAPIFormContainer::CalcFormPropSet](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a>Consulte también



[CbMAPIFormPropArray](cbmapiformproparray.md)
  
[SMAPIFormProp](smapiformprop.md)


[Estructuras MAPI](mapi-structures.md)

