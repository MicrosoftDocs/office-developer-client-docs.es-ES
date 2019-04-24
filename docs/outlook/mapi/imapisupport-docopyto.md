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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331811"
---
# <a name="imapisupportdocopyto"></a>IMAPISupport::DoCopyTo

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Copia o mueve todas las propiedades de un objeto, excepto para las propiedades excluidas específicamente, a otro objeto.
  
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

## <a name="parameters"></a>Parameters

 _lpSrcInterface_
  
> a Puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso al objeto que tiene las propiedades que se van a copiar o mover.
    
 _lpSrcObj_
  
> a Un puntero al objeto que contiene las propiedades que se van a copiar o mover.
    
 _ciidExclude_
  
> a Número de interfaces que se van a excluir al copiar o mover propiedades.
    
 _rgiidExclude_
  
> a Matriz de identificadores de interfaz que indica las interfaces que no se deben usar cuando se copia o se mueve información complementaria al objeto de destino.
    
 _lpExcludeProps_
  
> a Un puntero a una matriz de etiquetas de propiedad que identifica las etiquetas de propiedad que se deben excluir de la operación de copia o movimiento. Pasar NULL en el parámetro _lpExcludeProps_ indica que todas las propiedades del objeto se deben copiar o mover. **** Encopyto devuelve MAPI_E_INVALID_PARAMETER cuando el miembro **cValues** de la estructura [SPropTagArray](sproptagarray.md) a la que apunta _lpExcludeProps_ se establece en 0. 
    
 _ulUIParam_
  
> a Identificador de la ventana primaria del indicador de progreso. 
    
 _lpProgress_
  
> a Un puntero a una implementación del indicador de progreso. Si se pasa NULL en el parámetro _lpProgress_ , MAPI proporciona la implementación del progreso. El parámetro _lpProgress_ se omite a menos que se establezca la marca MAPI_DIALOG en el parámetro _ulFlags_ . 
    
 _lpDestInterface_
  
> a Puntero al identificador de interfaz que representa la interfaz que se va a usar para obtener acceso al objeto que va a recibir las propiedades que se han copiado o movido.
    
 _lpDestObj_
  
> a Un puntero al objeto que va a recibir las propiedades que se han copiado o movido.
    
 _ulFlags_
  
> a Una máscara de máscara de marcadores que controla la operación de copiar o mover. Se pueden establecer los siguientes indicadores:
    
MAPI_DIALOG 
  
> Muestra un indicador de progreso. 
    
MAPI_MOVE 
  
> **** Encopyto debe realizar una operación de movimiento en lugar de una operación de copia. Cuando esta marca no está establecida, **** encopyto realiza una operación de copia. 
    
MAPI_NOREPLACE 
  
> Las propiedades existentes en el objeto de destino no se deben sobrescribir. Cuando este indicador no está establecido, **** adcopyto sobrescribe las propiedades existentes. 
    
 _lppProblems_
  
> contempla En la entrada, un puntero a un puntero a una estructura [SPropProblemArray](spropproblemarray.md) ; de lo contrario, NULL, que indica que no es necesario información del error. Si _lppProblems_ es un puntero válido en INPUT, **** encopyto devuelve información detallada sobre los errores al copiar una o más propiedades. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las propiedades se han copiado o movido correctamente.
    
MAPI_E_COLLISION 
  
> Una propiedad que se va a copiar o mover ya existe en el objeto de destino y se ha establecido la marca MAPI_NOREPLACE. 
    
MAPI_E_FOLDER_CYCLE 
  
> El objeto de origen contiene directa o indirectamente el objeto de destino. Es posible que se haya realizado un trabajo significativo antes de que se detectara esta condición, por lo que los objetos de origen y de destino podrían modificarse parcialmente. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> La interfaz identificada por el parámetro _lpSrcInterface_ no es compatible con el objeto al que apunta _lpSrcObj_o la interfaz identificada por el parámetro _lpDestInterface_ no es compatible con el objeto al que señala _lpDestObj _. 
    
MAPI_E_NO_ACCESS 
  
> Se intentó obtener acceso a un objeto para el que el autor de la llamada no tiene permisos suficientes. Este error se devuelve si el objeto de destino es el mismo que el objeto de origen.
    
MAPI_E_INVALID_PARAMETER 
  
> El parámetro _lpSrcInterface_ es NULL. 
    
Los valores siguientes se pueden devolver en la estructura **SPropProblemArray** , pero no como valores devueltos para percopyto. **** Estos errores se aplican a una sola propiedad.
  
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció la marca MAPI_UNICODE y enCopyto no admite Unicode, o bien no se estableció MAPI_UNICODE y enCopyto solo admite Unicode. **** **** 
    
MAPI_E_COMPUTED 
  
> La propiedad no la puede modificar el autor de la llamada porque es una propiedad de solo lectura, calculada por el propietario del objeto de destino. Este error no es grave; el autor de la llamada debe permitir que continúe la operación de copia.
    
MAPI_E_INVALID_TYPE 
  
> El tipo de propiedad no es válido.
    
MAPI_E_UNEXPECTED_TYPE 
  
> El tipo de propiedad no es el tipo que espera el autor de la llamada.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::D ocopyto** se implementa para los objetos de compatibilidad del proveedor de almacenamiento de mensajes. Los proveedores de almacenamiento de **** mensajes pueden llamar a percopyto para implementar el método [IMAPIProp:: CopyTo](imapiprop-copyto.md) para sus carpetas y mensajes. 
  
De forma predeterminada **** , adcopyto copia o mueve todas las propiedades de un objeto a otro objeto. Todos los subobjetos del objeto de origen se incluyen automáticamente en la operación y se copian o se mueven en su totalidad. 
  
Si alguna de las propiedades que se han copiado o movido ya existe en el objeto de destino, las propiedades existentes se sobrescriben con las nuevas propiedades, a menos que la marca MAPI_NOREPLACE se establezca en el parámetro _ulFlags_ . La información existente en el objeto de destino que no se sobrescribe permanece inalterada. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para excluir propiedades de la operación de copiar o mover, incluya sus etiquetas de propiedad en el parámetro _lpExcludeProps_ . Si se pasan los resultados de usar la macro [PROP_TAG](prop_tag.md) para crear una etiqueta de propiedad a partir de un identificador específico de la matriz de etiquetas de propiedades, se excluirán todas las propiedades con ese identificador. Por ejemplo, la siguiente entrada en la matriz de etiquetas de propiedad hace que se excluyan todas las propiedades con un identificador de 0x8002, independientemente del tipo: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
Para evitar copiar el tiempo de entrega de un mensaje cuando copia el mensaje en una carpeta diferente, especifique **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) en la etiqueta de exclusión de la etiqueta de propiedad. Para excluir la lista de destinatarios de un mensaje, agregue la propiedad **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) a la matriz de exclusión. Para excluir los datos adjuntos de un mensaje, agregue la propiedad **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) a la matriz.
  
De forma similar, para evitar copiar o mover una carpeta o tabla de contenido de una carpeta o un contenedor de libreta de direcciones, incluya **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) o **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) en la matriz de exclusión de etiquetas de propiedad.
  
Omite los errores de MAPI_E_COMPUTED devueltos en la estructura **SPropProblemArray** en el parámetro _lppProblems_ . 
  
El identificador de interfaz al que apunta _lpSrcInterface_ es normalmente el mismo que el identificador de interfaz al que apunta _lpDestInterface_ . 
  
Si se pasa un identificador de interfaz aceptable en _lpDestInterface_ pero un puntero no válido en _lpDestObj_, los resultados son imprevisibles. Lo más probable es que el proveedor falle. 
  
Por el contrario, si tiene constancia de información complementaria que no se debe copiar o mover, agregue los identificadores de interfaz para las interfaces que se van a excluir de la matriz pasada en el parámetro _rgiidExclude_ . Por ejemplo, si está copiando mensajes, pero no todos sus datos adjuntos de mensajes, pase IID_IMessage en la matriz _rgiidExclude_ . **** Encopyto ignora cualquier interfaz enumerada en _rgiidExclude_ que no reconoce. 
  
Cuando se usa el parámetro _rgiidExclude_ para excluir una interfaz, también se excluyen todas las interfaces derivadas de esa interfaz. Por ejemplo, excluir la interfaz [IMAPIContainer](imapicontainerimapiprop.md) hace que se excluyan los contenedores de libretas de direcciones o carpetas, en función del tipo de proveedor. No excluya [IMAPIProp](imapipropiunknown.md) o [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) porque hay tantas interfaces que se derivan de ellos. 
  
 **** Encopyto informa sobre errores globales que se aplican a la operación en su totalidad, así como errores individuales que se aplican a propiedades individuales. Estos errores individuales se colocan en una estructura **SPropProblemArray** . Puede suprimir los informes de errores en el nivel de propiedad pasando NULL, en lugar de un puntero válido, para el parámetro de estructura de matriz con problemas de propiedad. 
  
Si desea recibir información sobre los errores, pase un puntero de estructura **SPropProblemArray** válido en el parámetro _lppProblems_ . Cuando **** encopyto Devuelve S_OK, compruebe si hay posibles errores con propiedades individuales en la estructura. Cuando **** percopyto devuelve un error, no se devuelve información en la estructura **SPropProblemArray** . En su lugar, llame al método [IMAPISupport:: GetLastError](imapisupport-getlasterror.md) para recuperar información detallada del error. 
  
Si **** encopyto Devuelve S_OK, libere la estructura **SPropProblemArray** devuelta llamando a la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Si se produce un error global en **** la llamada a encopyto, no use ni libere la estructura **SPropProblemArray** . Los proveedores deben omitir el miembro _ulIndex_ en las estructuras **SPropProblemArray** deVueltas por alcopyto. ****
  
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

