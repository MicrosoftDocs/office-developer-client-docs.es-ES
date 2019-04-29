---
title: IID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IID
api_type:
- COM
ms.assetid: fa5498ab-2f8a-42f8-ba9d-1d555768594f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5605de7dbcc18197748713bcf909839690d7259f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411599"
---
# <a name="iid"></a>IID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una estructura de [GUID](guid.md) que se usa para describir un identificador de una interfaz MAPI. 
  
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a>Members

Consulte la estructura **GUID** . 
  
## <a name="remarks"></a>Comentarios

Una estructura de **IID** se usa para identificar de forma exclusiva una interfaz MAPI y para asociar una interfaz determinada con un objeto. Por ejemplo, cuando un cliente llama a [IMAPISession:: OpenEntry](imapisession-openentry.md) para abrir una carpeta, el cliente establece el parámetro _lpInterface_ para que apunte a un **IID** que representa la interfaz [IMAPIFolder](imapifolderimapicontainer.md) . MAPI define la **IMAPIFolderIID** para que sea IID_IMAPIFolder. Las estructuras **IID** también se usan para identificar de forma exclusiva las interfaces OLE. 
  
Todas las estructuras de **IID** específicas de las interfaces MAPI se definen en el archivo de encabezado Mapiguid. h. 
  
## <a name="see-also"></a>Ver también



[GUID](guid.md)


[Estructuras MAPI](mapi-structures.md)

