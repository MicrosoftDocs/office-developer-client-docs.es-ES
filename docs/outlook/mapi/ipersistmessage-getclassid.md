---
title: IPersistMessageGetClassID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetClassID
api_type:
- COM
ms.assetid: 77eeb468-3432-4ccd-9c1e-1df9ce605193
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3f0d98b8ffa13fe238fc0fcf8ff0ec76a3a284eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309628"
---
# <a name="ipersistmessagegetclassid"></a>IPersistMessage::GetClassID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve un identificador que representa el servidor de formularios que puede administrar el formulario. 
  
```cpp
HRESULT GetClassID(
  LPCLSID lpClassID
);
```

## <a name="parameters"></a>Parámetros

 _lpClassID_
  
> [entrada, salida] Puntero al identificador de clase (CLSID) del formulario.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El identificador de clase se devolvió correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IPersistMessge::GetClassID** establece el contenido del parámetro  _lpClassID_ en el identificador de clase del servidor de formulario y devuelve S_OK. Cuando un visor de formularios llama **a GetClassID** y devuelve correctamente, el formulario se coloca en el [estado Uninitialized.](uninitialized-state.md) 
  
Para obtener más información acerca de cómo se usan los identificadores de clase con objetos de almacenamiento estructurados, vea la documentación del método [IPersist::GetClassID.](https://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) 
  
## <a name="see-also"></a>Consulte también



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

