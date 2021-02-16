---
title: IMAPIPropCopyTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyTo
api_type:
- COM
ms.assetid: e56042e9-5bb7-4a99-b6de-1546d4ca07f0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f76b0a5482647fe3e181a36d7dcd8cb60ffc8985
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356395"
---
# <a name="imapipropcopyto"></a>IMAPIProp::CopyTo

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Copia o mueve todas las propiedades, excepto las propiedades excluidas específicamente.
  
```cpp
HRESULT CopyTo(
 ULONG ciidExclude,
 LPCIID rgiidExclude,
 LPSPropTagArray lpExcludeProps,
 ULONG_PTR ulUIParam,
 LPMAPIPROGRESS lpProgress,
 LPCIID lpInterface,
 LPVOID lpDestObj,
 ULONG ulFlags,
 LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parámetros

 _ciidExclude_
  
> [entrada] Recuento de interfaces que se excluirán cuando se copien o se mueven las propiedades.
    
 _rgiidExclude_
  
> [entrada] Matriz de identificadores de interfaz (IID) que especifican interfaces que no deben usarse cuando se copia o mueve información complementaria al objeto de destino.
    
 _lpExcludeProps_
  
> [entrada] Puntero a una matriz de etiquetas de propiedades que identifica las etiquetas de propiedad que deben excluirse de la operación de copia o movimiento. Pasar **null** en  _el parámetro lpExcludeProps_ indica que todas las propiedades del objeto deben copiarse o moverse. **CopyTo** devuelve MAPI_E_INVALID_PARAMETER cuando el miembro **cValues** de la estructura [SPropProblemArray](spropproblemarray.md) a la que apunta  _lpExcludeProps_ está establecido en 0. 
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal del indicador de progreso. 
    
 _lpProgress_
  
> [entrada] Puntero a una implementación de indicador de progreso. Si **se** pasa null en el  _parámetro lpProgress,_ MAPI proporciona la implementación del progreso. El _parámetro lpProgress_ se omite a menos que MAPI_DIALOG marca esté establecida en el _parámetro ulFlags._ 
    
 _lpInterface_
  
> [entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para tener acceso al objeto al que apunta el parámetro _lpDestObj._ El _parámetro lpInterface_ no debe ser **nulo.**
    
 _lpDestObj_
  
> [entrada] Puntero al objeto para recibir las propiedades copiadas o movida.
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla la operación de copia o movimiento. Se pueden establecer las siguientes marcas:
    
MAPI_DECLINE_OK 
  
> Si **CopyTo** llama al método [IMAPISupport::D oCopyTo](imapisupport-docopyto.md) para controlar la operación de copia o movimiento, debería devolverse inmediatamente con el valor de error MAPI_E_DECLINE_COPY. MAPI MAPI_DECLINE_OK marca para limitar la recursión. Los clientes no establecen esta marca. 
    
MAPI_DIALOG 
  
> Muestra un indicador de progreso.
    
MAPI_MOVE 
  
> **CopyTo** debe realizar una operación de movimiento en lugar de una operación de copia. Cuando no se establece esta marca, **CopyTo** realiza una operación de copia. 
    
MAPI_NOREPLACE 
  
> Las propiedades existentes en el objeto de destino no deben sobrescribirse. Cuando no se establece esta marca, **CopyTo** sobrescribe las propiedades existentes. 
    
 _lppProblems_
  
> [entrada, salida] En la entrada, un puntero a un puntero a una **estructura SPropProblemArray;** de lo **contrario, null**, que indica que no es necesario obtener información de error. Si  _lppProblems_ es un puntero válido en la entrada, **CopyTo** devuelve información detallada acerca de los errores al copiar una o más propiedades. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las propiedades se han copiado o movido correctamente.
    
MAPI_E_COLLISION 
  
> No se puede copiar un subobjeto porque ya existe un subobjeto con el mismo nombre para mostrar ( especificado por la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) en el objeto de destino. 
    
MAPI_E_DECLINE_COPY 
  
> El proveedor de servicios no implementa la operación de copia.
    
MAPI_E_FOLDER_CYCLE 
  
> El objeto de origen que realiza la operación de copia o movimiento directa o indirectamente contiene el objeto de destino. Es posible que se haya realizado un trabajo significativo antes de que se detectara esta condición, por lo que los objetos de origen y destino podrían modificarse parcialmente. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> La interfaz identificada por el  _parámetro lpInterface_ no es compatible con el objeto de destino. 
    
MAPI_E_NO_ACCESS 
  
> Se intentó obtener acceso a un objeto para el que el autor de la llamada no tiene permisos suficientes. Este error se devuelve si el objeto de destino es el mismo que el objeto de origen.
    
Los siguientes valores se pueden devolver en la **estructura SPropProblemArray,** pero no como valores devueltos **para CopyTo**. Los siguientes errores se aplican a una sola propiedad:
  
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció MAPI_UNICODE marca y **CopyTo** no admite Unicode, o MAPI_UNICODE no se estableció y **CopyTo** solo admite Unicode. 
    
MAPI_E_COMPUTED 
  
> El autor de la llamada no puede modificar la propiedad porque es una propiedad de solo lectura, calculada por el propietario del objeto de destino. Este error no es grave; el autor de la llamada debe permitir que continúe la operación de copia.
    
MAPI_E_INVALID_TYPE 
  
> El tipo de propiedad no es válido.
    
MAPI_E_UNEXPECTED_TYPE 
  
> El tipo de propiedad no es el tipo esperado por el autor de la llamada.
    
## <a name="remarks"></a>Comentarios

De forma predeterminada, el **método IMAPIProp::CopyTo** copia o mueve todas las propiedades del objeto actual a un objeto de destino. **CopyTo** se usa cuando un objeto debe copiarse o moverse exactamente, con todas o la mayoría de sus propiedades intactas. 
  
Todos los subobjetos del objeto de origen se incluyen automáticamente en la operación y se copian o mueven en su totalidad. De forma predeterminada, **CopyTo** sobrescribe las propiedades del objeto de destino que coinciden con las propiedades del objeto de origen. Si alguna de las propiedades copiadas o movida ya existe en el objeto de destino, las propiedades existentes se sobrescriben mediante las nuevas propiedades, a menos que la marca MAPI_NOREPLACE esté establecida en el parámetro _ulFlags._ La información existente en el objeto de destino que no se sobrescribe se deja sin tocar. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Puede proporcionar una implementación completa de **CopyTo** o confiar en la implementación que MAPI proporciona en su objeto de compatibilidad. Si desea usar la implementación MAPI, llame a **IMAPISupport::D oCopyTo**. Sin embargo, si delega el procesamiento en **DoCopyTo** y se le pasa la marca MAPI_DECLINE_OK, evite la llamada de soporte técnico y devuelva MAPI_E_DECLINE_COPY en su lugar. MAPI llamará con esta marca para evitar la posible recursión que puede ocurrir cuando se copian carpetas. 
  
Dado que la operación de copia puede ser larga, debe mostrar un indicador de progreso. Use la [implementación IMAPIProgress](imapiprogressiunknown.md) pasada en el parámetro  _lpProgress,_ si la hay. Si  _lpProgress_ es **null,** llame al método [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) para usar la implementación mapi. 
  
No intente establecer ninguna propiedad de solo lectura conocida en el objeto de destino; devolver MAPI_E_NO_ACCESS en su lugar.
  
Los objetos de origen y destino deben usar las mismas interfaces. Devuelve MAPI_E_INVALID_PARAMETER si  _lpInterface_ no está establecido. 
  
Devuelve MAPI_E_INTERFACE_NOT_SUPPORTED si se excluyen todas las interfaces conocidas.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

No establezca la marca MAPI_DECLINE_OK; MAPI lo usa en sus llamadas a implementaciones **CopyTo** del proveedor del almacén de mensajes. 
  
Dado que las operaciones de copiar y mover pueden tardar tiempo, debe solicitar la visualización de un indicador de progreso estableciendo la MAPI_DIALOG de movimiento. Puede establecer el parámetro  _lpProgress_ en la implementación de **IMAPIProgress**, si tiene uno, o en **null**. Si  _lpProgress es_ **nulo,** **CopyTo** usará el indicador de progreso predeterminado que proporciona MAPI. 
  
Puedes suprimir la presentación de un indicador de progreso si no estableces la MAPI_DIALOG indicador. **CopyTo** omitirá  _los parámetros ulUIParam_ y  _lpProgress_ y no mostrará el indicador. 
  
 **CopyTo puede** notificar errores globales e individuales, o errores que se producen con una o más propiedades. Estos errores individuales se colocan en una **estructura SPropProblemArray.** Puede suprimir los informes de errores en el nivel de propiedad pasando **null**, en lugar de un puntero válido, para el parámetro de estructura de la matriz de problemas de propiedad. 
  
Si desea recibir información sobre errores, pase un puntero de estructura **SPropProblemArray** válido en el parámetro _lppProblems._ Cuando **CopyTo** devuelve S_OK, compruebe si hay errores posibles con propiedades individuales en la estructura. Cuando **CopyTo** devuelve un error, no se devuelve información en la **estructura SPropProblemArray.** En su lugar, [llame a IMAPIProp::GetLastError](imapiprop-getlasterror.md) para recuperar información detallada del error. 
  
Si **CopyTo** devuelve S_OK, libera la estructura **SPropProblemArray** devuelta llamando a la [función MAPIFreeBuffer.](mapifreebuffer.md) 
  
Si copia las propiedades que son exclusivas del tipo de objeto de origen, debe asegurarse de que el objeto de destino sea del mismo tipo. **CopyTo** no impide asociar propiedades que normalmente pertenecen a un tipo de objeto con otro tipo de objeto. Es usted el que debe copiar las propiedades que tienen sentido para el objeto de destino. Por ejemplo, no debe copiar las propiedades del mensaje en un contenedor de libreta de direcciones. 
  
Para asegurarse de copiar entre objetos del mismo tipo, compruebe que el objeto de origen y de destino sean del mismo tipo, ya sea comparando punteros de objeto o llamando a [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx). Establece el identificador de interfaz al que  _apunta lpInterface_ en la interfaz estándar para el objeto de origen. Además, asegúrese de que el tipo de **objeto PR_OBJECT_TYPE** propiedad ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) sea la misma para los dos objetos. Por ejemplo, si copia desde un mensaje, establezca _lpInterface_ en IID_IMessage y el PR_OBJECT_TYPE para ambos objetos en MAPI_MESSAGE.  
  
Si se pasa un puntero no válido en el  _parámetro lpDestObj,_ los resultados son impredecibles. 
  
Excluir las propiedades de **una llamada CopyTo** puede ser útil. Por ejemplo, algunos objetos tienen propiedades específicas de una sola instancia del objeto, como la fecha y la hora de entrega del mensaje. Para evitar copiar la hora de entrega de un mensaje al copiar el mensaje en otra carpeta, especifique **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) en la matriz de exclusión de etiqueta de propiedad. Para excluir la lista de destinatarios de un mensaje, agregue la propiedad **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) a la matriz de exclusión. Para excluir los datos adjuntos de un mensaje, agregue **la PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) a la matriz.
  
De forma similar, evita copiar o mover la jerarquía o la tabla de contenido de un contenedor de carpeta o libreta de direcciones incluyendo **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) o **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) en la matriz de exclusión de la etiqueta de propiedad.
  
Para excluir propiedades de la operación de copiar o mover, incluya sus etiquetas de propiedad en el parámetro _lpExcludeProps._ Si pasa los resultados de la macro PROP_TAG para crear una etiqueta de propiedad **a** partir de un identificador específico en la matriz de etiquetas de propiedad, se excluirán todas las propiedades con ese identificador. Por ejemplo, la siguiente entrada en la matriz de etiquetas de propiedades hace que todas las propiedades con un identificador de 0x8002 se excluyan, independientemente del tipo: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
La **PR_NULL** de propiedad ([PidTagNull](pidtagnull-canonical-property.md)) no se puede incluir en la matriz _lpExcludeProps._ 
  
La utilidad de la característica **CopyTo** para excluir interfaces quizás no sea tan obvia como la utilidad de excluir propiedades. Puede excluir una interfaz al copiar a un objeto que no tiene conocimiento de un grupo de propiedades. Por ejemplo, si copia propiedades de una carpeta a datos adjuntos, las únicas propiedades con las que pueden trabajar los datos adjuntos son las propiedades genéricas disponibles con cualquier [implementación imapiprop.](imapipropiunknown.md) Al excluir [IMAPIFolder de](imapifolderimapicontainer.md) la operación de copia, los datos adjuntos no recibirán ninguna de las propiedades de carpeta más específicas. 
  
Cuando se usa el  _parámetro rgiidExclude_ para excluir una interfaz, también se excluyen todas las interfaces derivadas de esa interfaz. Por ejemplo, la exclusión de [IMAPIContainer](imapicontainerimapiprop.md) hace que se excluyan carpetas o contenedores de libreta de direcciones, según el tipo de proveedor. No excluya **IMAPIProp** o [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) porque muchas interfaces derivan de ellas. 
  
Omitir MAPI_E_COMPUTED errores devueltos en la **estructura SPropProblemArray** en el parámetro _lppProblems._ 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadFromMSG  <br/> |MFCMAPI usa el **método IMAPIProp::CopyTo** para copiar propiedades de un archivo .msg a un [objeto IMAPIMessageSite.](imapimessagesiteiunknown.md)  <br/> |
|FolderDlg.cpp  <br/> |CFolderDlg::HandlePaste  <br/> |MFCMAPI usa el **método IMAPIProp::CopyTo** para copiar propiedades de un mensaje de origen a un mensaje de destino durante una operación de pegado.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)
  
[IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propiedad canónica PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[Propiedad canónica PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[Propiedad canónica PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)
  
[Propiedad canónica PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)
  
[Propiedad canónica PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[Propiedad canónica PidTagObjectType](pidtagobjecttype-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

