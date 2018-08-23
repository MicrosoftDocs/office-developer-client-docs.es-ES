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
ms.openlocfilehash: cf84c7d94e67da0ce7453829042e7be0d4e313f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585552"
---
# <a name="flatentry"></a>FLATENTRY

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una estructura de [ENTRYID](entryid.md) además de un recuento de bytes que especifica el tamaño de la estructura de la **propiedad ENTRYID** . 
  
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
  
> Recuento de bytes en el miembro **abEntry** . 
    
 **abEntry**
  
> El identificador de entrada completa que incluye la matriz de marcadores y datos binarios.
    
## <a name="remarks"></a>Comentarios

Una estructura **FLATENTRY** es similar a una estructura de [ENTRYID](entryid.md) . Sin embargo, hay algunas diferencias: 
  
- Una estructura **FLATENTRY** almacena el tamaño del identificador de entrada; **Propiedad ENTRYID** no lo hace. 
    
- Una estructura **FLATENTRY** almacena los datos de marca junto con el resto del identificador de entrada; **Propiedad ENTRYID** almacena por separado. 
    
- Una estructura **FLATENTRY** se usa para almacenar un identificador de entrada en un archivo o páselo en una secuencia de bytes, mientras que una estructura de la **propiedad ENTRYID** es utilizada por los métodos de interfaz [IMAPIProp](imapipropiunknown.md) y por los siguientes métodos de **OpenEntry** : [IABLogon: : OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)
    
- Una estructura **FLATENTRY** se usa para almacenar un identificador de entrada en un archivo o páselo en una secuencia de bytes. Una estructura de **ENTRYID** se usa para almacenar un identificador de entrada en el disco. 
    
## <a name="see-also"></a>Recursos adicionales



[ENTRYID](entryid.md)


[Estructuras MAPI](mapi-structures.md)

