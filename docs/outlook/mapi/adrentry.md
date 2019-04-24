---
title: ADRENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRENTRY
api_type:
- COM
ms.assetid: 5fa091a4-3a84-4881-91b3-e34fd9ca6f38
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 36e0218c9e4e312a138bef7517242f74079212c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330229"
---
# <a name="adrentry"></a>ADRENTRY

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe cero o más propiedades que pertenecen a un destinatario.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _ADRENTRY
{
  ULONG ulReserved1;
  ULONG cValues;
  LPSPropValue rgPropVals;
} ADRENTRY, FAR *LPADRENTRY;

```

## <a name="members"></a>Members

 **ulReserved1**
  
> Reserve debe ser cero.
    
 **cValues**
  
> Número de propiedades de la matriz de valores de propiedad a la que señala el miembro **rgPropVals** . El miembro **cValues** puede ser cero. 
    
 **rgPropVals**
  
> Puntero a una matriz de valores de propiedad que describe las propiedades del destinatario. El miembro **rgPropVals** puede ser nulo. 
    
## <a name="remarks"></a>Comentarios

Una estructura **ADRENTRY** describe las propiedades que pertenecen a un único destinatario. Las propiedades que se suelen usar para describir a un destinatario son las siguientes: 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
  
 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
  
 **** Es ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
Cuando se muestra un identificador de **** entrada o una propiedad de la matriz de [SPropValue](spropvalue.md) para un destinatario, esto indica que se ha resuelto el destinatario. Los clientes llaman al método [IAddrBook:: ResolveName](iaddrbook-resolvename.md) para asegurarse de que se han resuelto todos los destinatarios de la lista de destinatarios de un mensaje saliente. Solo se pueden enviar con mensajes los destinatarios resueltos. 
  
 Las estructuras **ADRENTRY** suelen combinarse para formar una matriz para el miembro **aEntries** de una estructura [ADRLIST](adrlist.md) . 
  
 Las estructuras **ADRENTRY** y [SRow](srow.md) son idénticas porque contienen un miembro reservado, una matriz de valores de propiedad y un recuento de valores de la matriz. Mientras que las estructuras **ADRENTRY** se combinan para formar el miembro **aEntries** de una estructura **ADRLIST** , las estructuras **SRow** se combinan para formar el miembro **aRow** de una estructura [SRowSet](srowset.md) . Ambos tipos de estructuras siguen las mismas reglas de asignación, lo que implica que una estructura **SRowSet** que se recupera de la tabla de contenido de un contenedor de libretas de direcciones se puede convertir en una estructura **ADRLIST** y usar tal cual. 
  
Una estructura **ADRENTRY** puede estar vacía. Por ejemplo, una estructura **ADRENTRY** que está incluida en la estructura **ADRLIST** a la que apunta el parámetro _LppAdrList_ en una llamada a **IAddrBook:: Address** puede estar vacía cuando se quita un destinatario. 
  
Para obtener más información acerca de cómo asignar memoria para estructuras de **ADRENTRY** , consulte [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).
  
## <a name="see-also"></a>Vea también



[IAddrBook::Address](iaddrbook-address.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ADRLIST](adrlist.md)
  
[SRow](srow.md)
  
[SRowSet](srowset.md)


[Estructuras MAPI](mapi-structures.md)

