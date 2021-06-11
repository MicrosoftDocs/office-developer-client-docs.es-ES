---
title: FLATENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATENTRY
api_type:
- COM
ms.assetid: 03e53e08-9113-4101-84c9-ccf6d43127f6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e47f4e0d1ab9ab3ecfd53932b8ef26440134c603
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407245"
---
# <a name="flatentry"></a>FLATENTRY

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una [estructura ENTRYID](entryid.md) más un recuento de bytes que especifica el tamaño de la **estructura ENTRYID.** 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Macros relacionadas:  <br/> |[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} FLATENTRY, FAR *LPFLATENTRY;

```

## <a name="members"></a>Members

 **cb**
  
> Recuento de bytes en el **miembro abEntry.** 
    
 **abEntry**
  
> El identificador de entrada completo que incluye la matriz de marcas y datos binarios.
    
## <a name="remarks"></a>Comentarios

Una **estructura FLATENTRY** es similar a una [estructura ENTRYID.](entryid.md) Sin embargo, hay algunas diferencias: 
  
- Una **estructura FLATENTRY** almacena el tamaño del identificador de entrada; **ENTRYID** no. 
    
- Una **estructura FLATENTRY** almacena los datos de la marca junto con el resto del identificador de entrada; **ENTRYID los** almacena por separado. 
    
- Una estructura **FLATENTRY** se usa para almacenar un identificador de entrada en un archivo o pasarlo en una secuencia de bytes, mientras que una estructura **ENTRYID** la usan los métodos de interfaz [IMAPIProp](imapipropiunknown.md) y los siguientes métodos **OpenEntry:** [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)
    
- Una **estructura FLATENTRY** se usa para almacenar un identificador de entrada en un archivo o pasarlo en una secuencia de bytes. Se **usa una estructura ENTRYID** para almacenar un identificador de entrada en el disco. 
    
## <a name="see-also"></a>Vea también



[ENTRYID](entryid.md)


[Estructuras MAPI](mapi-structures.md)

