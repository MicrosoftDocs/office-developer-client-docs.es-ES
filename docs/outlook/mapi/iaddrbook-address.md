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
ms.openlocfilehash: c2546fc990169526361f2c452c50212123d8284d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407910"
---
# <a name="iaddrbookaddress"></a>IAddrBook::Address

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Muestra el Outlook de la libreta de direcciones. 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Parameters

 _lpulUIParam_
  
> [in, out] Puntero a un identificador de la ventana primaria del cuadro de diálogo. En la entrada, siempre se debe pasar un identificador de ventana. En el resultado, si el **miembro ulFlags** del parámetro  _lpAdrParms_ se establece en DIALOG_SDI, se devuelve el identificador de ventana del cuadro de diálogo modeless. Consulte Comentarios. 
    
 _lpAdrParms_
  
> [in, out] Puntero a una estructura [ADRPARM](adrparm.md) que controla la presentación y el comportamiento del cuadro de diálogo de dirección. 
    
 _lppAdrList_
  
> [in, out] Puntero a un puntero a una [estructura ADRLIST](adrlist.md) que contiene información de destinatarios. En la entrada, este parámetro puede ser NULL o apuntar a un puntero válido. En el resultado, este parámetro apunta a un puntero a la información de destinatario válida. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El cuadro de diálogo dirección común se mostró correctamente.
    
## <a name="remarks"></a>Comentarios

Si el **miembro ulFlags** del parámetro _lpAdrParms_ se establece en DIALOG_SDI anticipando el retorno del controlador de ventana del cuadro de diálogo modeless en la salida, se omite en Outlook; la versión modal del cuadro de diálogo siempre se muestra en clientes que no Outlook usuario. 
  
La **estructura ADRLIST** pasada por MAPI al autor de la llamada a través del parámetro  _lppAdrList_ contiene una matriz de estructuras [ADRENTRY,](adrentry.md) una estructura para cada destinatario. Cuando se pasa al método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) de un mensaje saliente en el parámetro  _lpMods,_ la estructura **ADRLIST** se puede usar para actualizar su lista de destinatarios. 
  
Cada **estructura ADRENTRY** de la estructura **ADRLIST** contiene cero o más estructuras [SPropValue,](spropvalue.md) una estructura para cada conjunto de propiedades para el destinatario. Puede haber cero **estructuras SPropValue** cuando se usa el cuadro de diálogo presentado por el **método Address** para quitar un destinatario. Cuando hay una o varias estructuras **SPropValue,** se usa la estructura **ADRENTRY** correspondiente para agregar o actualizar un destinatario. El destinatario puede resolverse, lo que indica que una de las estructuras **SPropValue** describe la propiedad PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) del destinatario, o no resuelto, lo que indica que falta la propiedad **PR_ENTRYID.**  
  
Además de **PR_ENTRYID**, los destinatarios resueltos incluyen las siguientes propiedades:
  
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
La **estructura ADRLIST** que pasa el autor de la llamada puede tener un tamaño diferente de la estructura que devuelve MAPI. Si MAPI debe devolver una estructura **ADRLIST** más grande, libera la estructura original y asigna una nueva. Al asignar memoria para la estructura **ADRLIST,** asigne la memoria para cada **estructura SPropValue por** separado. Para obtener más información sobre cómo asignar y liberar estructuras **ADRLIST,** vea [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md)
  
 **Address** devuelve inmediatamente si la marca DIALOG_SDI se establece en el **miembro ulFlags** de la estructura **ADRPARM** del parámetro _lpAdrParms._ La DIALOG_SDI se omite para clientes que no Outlook cliente. Si DIALOG_SDI se omite, se mostrará la versión modal del cuadro de diálogo y no se debe esperar un puntero a un identificador en  _lpulUIParam_.
  
 **Address** admite cadenas de caracteres Unicode en la estructura **ADRPARM** si AB_UNICODEUI se especificó en el **miembro ulFlags** de **ADRPARM** en el parámetro  _lpAdrParms_ y admite cadenas de caracteres Unicode en **ADRLIST**. Las cadenas Unicode se convierten al formato de cadena de caracteres multibyte (MBCS) antes de que se muestren en el cuadro de diálogo Outlook libreta de direcciones.
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |OpenOtherUsersMailboxFromGal  <br/> |MFCMAPI usa el **método Address** para permitir al usuario seleccionar el buzón que se va a abrir.  <br/> |
   
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


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

