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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: d907f2e8ecb9b6126898ff35b13427b088af9561
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820710"
---
# <a name="smapiformproparray"></a>SMAPIFormPropArray

  
  
**Se aplica a**: Outlook 
  
Contiene una matriz de estructuras [SMAPIFormProp](smapiformprop.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIForm.h  <br/> |
|Macro relacionado:  <br/> |[CbMAPIFormPropArray](cbmapiformproparray.md) <br/> |
   
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
  
> Recuento de propiedades con nombre en la matriz en el miembro **aFormProp** . 
    
 **ulPad**
  
>  Ocho bytes de relleno utilizado para garantizar la alineación correcta. 
    
 **aFormProp**
  
> Matriz de las propiedades del formulario.
    
## <a name="remarks"></a>Notas

La estructura **SMAPIFormPropArray** se pasa como parámetro a los métodos siguientes: 
  
- [IMAPIFormInfo::CalcFormPropSet](imapiforminfo-calcformpropset.md)
    
- [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
    
- [IMAPIFormContainer::CalcFormPropSet](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a>Ver también



[CbMAPIFormPropArray](cbmapiformproparray.md)
  
[SMAPIFormProp](smapiformprop.md)


[Estructuras MAPI](mapi-structures.md)

