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
ms.openlocfilehash: a0e859ac0f8bcc3bd83e336c85da21f1251efcb5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817188"
---
# <a name="iid"></a>IID

  
  
**Hace referencia a**: Outlook 
  
Describe una estructura [GUID](guid.md) que se usa para describir un identificador para una interfaz de MAPI. 
  
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

Ver la estructura **GUID** . 
  
## <a name="remarks"></a>Comentarios

Una estructura de **IID** se usa para identificar de forma exclusiva una interfaz de MAPI y para asociar una interfaz determinada a un objeto. Por ejemplo, cuando un cliente llama a [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir una carpeta, el cliente establece el parámetro _lpInterface_ para que apunte a un **IID** que representa la interfaz [IMAPIFolder](imapifolderimapicontainer.md) . MAPI define la **IMAPIFolderIID** para que sea IID_IMAPIFolder. **IID** estructuras también se usan para identificar de forma exclusiva interfaces OLE. 
  
Todas las estructuras **IID** específicas para las interfaces MAPI se definen en el archivo de encabezado Mapiguid.h. 
  
## <a name="see-also"></a>Vea también



[GUID](guid.md)


[Estructuras MAPI](mapi-structures.md)

