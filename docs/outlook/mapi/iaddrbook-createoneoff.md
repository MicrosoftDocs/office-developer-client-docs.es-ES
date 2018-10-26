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
ms.openlocfilehash: ddb87af4b14be6d728bcceddb4d958ba49229ad4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579042"
---
# <a name="iaddrbookcreateoneoff"></a>IAddrBook::CreateOneOff

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
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
  
> [entrada] Un puntero al valor de la propiedad del destinatario **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). El parámetro _lpszName_ puede ser NULL. 
    
 _lpszAdrType_
  
> [entrada] Un puntero para el tipo de dirección del destinatario, como FAX o SMTP. El parámetro _lpszAdrType_ no puede ser NULL. 
    
 _lpszAddress_
  
> [entrada] Un puntero a la dirección del destinatario. El parámetro _lpszAddress_ no puede ser NULL. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que influye en el destinatario de uso único. Se pueden establecer los siguientes indicadores:
    
MAPI_SEND_NO_RICH_INFO 
  
> El destinatario no puede controlar el contenido del mensaje con formato. Si se establece MAPI_SEND_NO_RICH_INFO, MAPI establece la propiedad del destinatario **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) en FALSE. Si MAPI_SEND_NO_RICH_INFO no está establecido, MAPI establece esta propiedad en TRUE, a menos que se interpreta la dirección del destinatario mensajería indicada por _lpszAddress_ para que sea una dirección de Internet. En este caso, MAPI establece **PR_SEND_RICH_INFO** en FALSE. 
    
MAPI_UNICODE 
  
> El nombre para mostrar, el tipo de dirección y la dirección están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., estas cadenas se encuentran en formato ANSI.
    
 _lpcbEntryID_
  
> [out] Un puntero para el número de bytes en el identificador de entrada indicado por el parámetro _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Un puntero a un puntero al identificador de entrada para el destinatario de uso único.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El identificador de entrada único se ha creado correctamente.
    
## <a name="remarks"></a>Comentarios

Los clientes llaman al método **CreateOneOff** para crear un identificador de entrada para un destinatario de uso único, un destinatario que no pertenezcan a cualquiera de los contenedores desde cualquiera de los proveedores de la libreta de direcciones cargada actualmente. Destinatarios de uso único pueden tener cualquier tipo de dirección que es compatible con uno de los proveedores de la libreta de direcciones activa para la sesión. 
  
Los destinatarios de este tipo normalmente se crean con una plantilla para su tipo de dirección concreto. El proveedor de libreta de direcciones que admite el tipo de dirección proporciona la plantilla. Un usuario de una aplicación cliente escribe la información relevante en la plantilla.
  
MAPI admite cadenas de caracteres Unicode para el nombre para mostrar, el tipo de dirección y los parámetros de la dirección de **CreateOneOff**.
  
El indicador MAPI_SEND_NO_RICH_INFO controla si el texto con formato en el formato de texto enriquecido (RTF) se envía junto con cada mensaje. El formato de transporte de encapsulación neutro (TNEF): un formato que se utiliza para transmitir con formato de texto, se envía por la mayoría de los proveedores de transporte, independientemente de cómo el destinatario establece su propiedad **PR_SEND_RICH_INFO** . No es un problema para los clientes que funcionan con mensajes interpersonales de mensajería. Sin embargo, debido a que TNEF normalmente se usa para enviar las propiedades personalizadas para las clases de mensaje personalizadas, no se admite puede ser un problema para los clientes basada en formularios o los clientes que requieren las propiedades personalizadas de MAPI. Para obtener más información, consulte [Envío de mensajes con TNEF](sending-messages-with-tnef.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|Mapiabfunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI usa el método **CreateOneOff** para crear un identificador de entrada para una dirección que no se encuentra en cualquier libreta de direcciones.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

