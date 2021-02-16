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
ms.openlocfilehash: 418056f7222d5ab05f43a3661c1811bf2ae15be8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405117"
---
# <a name="imapiforminfomakeiconfrombinary"></a>IMAPIFormInfo::MakeIconFromBinary

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea un icono a partir de una de las propiedades de icono de un formulario.
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a>Parámetros

 _nPropID_
  
> [entrada] Identificador de propiedad de una propiedad de icono.
    
 _phicon_
  
> [salida] Puntero al icono devuelto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente llaman al **método IMAPIFormInfo::MakeIconFromBinary** para crear un icono a partir de una de las propiedades de icono de un formulario. En el  _parámetro nPropID,_ **MakeIconFromBinary** toma el identificador de propiedad de una de las propiedades de icono de un formulario. Con este identificador de propiedad, crea un icono que se puede mostrar en las vistas de tabla que incluyen columnas de propiedad para iconos. 
  
## <a name="see-also"></a>Consulte también



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

