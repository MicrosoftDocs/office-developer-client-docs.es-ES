---
title: IMAPIFormInfoMakeIconFromBinary
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.MakeIconFromBinary
api_type:
- COM
ms.assetid: 4daeddd7-3f0c-4178-ae8d-f74814090d40
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a230e8b69a64646dffb23147345d5960fdd38581
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817296"
---
# <a name="imapiforminfomakeiconfrombinary"></a>IMAPIFormInfo::MakeIconFromBinary

  
  
**Hace referencia a**: Outlook 
  
Se basa en un icono de una de las propiedades del icono de un formulario.
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a>Parámetros

 _nPropID_
  
> [entrada] Un identificador de propiedad para una propiedad de icono.
    
 _phicon_
  
> [out] Un puntero al icono devuelto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente de llaman al método **IMAPIFormInfo::MakeIconFromBinary** para crear un icono de una de las propiedades del icono de un formulario. En el parámetro _nPropID_ , **MakeIconFromBinary** toma el identificador de propiedad de una de las propiedades del icono de un formulario. Con este identificador de propiedad, que basa un icono que se puede mostrar en las vistas de tabla que incluyen columnas de propiedad para los iconos. 
  
## <a name="see-also"></a>Vea también



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

