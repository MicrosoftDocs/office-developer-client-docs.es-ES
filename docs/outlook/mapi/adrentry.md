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
ms.openlocfilehash: 4b6f850c8f88088863b37bd94de6b1f3d4c48d4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19816423"
---
# <a name="adrentry"></a>ADRENTRY

  
  
**Hace referencia a**: Outlook 
  
Se describen cero o más propiedades que pertenecen a un destinatario.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
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
  
> Reservado; debe ser cero.
    
 **cValues**
  
> Recuento de propiedades de la matriz de valores de propiedad que señala el miembro **rgPropVals** . El miembro **cValues** puede ser cero. 
    
 **rgPropVals**
  
> Puntero a una matriz de valores de propiedad que describe las propiedades para el destinatario. El miembro **rgPropVals** puede ser NULL. 
    
## <a name="remarks"></a>Comentarios

Una estructura de **ADRENTRY** describe las propiedades que pertenecen a un solo destinatario. Las propiedades que se usan normalmente para describir a un destinatario incluyen lo siguiente: 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
  
 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
  
 **Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
Cuando una propiedad de **entrada del objeto** o el identificador de entrada aparece en la matriz [SPropValue](spropvalue.md) para un destinatario, esto indica que el destinatario se ha resuelto. Los clientes de llaman al método [IAddrBook::ResolveName](iaddrbook-resolvename.md) para asegurarse de que se han resueltos todos los destinatarios en la lista de destinatarios de un mensaje saliente. Destinatarios resueltos sólo se pueden enviar con los mensajes. 
  
 Estructuras **ADRENTRY** normalmente se combinan para formar una matriz para el miembro **aEntries** de una estructura [ADRLIST](adrlist.md) . 
  
 Estructuras **ADRENTRY** y estructuras [SRow](srow.md) son idénticas porque ambos contienen un miembro reservado, una matriz de valores de propiedad y un recuento de valores de la matriz. Mientras que las estructuras **ADRENTRY** se combinan para formar al miembro **aEntries** de una estructura **ADRLIST** , **SRow** estructuras se combinan para formar al miembro **aRow** de una estructura de [SRowSet](srowset.md) . Ambos tipos de estructuras siguen las mismas reglas de asignación, lo que implica que se puede convertir en una estructura de **ADRLIST** y utilizada como es una estructura **SRowSet** que se recupera de la tabla de contenido de un contenedor de la libreta de direcciones. 
  
Una estructura de **ADRENTRY** puede estar vacía. Por ejemplo, una estructura **ADRENTRY** que se encuentra en la estructura **ADRLIST** indicada por el parámetro _lppAdrList_ en una llamada a **IAddrBook::Address** puede estar vacía cuando se está eliminando un destinatario. 
  
Para obtener más información acerca de cómo asignar memoria para las estructuras **ADRENTRY** , vea [Administración de la memoria de ADRLIST y estructuras SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).
  
## <a name="see-also"></a>Vea también



[IAddrBook::Address](iaddrbook-address.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ADRLIST](adrlist.md)
  
[SRow](srow.md)
  
[SRowSet](srowset.md)


[Estructuras MAPI](mapi-structures.md)

