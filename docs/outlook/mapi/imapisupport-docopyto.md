---
title: IMAPISupportDoCopyTo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyTo
api_type:
- COM
ms.assetid: 84019475-5176-4fc5-a3ee-871095077498
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6f6c802f1d5ead1750c05fafc54533487fe3732a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390635"
---
# <a name="imapisupportdocopyto"></a>IMAPISupport::DoCopyTo

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Copia o mueve todas las propiedades de un objeto, excepto propiedades excluidas específicamente, a otro objeto.
  
```cpp
HRESULT DoCopyTo(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  ULONG ciidExclude,
  LPCIID rgiidExclude,
  LPSPropTagArray lpExcludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpDestInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parámetros

 _lpSrcInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al objeto que tiene las propiedades que se pueden copiar o mover.
    
 _lpSrcObj_
  
> [entrada] Un puntero al objeto que tiene las propiedades que se pueden copiar o mover.
    
 _ciidExclude_
  
> [entrada] El recuento de interfaces que se deben excluir al copiar o mover las propiedades.
    
 _rgiidExclude_
  
> [entrada] Una matriz de identificadores de interfaz que indica las interfaces que no se deben usar cuando se copie o mueva información complementaria para el objeto de destino.
    
 _lpExcludeProps_
  
> [entrada] Un puntero a una matriz de etiqueta de propiedad que identifica las etiquetas de propiedad que se deben excluir de la copia o la operación de movimiento. Pasar NULL en el parámetro _lpExcludeProps_ indica que todas las propiedades del objeto deben copiar o mover. **DoCopyTo** devuelve MAPI_E_INVALID_PARAMETER cuando el miembro **cValues** de la estructura del [elemento SPropTagArray](sproptagarray.md) que apunta _lpExcludeProps_ se establece en 0. 
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal del indicador de progreso. 
    
 _lpProgress_
  
> [entrada] Un puntero a una implementación de indicador de progreso. Si se pasa NULL en el parámetro _lpProgress_ , MAPI proporciona la implementación de progreso. El parámetro _lpProgress_ se omite a menos que la marca MAPI_DIALOG se establece en el parámetro _ulFlags indicado_ . 
    
 _lpDestInterface_
  
> [entrada] Un puntero para el identificador de interfaz que representa la interfaz que se usará para tener acceso al objeto para recibir las propiedades que se ha movido o copiadas.
    
 _lpDestObj_
  
> [entrada] Un puntero al objeto que se va a recibir las propiedades que se ha movido o copiadas.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla la operación de copiar o mover. Se pueden establecer los siguientes indicadores:
    
MAPI_DIALOG 
  
> Muestra un indicador de progreso. 
    
MAPI_MOVE 
  
> **DoCopyTo** debe realizar una operación de movimiento en lugar de una operación de copia. Cuando no se establece este marcador, **DoCopyTo** realiza una operación de copia. 
    
MAPI_NOREPLACE 
  
> No se deben sobrescribir las propiedades existentes en el objeto de destino. Cuando no se establece este marcador, **DoCopyTo** sobrescribe las propiedades existentes. 
    
 _lppProblems_
  
> [out] En la entrada, un puntero a un puntero a una estructura [SPropProblemArray](spropproblemarray.md) ; de lo contrario, NULL, que indica que no hay necesidad de información de error. Si _lppProblems_ es un puntero válido en la entrada, **DoCopyTo** devuelve información detallada acerca de los errores de copiar una o más propiedades. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las propiedades se hayan copiado o movido correctamente.
    
MAPI_E_COLLISION 
  
> Una propiedad para ser copiado o movido ya existe en el objeto de destino y se establece la marca MAPI_NOREPLACE. 
    
MAPI_E_FOLDER_CYCLE 
  
> El objeto de origen, directa o indirectamente contiene el objeto de destino. Trabajo significativo es posible que se han realizado antes de que se ha detectado esta condición, por lo que los objetos de origen y de destino podrían modificarse parcialmente. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> La interfaz identificada mediante el parámetro _lpSrcInterface_ no es compatible con el objeto al que señala por _lpSrcObj_o la interfaz identificada mediante el parámetro _lpDestInterface_ no es compatible con el objeto al que señala por _lpDestObj _. 
    
MAPI_E_NO_ACCESS 
  
> Se ha intentado tener acceso a un objeto para el que el autor de la llamada no tiene permisos suficientes. Este error se devuelve si el objeto de destino es el mismo que el objeto de origen.
    
MAPI_E_INVALID_PARAMETER 
  
> El parámetro _lpSrcInterface_ es NULL. 
    
Los siguientes valores se pueden devolver en la estructura de **SPropProblemArray** , pero no como valores devueltos por **DoCopyTo**. Estos errores se aplican a una sola propiedad.
  
MAPI_E_BAD_CHARWIDTH 
  
> Se ha establecido el indicador MAPI_UNICODE y **DoCopyTo** no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y **DoCopyTo** admite sólo Unicode. 
    
MAPI_E_COMPUTED 
  
> La propiedad no puede modificarse el autor de la llamada porque es una propiedad de solo lectura, calculada por el propietario del objeto de destino. Este error no es grave; el autor de la llamada debe permitir que la operación de copia continuar.
    
MAPI_E_INVALID_TYPE 
  
> El tipo de propiedad no es válido.
    
MAPI_E_UNEXPECTED_TYPE 
  
> El tipo de propiedad no es el tipo esperado por el autor de la llamada.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::DoCopyTo** se implementa para objetos de soporte técnico de proveedor de almacén de mensajes. Los proveedores de almacén de mensajes pueden llamar a **DoCopyTo** para implementar el método [IMAPIProp::CopyTo](imapiprop-copyto.md) para sus carpetas y mensajes. 
  
De forma predeterminada, **DoCopyTo** copia o mueve todas las propiedades de un objeto a otro objeto. Los objetos secundarios en el objeto de origen automáticamente se incluyen en la operación y copiados o movidos en su totalidad. 
  
Si cualquiera de las propiedades que se ha movido o copiadas ya existe en el objeto de destino, se sobrescriben las propiedades existentes por las nuevas propiedades, a menos que se establece la marca MAPI_NOREPLACE en el parámetro _ulFlags indicado_ . Información existente en el objeto de destino que no se sobrescribe se toca. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para excluir las propiedades de la copia o la operación de movimiento, incluir sus etiquetas de propiedad en el parámetro _lpExcludeProps_ . Si pasa los resultados del uso de la macro [PROP_TAG](prop_tag.md) para crear una etiqueta de propiedad de un identificador específico de la matriz de la etiqueta de propiedad, se excluirán todas las propiedades con ese identificador. Por ejemplo, la siguiente entrada en la matriz de la etiqueta de propiedad hace que todas las propiedades con un identificador de 0x8002 que se deben excluir, independientemente del tipo de: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
Para evitar el tiempo de entrega de un mensaje cuando se copia el mensaje a una carpeta diferente de copia, especifique **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) en la matriz de exclusión de etiqueta de propiedad. Para excluir lista de destinatarios de un mensaje, agregue la propiedad **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) a la matriz de exclusión. Para excluir los datos adjuntos de un mensaje, agregue la propiedad **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) a la matriz.
  
De forma similar, para evitar que las acciones como copiar o mover de una carpeta o la jerarquía del contenedor de la libreta de direcciones o la tabla de contenido, incluya **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) o **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) en la propiedad etiqueta excluir matriz.
  
Omitir MAPI_E_COMPUTED devuelven errores en la estructura de **SPropProblemArray** en el parámetro _lppProblems_ . 
  
El identificador de interfaz que _lpSrcInterface_ puntos que suele ser el mismo que el identificador de interfaz que señala _lpDestInterface_ . 
  
Si se pasan un identificador de interfaz aceptable en _lpDestInterface_ pero un puntero no válido en _lpDestObj_, los resultados serán impredecibles. Es muy probable que esto hará que el proveedor se lleve a cabo. 
  
Por el contrario, si tiene constancia de información complementaria que no se puede copiar o mover, agregar los identificadores de interfaz de las interfaces que se deben excluir de la matriz que se pasa en el parámetro _rgiidExclude_ . Por ejemplo, si va a copiar los mensajes, pero no en cualquiera de sus datos adjuntos de mensajes, pase IID_IMessage en la matriz _rgiidExclude_ . **DoCopyTo** pasa por alto cualquier interfaces que aparecen en _rgiidExclude_ que no reconoce. 
  
Cuando se usa el parámetro _rgiidExclude_ para excluir una interfaz, también excluye todas las interfaces derivadas de dicha interfaz. Por ejemplo, la exclusión de la interfaz de [IMAPIContainer](imapicontainerimapiprop.md) hace que las carpetas o los contenedores de la libreta de direcciones que se deben excluir, según el tipo de proveedor de. No excluya [IMAPIProp](imapipropiunknown.md) o [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) debido a que muchas interfaces derivan de ellos. 
  
 **DoCopyTo** informes de errores global que se aplican a la operación como un todo y errores individuales que se aplican a las propiedades individuales. Estos errores individuales se colocan en una estructura **SPropProblemArray** . Puede suprimir informes en el nivel de propiedad pasando NULL, en lugar de un puntero válido para el parámetro de estructura de matriz de propiedad problema de error. 
  
Si desea recibir información acerca de los errores, pase un puntero de estructura **SPropProblemArray** válido en el parámetro _lppProblems_ . Cuando **DoCopyTo** devuelve S_OK, comprobar los posibles errores con las propiedades individuales de la estructura de. Cuando **DoCopyTo** devuelve un error, no se devuelve información de la estructura de **SPropProblemArray** . En su lugar, llame al método de [IMAPISupport::GetLastError](imapisupport-getlasterror.md) para recuperar información detallada del error. 
  
Si **DoCopyTo** devuelve S_OK, liberar la estructura **SPropProblemArray** devuelta por una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Si se produce un error global en la llamada **DoCopyTo** , no utilice ni libre la estructura **SPropProblemArray** . Proveedores de deben omitir al miembro _ulIndex_ en estructuras **SPropProblemArray** devuelto por **DoCopyTo**.
  
## <a name="see-also"></a>Vea también



[IMAPIProp::CopyTo](imapiprop-copyto.md)
  
[IMAPISupport::CopyFolder](imapisupport-copyfolder.md)
  
[IMAPISupport::CopyMessages](imapisupport-copymessages.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[Propiedad canónica PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[Propiedad canónica PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[Propiedad canónica PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)
  
[Propiedad canónica PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)
  
[Propiedad canónica PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

