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
ms.openlocfilehash: c9d769e6a32fad22750a965debbbdce83e4de539
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586462"
---
# <a name="ipersistmessagegetclassid"></a>IPersistMessage::GetClassID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve un identificador que representa el servidor de formulario que puede administrar el formulario. 
  
```cpp
HRESULT GetClassID(
  LPCLSID lpClassID
);
```

## <a name="parameters"></a>Parámetros

 _lpClassID_
  
> [entrada, salida] Un puntero para el identificador de clase (CLSID) del formulario.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El identificador de clase se devolvió correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IPersistMessge::GetClassID** establece el contenido del parámetro _lpClassID_ al identificador de clase del servidor de formulario y devuelve S_OK. Cuando llama a un visor de formulario **GetClassID** y devuelve correctamente, el formulario se coloca en el estado de [Uninitialized](uninitialized-state.md) . 
  
Para obtener más información acerca de cómo se usan los identificadores de clase con objetos de almacenamiento estructurado, consulte la documentación para el método [IPersist:: GetClassID](http://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) . 
  
## <a name="see-also"></a>Recursos adicionales



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

