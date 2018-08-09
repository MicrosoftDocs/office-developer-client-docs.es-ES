---
title: IAddrBookAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Address
api_type:
- COM
ms.assetid: ef2112c7-35cd-4106-ad18-a45e1dbe07d6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 10f8f2cf44bf1a8e00f8c2b1a76826db5fc07161
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817118"
---
# <a name="iaddrbookaddress"></a>IAddrBook::Address

  
  
**Hace referencia a**: Outlook 
  
Muestra el cuadro de diálogo de la libreta de direcciones de Outlook. 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Parámetros

 _lpulUIParam_
  
> [entrada, salida] Un puntero a un identificador de la ventana principal del cuadro de diálogo. En la entrada, siempre se debe pasar un identificador de ventana. En la salida, si el miembro **ulFlags** del parámetro _lpAdrParms_ se establece en DIALOG_SDI, se devuelve el identificador de ventana del cuadro de diálogo no modal. Consulte Comentarios. 
    
 _lpAdrParms_
  
> [entrada, salida] Un puntero a una estructura [ADRPARM](adrparm.md) que controla la presentación y el comportamiento del cuadro de diálogo dirección. 
    
 _lppAdrList_
  
> [entrada, salida] Un puntero a un puntero a una estructura [ADRLIST](adrlist.md) que contiene la información del destinatario. En la entrada, este parámetro puede ser NULL o elija un puntero válido. En la salida, este parámetro señala a un puntero a la información de destinatario válido. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El cuadro de diálogo común de dirección se muestra correctamente.
    
## <a name="remarks"></a>Comentarios

Si el miembro **ulFlags** del parámetro _lpAdrParms_ se establece en DIALOG_SDI prever el retorno del identificador de ventana del cuadro de diálogo no modal de salida, se omite en Outlook; la versión del cuadro de diálogo modal siempre se muestra en los clientes de Outlook que no sean. 
  
La estructura **ADRLIST** pasada back MAPI al autor de la llamada a través del parámetro _lppAdrList_ contiene una matriz de estructuras [ADRENTRY](adrentry.md) , una estructura para cada destinatario. Cuando se pasa al método de [IMessage::ModifyRecipients](imessage-modifyrecipients.md) de un mensaje saliente en el parámetro _lpMods_ , la estructura **ADRLIST** puede utilizarse para actualizar su lista de destinatarios. 
  
Cada estructura **ADRENTRY** en la estructura **ADRLIST** contiene cero o más estructuras de [SPropValue](spropvalue.md) , una estructura para cada conjunto de propiedades para el destinatario. Puede haber cero estructuras **SPropValue** cuando el cuadro de diálogo presentado por el método de **dirección** se usa para quitar a un destinatario. Cuando hay una o más estructuras de **SPropValue** , la estructura **ADRENTRY** correspondiente se utiliza para agregar o actualizar a un destinatario. El destinatario puede ser resuelto, lo que indica que una de las estructuras de **SPropValue** describe la propiedad del destinatario **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)), o sin resolver, lo que indica que la propiedad de **entrada del objeto** es falta. 
  
Además de **entrada del objeto**resueltos destinatarios incluyen las siguientes propiedades:
  
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
Es posible que la estructura **ADRLIST** que el autor de la llamada que se pasa en un tamaño diferente de la estructura que se devuelve de MAPI. Si MAPI debe devolver una estructura **ADRLIST** más grande, libera la estructura original y asigna una nueva. Al asignar memoria para la estructura **ADRLIST** , asignar la memoria para cada estructura **SPropValue** por separado. Para obtener más información acerca de cómo asignar y liberar estructuras **ADRLIST** , vea [Administración de la memoria de ADRLIST y estructuras SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)
  
 **Dirección** se devuelve inmediatamente si la marca DIALOG_SDI se establece en el miembro **ulFlags** de la estructura **ADRPARM** en el parámetro _lpAdrParms_ . El indicador DIALOG_SDI se omite para los clientes de Outlook que no sean. Si se omite la DIALOG_SDI, se mostrará la versión del cuadro de diálogo modal y no se debe esperar un puntero a un identificador en _lpulUIParam_.
  
 **Dirección** admite cadenas de caracteres Unicode en la estructura **ADRPARM** si AB_UNICODEUI se especificó en el miembro **ulFlags** de **ADRPARM** en el parámetro _lpAdrParms_ , y admite las cadenas de caracteres Unicode en ** ADRLIST**. Las cadenas de Unicode se convierten en el formato de caracteres de varios bytes (MBCS) de la cadena antes de que se muestren en el cuadro de diálogo de la libreta de direcciones de Outlook.
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |OpenOtherUsersMailboxFromGal  <br/> |MFCMAPI utiliza el método de **dirección** para permitir al usuario seleccionar qué buzón para abrir.  <br/> |
   
## <a name="see-also"></a>Vea también



[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[ADRPARM](adrparm.md)
  
[FreePadrlist](freepadrlist.md)
  
[FreeProws](freeprows.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)
  
[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

