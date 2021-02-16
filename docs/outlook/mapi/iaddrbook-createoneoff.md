---
title: IAddrBookCreateOneOff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.CreateOneOff
api_type:
- COM
ms.assetid: bcacfbdf-edff-4810-a985-e6d2c9271901
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 980ac82c6f7fcb5771a6013b3fb033b0bdfd05e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427384"
---
# <a name="iaddrbookcreateoneoff"></a>IAddrBook::CreateOneOff

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea un identificador de entrada para una dirección de uso único.
  
```cpp
HRESULT CreateOneOff(
  LPSTR lpszName,
  LPSTR lpszAdrType,
  LPSTR lpszAddress,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parámetros

 _lpszName_
  
> [entrada] Puntero al valor de la propiedad PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) del destinatario. El  _parámetro lpszName_ puede ser NULL. 
    
 _lpszAdrType_
  
> [entrada] Puntero al tipo de dirección del destinatario, como FAX o SMTP. El  _parámetro lpszAdrType_ no puede ser NULL. 
    
 _lpszAddress_
  
> [entrada] Puntero a la dirección del destinatario. El  _parámetro lpszAddress_ no puede ser NULL. 
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que afecta al destinatario de uso único. Se pueden establecer las siguientes marcas:
    
MAPI_SEND_NO_RICH_INFO 
  
> El destinatario no puede controlar el contenido del mensaje con formato. Si MAPI_SEND_NO_RICH_INFO se establece, MAPI establece la propiedad PR_SEND_RICH_INFO **del** destinatario ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) en FALSE. Si MAPI_SEND_NO_RICH_INFO no se establece, MAPI establece esta propiedad en TRUE a menos que la dirección de mensajería del destinatario a la que apunta  _lpszAddress_ se interprete como una dirección de Internet. En este caso, MAPI establece **PR_SEND_RICH_INFO** en FALSE. 
    
MAPI_UNICODE 
  
> El nombre para mostrar, el tipo de dirección y la dirección están en formato Unicode. Si no MAPI_UNICODE marca, estas cadenas están en formato ANSI.
    
 _lpcbEntryID_
  
> [salida] Puntero al recuento de bytes en el identificador de entrada al que apunta el _parámetro lppEntryID._ 
    
 _lppEntryID_
  
> [salida] Puntero a un puntero al identificador de entrada del destinatario de uso único.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El identificador de entrada único se creó correctamente.
    
## <a name="remarks"></a>Comentarios

Los clientes llaman al **método CreateOneOff** para crear un identificador de entrada para un destinatario de uso único, un destinatario que no pertenece a ninguno de los contenedores de ninguno de los proveedores de libretas de direcciones cargados actualmente. Los destinatarios de uso único pueden tener cualquier tipo de dirección compatible con uno de los proveedores de libretas de direcciones activas para la sesión. 
  
Los destinatarios de uso único suelen crearse con una plantilla para su tipo de dirección particular. El proveedor de libreta de direcciones que admite el tipo de dirección proporciona la plantilla. Un usuario de una aplicación cliente escribe la información relevante en la plantilla.
  
MAPI admite cadenas de caracteres Unicode para el nombre para mostrar, el tipo de dirección y los parámetros de dirección **de CreateOneOff**.
  
La MAPI_SEND_NO_RICH_INFO marca controla si el texto con formato en formato de texto enriquecido (RTF) se envía junto con cada mensaje. La mayoría de los proveedores de transporte envían el formato de encapsulamiento neutro de transporte (TNEF), un formato que se usa para transmitir texto con formato, independientemente de cómo el destinatario establece su **propiedad PR_SEND_RICH_INFO** transporte. Esto no es un problema para los clientes de mensajería que trabajan con mensajes interpersonales. Sin embargo, dado que TNEF se usa normalmente para enviar propiedades personalizadas para clases de mensajes personalizadas, no admitirlo puede ser un problema para clientes basados en formularios o clientes que requieren propiedades MAPI personalizadas. Para obtener más información, vea [Enviar mensajes con TNEF](sending-messages-with-tnef.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|Mapiabfunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI usa el **método CreateOneOff** para crear un identificador de entrada para una dirección que no se encuentra en ninguna libreta de direcciones.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

