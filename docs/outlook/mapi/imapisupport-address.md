---
title: IMAPISupportAddress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Address
api_type:
- COM
ms.assetid: 8c22547e-ddf5-47f7-aed3-76e3854688df
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: cb683178a8e258f571cbc3d05a3b030481905433
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817476"
---
# <a name="imapisupportaddress"></a>IMAPISupport::Address

  
  
**Hace referencia a**: Outlook 
  
Muestra el cuadro de diálogo dirección común. 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Parámetros

 _lpulUIParam_
  
> [entrada, salida] Un puntero al controlador de la ventana principal del cuadro de diálogo. En la entrada, siempre se debe pasar un identificador de ventana. En la salida, si se establece la marca DIALOG_SDI en la estructura [ADRPARM](adrparm.md) indicada por el parámetro _lpAdrParms_ , se devuelve el identificador de ventana del cuadro de diálogo no modal. 
    
 _lpAdrParms_
  
> [entrada, salida] Un puntero a una estructura **ADRPARM** que controla la presentación y el comportamiento del cuadro de diálogo dirección. 
    
 _lppAdrList_
  
> [entrada, salida] Un puntero a un puntero a una lista de direcciones. En la entrada, esta lista es la lista actual de los destinatarios de un mensaje o NULL, si no existe ninguna dicha lista. En la salida, _lppAdrList_ apunta a una lista actualizada de los destinatarios del mensaje. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El cuadro de diálogo dirección se muestra correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::Address** se implementa para objetos de compatibilidad con de proveedor de la libreta de direcciones. Los proveedores de la libreta de direcciones, llame a **dirección** para crear o actualizar una lista de destinatarios del mensaje. 
  
Cada destinatario se describe en una estructura [ADRENTRY](adrentry.md) que se incluye en la estructura [ADRLIST](adrlist.md) indicada por el parámetro _lppAdrList_ . La estructura **ADRENTRY** contiene una matriz de valores de propiedades de los destinatarios, uno de los cuales es el destinatario tipo o propiedad de **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). Esta estructura **ADRLIST** se puede pasar a un cliente para usar como el parámetro _lpMods_ en una llamada a [IMessage::ModifyRecipients](imessage-modifyrecipients.md).
  
Cada destinatario de la estructura de **ADRLIST** puede ser ya sea resuelto, lo que indica que uno de sus valores de propiedad es de su propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)), o sin resolver, lo que indica que la propiedad de **entrada del objeto** es falta. 
  
Además de **entrada del objeto**resueltos destinatarios incluyen las siguientes propiedades:
  
- **PR_RECIPIENT_TYPE**
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
Destinatarios sin resolver suelen incluyen solo **PR_DISPLAY_NAME** y **PR_RECIPIENT_TYPE**. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Es posible que la estructura **ADRLIST** que el autor de la llamada que se pasa en un tamaño diferente de la estructura que se devuelve de MAPI. Al asignar memoria para la estructura **ADRLIST** , asignar la memoria para cada estructura [SPropValue](spropvalue.md) por separado. 
  
Use los punteros a las funciones de asignación de memoria MAPI que se pasó a la función [ABProviderInit](abproviderinit.md) para asignar memoria. Asignar memoria con la función [MAPIAllocateBuffer](mapiallocatebuffer.md) para cada estructura de valor de propiedad en las estructuras **ADRENTRY** en **ADRLIST**y **ADRLIST** . 
  
Si **dirección** debe devolver una estructura **ADRLIST** más grande, o si han transcurrido NULL para _lppAdrList_, **dirección** libera la estructura original y asigna una nueva. **Dirección** también asigna las estructuras de valor de propiedad adicional en la estructura **ADRLIST** y libera los antiguos según corresponda. Para obtener más información acerca de cómo se administra la memoria para las estructuras **ADRLIST** , vea [Administración de la memoria de ADRLIST y estructuras SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).
  
 **Dirección** se devuelve inmediatamente si se ha establecido el indicador DIALOG_SDI en la estructura **ADRPARM** en el parámetro _lpAdrParms_ . 
  
## <a name="see-also"></a>Vea también



[ABProviderInit](abproviderinit.md)
  
[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[ADRPARM](adrparm.md)
  
[FreePadrlist](freepadrlist.md)
  
[FreeProws](freeprows.md)
  
[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propiedad canónica PidTagAddressType](pidtagaddresstype-canonical-property.md)
  
[Propiedad canónica PidTagDisplayName](pidtagdisplayname-canonical-property.md)
  
[Propiedad canónica PidTagDisplayType](pidtagdisplaytype-canonical-property.md)
  
[Propiedad canónica PidTagEntryId](pidtagentryid-canonical-property.md)
  
[Propiedad canónica PidTagRecipientType](pidtagrecipienttype-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Administrar memoria para ADRLIST y estructuras SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)

