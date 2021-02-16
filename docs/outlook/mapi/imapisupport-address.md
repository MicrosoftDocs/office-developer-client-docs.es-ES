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
ms.openlocfilehash: 7300c11d5835640fe308430c9bb08d40b397e47b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407322"
---
# <a name="imapisupportaddress"></a>IMAPISupport::Address

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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
  
> [entrada, salida] Puntero al controlador de la ventana primaria del cuadro de diálogo. En la entrada, siempre se debe pasar un controlador de ventana. En el resultado, si la marca DIALOG_SDI se establece en la estructura [ADRPARM](adrparm.md) a la que apunta el parámetro  _lpAdrParms,_ se devuelve el controlador de ventana del cuadro de diálogo no modelado. 
    
 _lpAdrParms_
  
> [entrada, salida] Puntero a una estructura **ADRPARM** que controla la presentación y el comportamiento del cuadro de diálogo de dirección. 
    
 _lppAdrList_
  
> [entrada, salida] Puntero a un puntero a una lista de direcciones. En la entrada, esta lista es la lista actual de destinatarios de un mensaje o NULL, si no existe dicha lista. En el resultado,  _lppAdrList_ apunta a una lista actualizada de destinatarios de mensajes. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El cuadro de diálogo de dirección se ha mostrado correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::Address** se implementa para objetos de compatibilidad del proveedor de libreta de direcciones. Los proveedores de libretas de direcciones llaman a **Address** para crear o actualizar una lista de destinatarios de mensajes. 
  
Cada destinatario se describe en una [estructura ADRENTRY](adrentry.md) que se incluye en la estructura [ADRLIST](adrlist.md) a la que apunta el parámetro _lppAdrList._ La **estructura ADRENTRY** contiene una matriz de valores de propiedad de destinatario, uno de los cuales es el tipo del destinatario, o **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). Esta **estructura ADRLIST** se puede pasar a un cliente para usarla como parámetro  _lpMods_ en una llamada a [IMessage::ModifyRecipients](imessage-modifyrecipients.md).
  
Cada destinatario de la estructura **ADRLIST** se puede resolver, lo que indica que uno de sus valores de propiedad es su propiedad **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) o no resuelto, lo que indica que falta la propiedad **PR_ENTRYID** . 
  
Además de **PR_ENTRYID**, los destinatarios resueltos incluyen las siguientes propiedades:
  
- **PR_RECIPIENT_TYPE**
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
Los destinatarios sin resolver normalmente incluyen solo **PR_DISPLAY_NAME** y **PR_RECIPIENT_TYPE**. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

La **estructura ADRLIST** que pasa el autor de la llamada puede tener un tamaño diferente de la estructura que devuelve MAPI. Cuando asigne memoria para la estructura **ADRLIST,** asigne la memoria para cada [estructura SPropValue por](spropvalue.md) separado. 
  
Use los punteros a las funciones de asignación de memoria MAPI pasadas a la [función ABProviderInit](abproviderinit.md) para asignar memoria. Asigne memoria con la [función MAPIAllocateBuffer](mapiallocatebuffer.md) para **ADRLIST** y cada estructura de valor de propiedad en las **estructuras ADRENTRY** en **ADRLIST**. 
  
Si **Address** debe devolver una estructura **ADRLIST** más grande, o si ha pasado NULL para  _lppAdrList_, **Address** libera la estructura original y asigna una nueva. **Address** también asigna estructuras de valor de propiedad adicionales en la estructura **ADRLIST** y libera las antiguas según corresponda. Para obtener más información acerca de cómo se administra la memoria para las **estructuras ADRLIST,** vea [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).
  
 **La** dirección devuelve inmediatamente si DIALOG_SDI marca se estableció en la estructura **ADRPARM** en el _parámetro lpAdrParms._ 
  
## <a name="see-also"></a>Consulte también



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


[Administración de memoria para estructuras ADRLIST y SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)

