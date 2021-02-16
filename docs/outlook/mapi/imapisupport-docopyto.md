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
  
Copia o mueve todas las propiedades de un objeto, excepto las propiedades excluidas específicamente, a otro objeto.
  
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
  
> [entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para tener acceso al objeto que tiene las propiedades que se van a copiar o mover.
    
 _lpSrcObj_
  
> [entrada] Puntero al objeto que tiene las propiedades que se van a copiar o mover.
    
 _ciidExclude_
  
> [entrada] Recuento de interfaces que se excluirán al copiar o mover propiedades.
    
 _rgiidExclude_
  
> [entrada] Matriz de identificadores de interfaz que indica interfaces que no deben usarse al copiar o mover información complementaria al objeto de destino.
    
 _lpExcludeProps_
  
> [entrada] Puntero a una matriz de etiquetas de propiedades que identifica las etiquetas de propiedad que se deben excluir de la operación de copia o movimiento. Pasar NULL en  _el parámetro lpExcludeProps_ indica que todas las propiedades del objeto deben copiarse o moverse. **DoCopyTo** devuelve MAPI_E_INVALID_PARAMETER cuando el miembro **cValues** de la estructura [SPropTagArray](sproptagarray.md) a la que apunta  _lpExcludeProps_ está establecido en 0. 
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal del indicador de progreso. 
    
 _lpProgress_
  
> [entrada] Puntero a una implementación de indicador de progreso. Si se pasa NULL en el  _parámetro lpProgress,_ MAPI proporciona la implementación del progreso. El _parámetro lpProgress_ se omite a menos que MAPI_DIALOG marca esté establecida en el _parámetro ulFlags._ 
    
 _lpDestInterface_
  
> [entrada] Puntero al identificador de interfaz que representa la interfaz que se va a usar para tener acceso al objeto para recibir las propiedades copiadas o movida.
    
 _lpDestObj_
  
> [entrada] Puntero al objeto para recibir las propiedades copiadas o movida.
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla la operación de copia o movimiento. Se pueden establecer las siguientes marcas:
    
MAPI_DIALOG 
  
> Muestra un indicador de progreso. 
    
MAPI_MOVE 
  
> **DoCopyTo debe** realizar una operación de movimiento en lugar de una operación de copia. Cuando no se establece esta marca, **DoCopyTo** realiza una operación de copia. 
    
MAPI_NOREPLACE 
  
> Las propiedades existentes en el objeto de destino no deben sobrescribirse. Cuando no se establece esta marca, **DoCopyTo** sobrescribe las propiedades existentes. 
    
 _lppProblems_
  
> [salida] En la entrada, un puntero a un puntero a una [estructura SPropProblemArray;](spropproblemarray.md) de lo contrario, NULL, que indica que no es necesario obtener información de error. Si  _lppProblems_ es un puntero válido en la entrada, **DoCopyTo** devuelve información detallada acerca de los errores al copiar una o más propiedades. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las propiedades se han copiado o movido correctamente.
    
MAPI_E_COLLISION 
  
> Ya existe una propiedad que se va a copiar o mover en el objeto de destino y se MAPI_NOREPLACE marca. 
    
MAPI_E_FOLDER_CYCLE 
  
> El objeto de origen contiene directa o indirectamente el objeto de destino. Es posible que se haya realizado un trabajo significativo antes de que se detectara esta condición, por lo que los objetos de origen y destino podrían modificarse parcialmente. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> La interfaz identificada por el parámetro  _lpSrcInterface_ no es compatible con el objeto al que apunta  _lpSrcObj_, o la interfaz identificada por el parámetro  _lpDestInterface_ no es compatible con el objeto que apunta  _lpDestObj_. 
    
MAPI_E_NO_ACCESS 
  
> Se intentó obtener acceso a un objeto para el que el autor de la llamada no tiene permisos suficientes. Este error se devuelve si el objeto de destino es el mismo que el objeto de origen.
    
MAPI_E_INVALID_PARAMETER 
  
> El  _parámetro lpSrcInterface_ es NULL. 
    
Los siguientes valores se pueden devolver en la **estructura SPropProblemArray,** pero no como valores devueltos **para DoCopyTo**. Estos errores se aplican a una sola propiedad.
  
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció MAPI_UNICODE marca y **DoCopyTo** no admite Unicode o MAPI_UNICODE no se estableció y **DoCopyTo** solo admite Unicode. 
    
MAPI_E_COMPUTED 
  
> El autor de la llamada no puede modificar la propiedad porque es una propiedad de solo lectura, calculada por el propietario del objeto de destino. Este error no es grave; el autor de la llamada debe permitir que continúe la operación de copia.
    
MAPI_E_INVALID_TYPE 
  
> El tipo de propiedad no es válido.
    
MAPI_E_UNEXPECTED_TYPE 
  
> El tipo de propiedad no es el tipo esperado por el autor de la llamada.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::D oCopyTo** se implementa para objetos de compatibilidad del proveedor de almacenamiento de mensajes. Los proveedores de almacenamiento de mensajes pueden llamar **a DoCopyTo** para implementar el método [IMAPIProp::CopyTo](imapiprop-copyto.md) para sus carpetas y mensajes. 
  
De forma predeterminada, **DoCopyTo** copia o mueve todas las propiedades de un objeto a otro objeto. Todos los subobjetos del objeto de origen se incluyen automáticamente en la operación y se copian o mueven en su totalidad. 
  
Si alguna de las propiedades copiadas o movida ya existe en el objeto de destino, las propiedades existentes se sobrescriben mediante las nuevas propiedades, a menos que la marca MAPI_NOREPLACE esté establecida en el parámetro _ulFlags._ La información existente en el objeto de destino que no se sobrescribe se deja sin tocar. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para excluir propiedades de la operación de copiar o mover, incluya sus etiquetas de propiedad en el parámetro _lpExcludeProps._ Si pasa los resultados de usar la macro PROP_TAG para crear una etiqueta de propiedad [a](prop_tag.md) partir de un identificador específico en la matriz de etiquetas de propiedad, se excluirán todas las propiedades con ese identificador. Por ejemplo, la siguiente entrada en la matriz de etiquetas de propiedades hace que todas las propiedades con un identificador de 0x8002 se excluyan, independientemente del tipo: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
Para evitar copiar la hora de entrega de un mensaje al copiar el mensaje en otra carpeta, especifique **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) en la matriz de exclusión de la etiqueta de propiedad. Para excluir la lista de destinatarios de un mensaje, agregue la propiedad **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) a la matriz de exclusión. Para excluir los datos adjuntos de un mensaje, agregue **la PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) a la matriz.
  
De forma similar, para evitar copiar o mover la jerarquía o la tabla de contenido de un contenedor de carpeta o libreta de direcciones, incluya **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) o **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) en la matriz de exclusión de la etiqueta de propiedad.
  
Ignore MAPI_E_COMPUTED errores devueltos en la **estructura SPropProblemArray** en el _parámetro lppProblems._ 
  
El identificador de interfaz al _que señala lpSrcInterface_ suele ser el mismo que el identificador de interfaz al que _apunta lpDestInterface._ 
  
Si pasa un identificador de interfaz aceptable en  _lpDestInterface_ pero un puntero no válido en  _lpDestObj_, los resultados son impredecibles. Lo más probable es que esto cause un error en el proveedor. 
  
Por el contrario, si conoce información complementaria que no se debe copiar ni mover, agregue los identificadores de interfaz de las interfaces que se excluirán en la matriz pasada en el parámetro _rgiidExclude._ Por ejemplo, si va a copiar mensajes, pero no ninguno de sus datos adjuntos, pase IID_IMessage en la matriz _rgiidExclude._ **DoCopyTo omite** las interfaces enumeradas  _en rgiidExclude_ que no reconoce. 
  
Cuando se usa el  _parámetro rgiidExclude_ para excluir una interfaz, también se excluyen todas las interfaces derivadas de esa interfaz. Por ejemplo, la exclusión de la [interfaz IMAPIContainer](imapicontainerimapiprop.md) hace que se excluyan carpetas o contenedores de libreta de direcciones, según el tipo de proveedor. No excluya [IMAPIProp](imapipropiunknown.md) o [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) porque muchas interfaces derivan de ellas. 
  
 **DoCopyTo notifica** los errores globales que se aplican a la operación en su totalidad y los errores individuales que se aplican a propiedades individuales. Estos errores individuales se ponen en una **estructura SPropProblemArray.** Puede suprimir los informes de errores en el nivel de propiedad pasando NULL, en lugar de un puntero válido, para el parámetro de estructura de la matriz de problemas de propiedad. 
  
Si desea recibir información sobre errores, pase un puntero de estructura **SPropProblemArray** válido en el parámetro _lppProblems._ Cuando **DoCopyTo devuelve** S_OK, compruebe si hay errores posibles con propiedades individuales en la estructura. Cuando **DoCopyTo devuelve** un error, no se devuelve información en la **estructura SPropProblemArray.** En su lugar, llame [al método IMAPISupport::GetLastError](imapisupport-getlasterror.md) para recuperar información detallada del error. 
  
Si **DoCopyTo** devuelve S_OK, libera la estructura **SPropProblemArray** devuelta llamando a la [función MAPIFreeBuffer.](mapifreebuffer.md) 
  
Si se produce un error global en la llamada **a DoCopyTo,** no use ni libre la estructura **SPropProblemArray.** Los proveedores deben omitir el  _miembro ulIndex_ en **las estructuras SPropProblemArray** devueltas **por DoCopyTo**.
  
## <a name="see-also"></a>Consulte también



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

