---
title: IMessageModifyRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.ModifyRecipients
api_type:
- COM
ms.assetid: 2625f29d-325f-417d-bcec-49d580f9cd7e
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 07e1c2104068a6eb242e8ba81f91655edaa92cd8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426243"
---
# <a name="imessagemodifyrecipients"></a>IMessage::ModifyRecipients

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Agrega, elimina o modifica a los destinatarios del mensaje.
  
```cpp
HRESULT ModifyRecipients(
  ULONG ulFlags,
  LPADRLIST lpMods
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [entrada] M�scara de bits de indicadores que controla los cambios de destinatarios. Si se pasa cero para el par�metro  _ulFlags_, **ModifyRecipients** reemplaza a todos los destinatarios existentes con la lista de destinatarios que apunta el par�metro  _lpMods_. Pueden establecer los siguientes indicadores para  _ulFlags_:
    
MODRECIP_ADD 
  
> Los destinatarios que apunta el par�metro  _lpMods_ deben agregarse a la lista de destinatarios. 
    
MODRECIP_MODIFY 
  
> Los destinatarios que apunta el par�metro  _lpMods_ deben reemplazar a los destinatarios existentes. Todas las propiedades existentes se reemplazan por las de la estructura [ADRENTRY](adrentry.md) correspondiente. 
    
MODRECIP_REMOVE 
  
> Los destinatarios existentes deben quitarse de la lista de destinatarios utilizando como índice la propiedad **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) incluida en la matriz de valores de propiedad de cada entrada de destinatario en el parámetro _lpMods_ . 
    
 _lpMods_
  
> [entrada] Puntero a una estructura [ADRLIST](adrlist.md) que contiene una lista de destinatarios para agregar, eliminar o modificar en el mensaje. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La lista de destinatarios se modific� correctamente.
    
## <a name="remarks"></a>Comentarios

El m�todo **IMessage::ModifyRecipients** cambia la lista de destinatarios del mensaje. Es en esta lista, que se celebran en una estructura [ADRLIST](adrlist.md) , que se basa la tabla de destinatarios. 
  
La estructura **ADRLIST** contiene una estructura [ADRENTRY](adrentry.md) para cada destinatario y cada estructura **ADRENTRY** contiene una matriz de valores de propiedad que describe las propiedades del destinatario. 
  
Los destinatarios de la estructura **ADRLIST** se pueden resolver o sin resolver. La diferencia est� en el n�mero y tipo de propiedades que se incluyen. Un destinatario sin resolver contiene solo las propiedades **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) y **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)), mientras que un destinatario resuelto contiene esas dos propiedades más **PR_ADDRTYPE **([PidTagAddressType](pidtagaddresstype-canonical-property.md)) y **** [PidTagEntryId](pidtagentryid-canonical-property.md)(en inglés). Si **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) está disponible, también puede incluirse.
  
En el momento en que se env�a un mensaje, deben incluir s�lo los destinatarios resueltos en su lista de destinatarios. Destinatarios sin resolver dar lugar a informes de entrega que se crea y se env�a al remitente del mensaje original. Para obtener m�s informaci�n acerca del proceso de resoluci�n de nombres desde la perspectiva del cliente, vea la [resoluci�n de un nombre](resolving-a-recipient-name.md). Para obtener m�s informaci�n desde la perspectiva de la libreta de direcciones, vea [Implementaci�n de resoluci�n de nombres](implementing-name-resolution.md).
  
Adem�s de los destinatarios resueltos y no resueltos, un destinatario puede ser NULL. El miembro **cValues** de la estructura de **ADRENTRY** para el destinatario se establece en cero y el miembro **rgPropVals** se establece en NULL. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede crear una lista de destinatarios mediante una llamada a [IAddrBook::Address](imapisupport-address.md) para mostrar el cuadro de di�logo com�n y pedir al usuario que seleccione entradas. La lista de direcciones que apunta el par�metro  _lppAdrList_ a **Address** se pueden pasar a **ModifyRecipients** como el par�metro  _lpMods_. 
  
Al especificar las propiedades para un destinatario de la estructura [ADRLIST](adrlist.md) , incluye todas las propiedades del destinatario, no s�lo los nuevos o modificados. Cuando se modifica un destinatario, se eliminan todas las propiedades que no se incluyen en la estructura de **ADRLIST**. Para recuperar el conjunto actual de propiedades para todos los destinatarios de un mensaje, llame [GetRecipientTable](imessage-getrecipienttable.md) y recuperar todas las filas. Dado que es id�ntico en estructura a un **ADRLIST**un **SRowSet**, puede utilizar indistintamente ellos.
  
 **ModifyRecipients** reemplaza todas las entradas en la lista de destinatarios actual con la informaci�n que se�ala  _lpMods_ cuando ninguno de los indicadores se establecen en el par�metro  _ulFlags_. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando se establece la marca MODRECIP_MODIFY, **ModifyRecipients** reemplaza cada destinatario toda la fila con la fila asociada en la estructura [ADRLIST](adrlist.md) pasada en  _lpMods_. Tenga cuidado especificar todas las propiedades que debe tener un destinatario independientemente de si han cambiado para impedir que se va a eliminar accidentalmente.
  
A continuaci�n se muestran algunas reglas para establecer las propiedades de los destinatarios en la estructura de **ADRLIST**: 
  
- No use PT_NULL como un tipo de propiedad. **ModifyRecipients** devuelve un error al encontrar este valor. 
    
- No use PT_ERROR como un tipo de propiedad. **ModifyRecipients** pasa por alto este valor. 
    
- Incluir la propiedad **PR_ROWID** para todos los destinatarios cuando se establece la marca de la MODRECIP_REMOVE o MODRECIP_MODIFY en  _ulFlags_. 
    
- No incluya la propiedad **PR_ROWID** para cualquiera de los destinatarios cuando se establece la marca MODRECIP_ADD en  _ulFlags_ o cuando se pasa cero en  _ulFlags_.
    
Si se incluye la propiedad **PR_ADDRTYPE** o **PR_EMAIL_ADDRESS** (propiedad) para un destinatario y uno o ambos de estas propiedades no son coherentes con el tipo de direcci�n y la direcci�n del destinatario como identificado por **PR_ENTRYID**, los resultados se definen. Es decir, hay tres posibilidades, seg�n el proveedor de servicio:
  
- El mensaje se entregar� en la direcci�n descrita por las propiedades **PR_ADDRTYPE** y **PR_EMAIL_ADDRESS**. 
    
- El mensaje se entregar� al destinatario identificado por **PR_ENTRYID**.
    
- El mensaje se va a declarar no se puede entregar debido a la ambig�edad de la informaci�n de direcci�n.
    
Use las reglas de asignaci�n descritas en [Administraci�n de la memoria de ADRLIST y estructuras SRowSet](managing-memory-for-adrlist-and-srowset-structures.md) asignar memoria para la lista de destinatarios. **ModifyRecipients** no libere la estructura **ADRLIST** ni ninguna de sus subestructuras. La estructura de **ADRLIST** y cada estructura [SPropValue](spropvalue.md) deben asignarse por separado mediante el uso de la funci�n [MAPIAllocateBuffer](mapiallocatebuffer.md) tal que cada uno de ellos se puede liberar individualmente. Si el m�todo requiere espacio adicional para cualquier estructura **SPropValue**, puede reemplazar la estructura de **SPropValue** con una nueva que m�s adelante se puede liberar mediante [MAPIFreeBuffer](mapifreebuffer.md). La estructura **SPropValue** original tambi�n debe liberarse mediante **MAPIFreeBuffer**.
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIABFunctions. cpp  <br/> |AddRecipient  <br/> |MFCMAPI, utiliza el m�todo **IMessage::ModifyRecipients** para agregar a un nuevo destinatario a un mensaje.  <br/> |
   
## <a name="see-also"></a>Ver también



[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

