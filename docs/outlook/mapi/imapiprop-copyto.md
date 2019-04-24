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

## <a name="parameters"></a>Parameters

 _ciidExclude_
  
> a Número de interfaces que se van a excluir al copiar o mover las propiedades.
    
 _rgiidExclude_
  
> a Matriz de identificadores de interfaz (IID) que especifican interfaces que no se deben usar cuando se copia o se mueve información complementaria al objeto de destino.
    
 _lpExcludeProps_
  
> a Un puntero a una matriz de etiquetas de propiedad que identifica las etiquetas de propiedad que se deben excluir de la operación de copia o movimiento. Pasar **null** en el parámetro _lpExcludeProps_ indica que todas las propiedades del objeto se deben copiar o mover. **CopyTo** devuelve MAPI_E_INVALID_PARAMETER cuando el miembro **cValues** de la estructura [SPropProblemArray](spropproblemarray.md) a la que apunta _lpExcludeProps_ se establece en 0. 
    
 _ulUIParam_
  
> a Identificador de la ventana primaria del indicador de progreso. 
    
 _lpProgress_
  
> a Un puntero a una implementación del indicador de progreso. Si se pasa **null** en el parámetro _lpProgress_ , MAPI proporciona la implementación del progreso. El parámetro _lpProgress_ se omite a menos que se establezca la marca MAPI_DIALOG en el parámetro _ulFlags_ . 
    
 _lpInterface_
  
> a Un puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso al objeto al que apunta el parámetro _lpDestObj_ . El parámetro _lpInterface_ no debe ser **nulo**.
    
 _lpDestObj_
  
> a Un puntero al objeto que va a recibir las propiedades que se han copiado o movido.
    
 _ulFlags_
  
> a Una máscara de máscara de marcadores que controla la operación de copiar o mover. Se pueden establecer los siguientes indicadores:
    
MAPI_DECLINE_OK 
  
> Si **CopyTo** llama al método [IMAPISupport::D ocopyto](imapisupport-docopyto.md) para controlar la operación de copia o movimiento, en su lugar debe volver inmediatamente con el valor de error MAPI_E_DECLINE_COPY. MAPI establece la marca MAPI_DECLINE_OK para limitar la recursividad. Los clientes no establecen esta marca. 
    
MAPI_DIALOG 
  
> Muestra un indicador de progreso.
    
MAPI_MOVE 
  
> **CopyTo** debe realizar una operación de movimiento en lugar de una operación de copia. Si no se establece esta marca, **CopyTo** realiza una operación de copia. 
    
MAPI_NOREPLACE 
  
> Las propiedades existentes en el objeto de destino no se deben sobrescribir. Si no se establece este indicador, **CopyTo** sobrescribe las propiedades existentes. 
    
 _lppProblems_
  
> [in, out] En la entrada, un puntero a un puntero a una estructura **SPropProblemArray** ; de lo contrario, **null**, que indica que no es necesaria información de error. Si _lppProblems_ es un puntero válido en la entrada **** , CopyTo devuelve información detallada sobre los errores al copiar una o más propiedades. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las propiedades se han copiado o movido correctamente.
    
MAPI_E_COLLISION 
  
> No se puede copiar un subobjeto porque ya existe un subobjeto con el mismo nombre para mostrar, especificado por la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), en el objeto de destino. 
    
MAPI_E_DECLINE_COPY 
  
> El proveedor de servicios no implementa la operación de copia.
    
MAPI_E_FOLDER_CYCLE 
  
> El objeto de origen que realiza la operación de copia o movimiento contiene directa o indirectamente el objeto de destino. Es posible que se haya realizado un trabajo significativo antes de que se detectara esta condición, por lo que los objetos de origen y de destino podrían modificarse parcialmente. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> La interfaz identificada por el parámetro _lpInterface_ no es compatible con el objeto de destino. 
    
MAPI_E_NO_ACCESS 
  
> Se intentó obtener acceso a un objeto para el que el autor de la llamada no tiene permisos suficientes. Este error se devuelve si el objeto de destino es el mismo que el objeto de origen.
    
Los valores siguientes se pueden devolver en la estructura **SPropProblemArray** , pero no como valores devueltos para **CopyTo**. Los errores siguientes se aplican a una sola propiedad:
  
MAPI_E_BAD_CHARWIDTH 
  
> Se ha establecido la marca MAPI_UNICODE y **CopyTo** no admite Unicode, o bien no se ha establecido MAPI_UNICODE **** y CopyTo solo admite Unicode. 
    
MAPI_E_COMPUTED 
  
> La propiedad no la puede modificar el autor de la llamada porque es una propiedad de solo lectura, calculada por el propietario del objeto de destino. Este error no es grave; el autor de la llamada debe permitir que continúe la operación de copia.
    
MAPI_E_INVALID_TYPE 
  
> El tipo de propiedad no es válido.
    
MAPI_E_UNEXPECTED_TYPE 
  
> El tipo de propiedad no es el tipo que espera el autor de la llamada.
    
## <a name="remarks"></a>Comentarios

De forma predeterminada, el método **IMAPIProp:: CopyTo** copia o mueve todas las propiedades del objeto actual a un objeto de destino. **CopyTo** se usa cuando un objeto se debe copiar o mover exactamente, con todas o casi todas sus propiedades intactas. 
  
Todos los subobjetos del objeto de origen se incluyen automáticamente en la operación y se copian o se mueven en su totalidad. De forma predeterminada **** , CopyTo sobrescribe las propiedades del objeto de destino que coinciden con las propiedades del objeto de origen. Si alguna de las propiedades que se han copiado o movido ya existe en el objeto de destino, las propiedades existentes se sobrescriben con las nuevas propiedades, a menos que la marca MAPI_NOREPLACE se establezca en el parámetro _ulFlags_ . La información existente en el objeto de destino que no se sobrescribe permanece inalterada. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Puede proporcionar una implementación completa de **CopyTo** o confiar en la implementación que proporciona MAPI en su objeto de soporte. Si desea usar la implementación de MAPI, llame a **IMAPISupport::D ocopyto**. Sin embargo, si realiza el procesamiento delegado **** en encopyto y se le pasa la marca MAPI_DECLINE_OK, evite la llamada al soporte técnico y devuelva MAPI_E_DECLINE_COPY en su lugar. MAPI llamará con esta marca para evitar la posible recursividad que puede ocurrir cuando se copian carpetas. 
  
Como la operación de copia puede ser prolongada, debe mostrar un indicador de progreso. Use la implementación de [método imapiprogress](imapiprogressiunknown.md) que se ha pasado en el parámetro _lpProgress_ , si hay alguno. Si _lpProgress_ es **null**, llame al método [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) para usar la implementación de MAPI. 
  
No intente establecer ninguna de las propiedades de solo lectura conocidas en el objeto de destino; Devuelve MAPI_E_NO_ACCESS en su lugar.
  
Los objetos de origen y de destino deben usar las mismas interfaces. Devuelve MAPI_E_INVALID_PARAMETER si no se establece _lpInterface_ . 
  
Devuelve MAPI_E_INTERFACE_NOT_SUPPORTED si se excluyen todas las interfaces conocidas.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

No establezca la marca MAPI_DECLINE_OK; MAPI la usa en sus llamadas a implementaciones **CopyTo** del proveedor de almacenamiento de mensajes. 
  
Como las operaciones de copiar y mover pueden tardar algún tiempo, debe solicitar la presentación de un indicador de progreso estableciendo la marca MAPI_DIALOG. Puede establecer el parámetro _lpProgress_ en su implementación de **método imapiprogress**, si tiene uno, o en **null**. Si _lpProgress_ es **null**, **CopyTo** usará el indicador de progreso predeterminado que proporciona MAPI. 
  
Puede suprimir la presentación de un indicador de progreso si no se configura la marca MAPI_DIALOG. **CopyTo** omitirá los parámetros _ulUIParam_ y _lpProgress_ , y no mostrará el indicador. 
  
 **CopyTo** puede informar de errores globales y individuales, o errores que se producen con una o más propiedades. Estos errores individuales se colocan en una estructura **SPropProblemArray** . Puede suprimir los informes de errores en el nivel de propiedad pasando **null**, en lugar de un puntero válido, para el parámetro de estructura de matriz con problemas de propiedad. 
  
Si desea recibir información sobre los errores, pase un puntero de estructura **SPropProblemArray** válido en el parámetro _lppProblems_ . Cuando **CopyTo** Devuelve S_OK, compruebe si hay posibles errores con propiedades individuales en la estructura. Cuando **CopyTo** devuelve un error, no se devuelve información en la estructura **SPropProblemArray** . En su lugar, llame a [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) para recuperar información detallada del error. 
  
Si **CopyTo** Devuelve S_OK, libere la estructura **SPropProblemArray** devuelta llamando a la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Si copia propiedades que son exclusivas del tipo de objeto de origen, debe asegurarse de que el objeto de destino es del mismo tipo. **CopyTo** no impide que se asocien propiedades que, por lo general, pertenecen a un tipo de objeto con otro tipo de objeto. El usuario debe copiar las propiedades que tengan sentido para el objeto de destino. Por ejemplo, no debe copiar las propiedades de los mensajes en un contenedor de libretas de direcciones. 
  
Para asegurarse de que copia entre objetos del mismo tipo, compruebe que el objeto de origen y el de destino son el mismo tipo, ya sea comparando los punteros de objeto o llamando a [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx). Establezca el identificador de interfaz al que apunta _lpInterface_ en la interfaz estándar del objeto de origen. Además, asegúrese de que la propiedad tipo de objeto o **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) es la misma para los dos objetos. Por ejemplo, si copia de un mensaje, establezca _lpInterface_ en IID_IMessage y el **PR_OBJECT_TYPE** para ambos objetos en MAPI_MESSAGE. 
  
Si se pasa un puntero no válido en el parámetro _lpDestObj_ , los resultados son imprevisibles. 
  
La exclusión de propiedades **** en una llamada a CopyTo puede ser útil. Por ejemplo, algunos objetos tienen propiedades que son específicas de una única instancia del objeto, como la fecha y la hora de la entrega del mensaje. Para evitar copiar el tiempo de entrega de un mensaje cuando copia el mensaje en una carpeta diferente, especifique **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) en la etiqueta de exclusión de la etiqueta de propiedad. Para excluir la lista de destinatarios de un mensaje, agregue la propiedad **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) a la matriz de exclusión. Para excluir los datos adjuntos de un mensaje, agregue la propiedad **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) a la matriz.
  
De forma similar, evite copiar o mover una carpeta o una jerarquía de contenedor de libreta de direcciones o de contenido incluyendo **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) o **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) en la matriz de exclusión de etiquetas de propiedad.
  
Para excluir propiedades de la operación de copiar o mover, incluya sus etiquetas de propiedad en el parámetro _lpExcludeProps_ . Si pasa los resultados de la macro **PROP_TAG** para crear una etiqueta de propiedad a partir de un identificador específico de la matriz de etiquetas de propiedades, se excluirán todas las propiedades con ese identificador. Por ejemplo, la siguiente entrada en la matriz de etiquetas de propiedad hace que se excluyan todas las propiedades con un identificador de 0x8002, independientemente del tipo: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
La etiqueta de propiedad **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) no se puede incluir en la matriz de _lpExcludeProps_ . 
  
La utilidad de la característica **CopyTo** para excluir interfaces quizá no es tan evidente como la utilidad de excluir las propiedades. Puede excluir una interfaz al copiar a un objeto que no tenga ningún conocimiento de un grupo de propiedades. Por ejemplo, si se copian propiedades de una carpeta a datos adjuntos, las únicas propiedades con las que se pueden trabajar los datos adjuntos son las propiedades genéricas disponibles con cualquier implementación de [IMAPIProp](imapipropiunknown.md) . Si se excluye [IMAPIFolder](imapifolderimapicontainer.md) de la operación de copia, los datos adjuntos no recibirán ninguna de las propiedades de carpeta más específicas. 
  
Cuando se usa el parámetro _rgiidExclude_ para excluir una interfaz, también se excluyen todas las interfaces derivadas de esa interfaz. Por ejemplo, excluir [IMAPIContainer](imapicontainerimapiprop.md) hace que se excluyan las carpetas o los contenedores de la libreta de direcciones, según el tipo de proveedor. No excluya **IMAPIProp** o [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) porque hay tantas interfaces que se derivan de ellos. 
  
Omite los errores de MAPI_E_COMPUTED devueltos en la estructura **SPropProblemArray** en el parámetro _lppProblems_ . 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|Archivo. cpp  <br/> |LoadFromMSG  <br/> |MFCMAPI usa el método **IMAPIProp:: CopyTo** para copiar las propiedades de un archivo. msg a un objeto [IMAPIMessageSite](imapimessagesiteiunknown.md) .  <br/> |
|FolderDlg. cpp  <br/> |CFolderDlg:: HandlePaste  <br/> |MFCMAPI usa el método **IMAPIProp:: CopyTo** para copiar las propiedades de un mensaje de origen en un mensaje de destino durante una operación de pegado.  <br/> |
   
## <a name="see-also"></a>Vea también



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

