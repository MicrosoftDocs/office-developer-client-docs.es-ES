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
  
Muestra el cuadro de diálogo Dirección común. 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Parameters

 _lpulUIParam_
  
> [in, out] Puntero al controlador de la ventana principal del cuadro de diálogo. En la entrada, siempre debe pasarse un identificador de ventana. En la salida, si la marca DIALOG_SDI se establece en la estructura [ADRPARM](adrparm.md) apuntada por el parámetro _lpAdrParms_ , se devuelve el identificador de ventana del cuadro de diálogo no modal. 
    
 _lpAdrParms_
  
> [in, out] Un puntero a una estructura **ADRPARM** que controla la presentación y el comportamiento del cuadro de diálogo Dirección. 
    
 _lppAdrList_
  
> [in, out] Un puntero a un puntero a una lista de direcciones. En la entrada, esta lista es la lista actual de destinatarios de un mensaje o NULL, si no existe dicha lista. En la salida, _lppAdrList_ apunta a una lista actualizada de destinatarios del mensaje. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El cuadro de diálogo de la dirección se mostró correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport:: Address** se implementa para los objetos de compatibilidad del proveedor de la libreta de direcciones. Los proveedores de la libreta de direcciones llaman a la **Dirección** para crear o actualizar una lista de destinatarios del mensaje. 
  
Cada destinatario se describe en una estructura [ADRENTRY](adrentry.md) que se incluye en la estructura [ADRLIST](adrlist.md) a la que apunta el parámetro _lppAdrList_ . La estructura **ADRENTRY** contiene una matriz de valores de propiedad de destinatario, uno de los cuales es el tipo de destinatario o la propiedad **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). Esta estructura de **ADRLIST** se puede pasar a un cliente para usarla como el parámetro _lpMods_ en una llamada a [IMessage:: ModifyRecipients](imessage-modifyrecipients.md).
  
Cada uno de los destinatarios de la estructura **ADRLIST** se puede resolver, lo que indica que uno de sus **** valores de propiedad es su propiedad tipo ([PidTagEntryId](pidtagentryid-canonical-property.md)) o sin resolver, lo **** que indica que la propiedad 1 es ausencia. 
  
Además de la ****, los destinatarios resueltos incluyen las siguientes propiedades:
  
- **PR_RECIPIENT_TYPE**
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
Normalmente, los destinatarios sin resolver solo incluyen **PR_DISPLAY_NAME** y **PR_RECIPIENT_TYPE**. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

La estructura **ADRLIST** que pasa el autor de la llamada puede tener un tamaño diferente al de la estructura que devuelve MAPI. Cuando asigne memoria para la estructura **ADRLIST** , asigne la memoria para cada estructura [SPropValue](spropvalue.md) por separado. 
  
Use los punteros a las funciones de asignación de memoria MAPI que se pasan a la función [ABProviderInit](abproviderinit.md) para asignar memoria. Asigne memoria con la función [MAPIAllocateBuffer](mapiallocatebuffer.md) para **ADRLIST** y cada estructura de valor de propiedad en las estructuras **ADRENTRY** en **ADRLIST**. 
  
Si la **Dirección** debe devolver una estructura **ADRLIST** mayor o si ha pasado null para _lppAdrList_, **Address** libera la estructura original y asigna una nueva. **Address** también asigna estructuras de valores de propiedad adicionales en la estructura **ADRLIST** y libera los antiguos según corresponda. Para obtener más información acerca de cómo se administra la memoria para las estructuras de **ADRLIST** , consulte [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).
  
 La **Dirección** vuelve inmediatamente si la marca DIALOG_SDI se ha establecido en la estructura **ADRPARM** en el parámetro _lpAdrParms_ . 
  
## <a name="see-also"></a>Ver también



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


[Administración de la memoria para las estructuras ADRLIST y SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)

