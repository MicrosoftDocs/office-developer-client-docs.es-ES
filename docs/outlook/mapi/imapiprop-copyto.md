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
ms.openlocfilehash: aa2869b1e3495bfb8a431e79a55d11a1ee1c5ca6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817403"
---
# <a name="imapipropcopyto"></a>IMAPIProp::CopyTo

  
  
**Hace referencia a**: Outlook 
  
Copia o mueve todas las propiedades, excepto propiedades excluidas específicamente.
  
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
  
> [entrada] El recuento de interfaces que se deben excluir cuando se copian o se mueven las propiedades.
    
 _rgiidExclude_
  
> [entrada] Una matriz de identificadores de interfaz (IID) que especifican las interfaces que no se deben usar cuando información complementaria se copian o se mueve para el objeto de destino.
    
 _lpExcludeProps_
  
> [entrada] Un puntero a una matriz de etiqueta de propiedad que identifica las etiquetas de propiedad que se deben excluir de la copia o la operación de movimiento. Pasar **null** en el parámetro _lpExcludeProps_ indica que todas las propiedades del objeto deben copiar o mover. **CopyTo** devuelve MAPI_E_INVALID_PARAMETER cuando el miembro **cValues** de la estructura [SPropProblemArray](spropproblemarray.md) que apunta _lpExcludeProps_ se establece en 0. 
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal del indicador de progreso. 
    
 _lpProgress_
  
> [entrada] Un puntero a una implementación de indicador de progreso. Si se pasa **null** en el parámetro _lpProgress_ , MAPI proporciona la implementación de progreso. El parámetro _lpProgress_ se omite a menos que la marca MAPI_DIALOG se establece en el parámetro _ulFlags indicado_ . 
    
 _lpInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al objeto al que apunta el parámetro _lpDestObj_ . El parámetro _lpInterface_ no debe ser **null**.
    
 _lpDestObj_
  
> [entrada] Un puntero al objeto que se va a recibir las propiedades que se ha movido o copiadas.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla la operación de copiar o mover. Se pueden establecer los siguientes indicadores:
    
MAPI_DECLINE_OK 
  
> Si **CopyTo** llama al método de [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) para controlar la copia o la operación de movimiento, debe en su lugar devolver inmediatamente con el valor de error MAPI_E_DECLINE_COPY. Para limitar la recursividad, se establece la marca MAPI_DECLINE_OK de MAPI. Los clientes no establezca esta marca. 
    
MAPI_DIALOG 
  
> Muestra un indicador de progreso.
    
MAPI_MOVE 
  
> **CopyTo** debe realizar una operación de movimiento en lugar de una operación de copia. Cuando no se establece este marcador, **CopyTo** realiza una operación de copia. 
    
MAPI_NOREPLACE 
  
> No se deben sobrescribir las propiedades existentes en el objeto de destino. Cuando no se establece este marcador, **CopyTo** sobrescribe las propiedades existentes. 
    
 _lppProblems_
  
> [entrada, salida] En la entrada, un puntero a un puntero a una estructura **SPropProblemArray** ; en caso contrario, **null**, que indica que no hay necesidad de información de error. Si _lppProblems_ es un puntero válido en la entrada, **CopyTo** devuelve información detallada acerca de los errores de copiar una o más propiedades. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las propiedades se hayan copiado o movido correctamente.
    
MAPI_E_COLLISION 
  
> No se puede copiar un subobjetos porque un subobjetos con el mismo nombre para mostrar, especificado por la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) — ya existe en el objeto de destino. 
    
MAPI_E_DECLINE_COPY 
  
> El proveedor de servicios no implementa la operación de copia.
    
MAPI_E_FOLDER_CYCLE 
  
> El objeto de origen a realizar la operación de copiar o mover directa o indirectamente contiene el objeto de destino. Trabajo significativo es posible que se han realizado antes de que se ha detectado esta condición, por lo que los objetos de origen y de destino podrían modificarse parcialmente. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> La interfaz identificada mediante el parámetro _lpInterface_ no es compatible con el objeto de destino. 
    
MAPI_E_NO_ACCESS 
  
> Se ha intentado tener acceso a un objeto para el que el autor de la llamada no tiene permisos suficientes. Este error se devuelve si el objeto de destino es el mismo que el objeto de origen.
    
Los siguientes valores se pueden devolver en la estructura de **SPropProblemArray** , pero no como valores devueltos por **CopyTo**. Los errores siguientes se aplican a una sola propiedad:
  
MAPI_E_BAD_CHARWIDTH 
  
> Se ha establecido el indicador MAPI_UNICODE y **CopyTo** no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y **CopyTo** admite sólo Unicode. 
    
MAPI_E_COMPUTED 
  
> La propiedad no puede modificarse el autor de la llamada porque es una propiedad de solo lectura, calculada por el propietario del objeto de destino. Este error no es grave; el autor de la llamada debe permitir que la operación de copia continuar.
    
MAPI_E_INVALID_TYPE 
  
> El tipo de propiedad no es válido.
    
MAPI_E_UNEXPECTED_TYPE 
  
> El tipo de propiedad no es el tipo esperado por el autor de la llamada.
    
## <a name="remarks"></a>Comentarios

De forma predeterminada, el método **IMAPIProp::CopyTo** copia o mueve todas las propiedades del objeto actual a un objeto de destino. **CopyTo** se usa cuando un objeto debe ser copiado o movido exactamente, con todos o la mayoría de sus propiedades intactas. 
  
Los objetos secundarios en el objeto de origen se incluyen automáticamente en la operación y se copian o mueven en su totalidad. De forma predeterminada, **CopyTo** sobrescribe cualquier propiedades en el objeto de destino que coinciden con las propiedades del objeto de origen. Si cualquiera de las propiedades que se ha movido o copiadas ya existe en el objeto de destino, se sobrescriben las propiedades existentes por las nuevas propiedades, a menos que se establece la marca MAPI_NOREPLACE en el parámetro _ulFlags indicado_ . Información existente en el objeto de destino que no se sobrescribe se toca. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Puede proporcionar una implementación completa de **CopyTo** o se basan en la implementación que proporciona MAPI en su objeto de soporte técnico. Si desea utilizar la implementación de MAPI, llame a **IMAPISupport::DoCopyTo**. Sin embargo, si delegar procesamiento a **DoCopyTo** y se pasa el indicador MAPI_DECLINE_OK, evitar la llamada de soporte técnico y devolver MAPI_E_DECLINE_COPY en su lugar. MAPI llamará a con esta marca para evitar la recursividad posible que puede ocurrir cuando se copian las carpetas. 
  
Debido a que la operación de copia puede ser prolongada, debe mostrar un indicador de progreso. Utilice la implementación de [IMAPIProgress](imapiprogressiunknown.md) que se pasa en el parámetro _lpProgress_ , si hay alguno. Si _lpProgress_ es **null**, llame al método [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) para usar la implementación de MAPI. 
  
No intente establecer las propiedades de solo lectura conocidas en el objeto de destino; devolver MAPI_E_NO_ACCESS en su lugar.
  
Los objetos de origen y de destino deben utilizar las mismas interfaces. Devolver MAPI_E_INVALID_PARAMETER si _lpInterface_ no está establecido. 
  
Devolver MAPI_E_INTERFACE_NOT_SUPPORTED si se excluyen todas las interfaces conocidas.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

No se establece la marca MAPI_DECLINE_OK; MAPI utiliza en sus llamadas a las implementaciones de **CopyTo** de proveedor de almacén de mensajes. 
  
Debido a que las operaciones de copia y movimiento pueden tardar, debería solicitar la visualización de un indicador de progreso estableciendo el indicador MAPI_DIALOG. Puede establecer el parámetro _lpProgress_ a la implementación de **IMAPIProgress**, si dispone de uno, o en **null**. Si _lpProgress_ es **null**, **CopyTo** usará el indicador de progreso predeterminada que proporciona de MAPI. 
  
Puede suprimir la visualización de un indicador de progreso no establecer el indicador MAPI_DIALOG. **CopyTo** pasará por alto los parámetros _ulUIParam_ y _lpProgress_ y no se mostrará el indicador. 
  
 **CopyTo** puede informar errores globales e individuales o errores que se producen con una o más propiedades. Estos errores individuales se colocan en una estructura **SPropProblemArray** . Puede suprimir informes en el nivel de propiedad pasando **null**, en lugar de un puntero válido para el parámetro de estructura de matriz de propiedad problema de error. 
  
Si desea recibir información acerca de los errores, pase un puntero de estructura **SPropProblemArray** válido en el parámetro _lppProblems_ . Cuando **CopyTo** devuelve S_OK, comprobar los posibles errores con las propiedades individuales de la estructura de. Cuando **CopyTo** devuelve un error, no se devuelve información de la estructura de **SPropProblemArray** . En su lugar, llame a [IMAPIProp::GetLastError](imapiprop-getlasterror.md) para recuperar información detallada del error. 
  
Si **CopyTo** devuelve S_OK, liberar la estructura **SPropProblemArray** devuelta por una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Si copia las propiedades que son únicas para el tipo de objeto de origen, debe asegurarse de que el objeto de destino es del mismo tipo. **CopyTo** no impide la asociación de las propiedades que suelen pertenecen a un tipo de objeto con otro tipo de objeto. Depende de usted para copiar las propiedades que tienen sentido para el objeto de destino. Por ejemplo, no debe copiar las propiedades del mensaje a un contenedor de la libreta de direcciones. 
  
Para asegurarse de que copie entre objetos del mismo tipo, compruebe que el objeto de origen y de destino son el mismo tipo, ya sea mediante la comparación de punteros a objetos o llamar a [IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx). Establecer el identificador de interfaz que señala _lpInterface_ a la interfaz estándar para el objeto de origen. Además, asegúrese de que el tipo de objeto o la propiedad de **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) es el mismo para los dos objetos. Por ejemplo, si copia de un mensaje, establecer _lpInterface_ a IID_IMessage y el **PR_OBJECT_TYPE** para ambos objetos a MAPI_MESSAGE. 
  
Si se pasa un puntero no válido en el parámetro _lpDestObj_ , los resultados serán impredecibles. 
  
Excluir propiedades en una llamada de **CopyTo** puede ser útil. Por ejemplo, algunos objetos tienen propiedades que son específicas de una sola instancia del objeto, como la fecha y la hora de entrega del mensaje. Para evitar el tiempo de entrega de un mensaje cuando se copia el mensaje a una carpeta diferente de copia, especifique **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) en la matriz de exclusión de etiqueta de propiedad. Para excluir lista de destinatarios de un mensaje, agregue la propiedad **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) a la matriz de exclusión. Para excluir los datos adjuntos de un mensaje, agregue la propiedad **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) a la matriz.
  
De igual forma, evitar que las acciones como copiar o mover de una carpeta o una tabla de contenido o de jerarquía del contenedor de la libreta de direcciones mediante la inclusión de **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) o **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) en la propiedad etiqueta excluir matriz.
  
Para excluir las propiedades de la copia o la operación de movimiento, incluir sus etiquetas de propiedad en el parámetro _lpExcludeProps_ . Si se pasa el resultado de la macro **PROP_TAG** para crear una etiqueta de propiedad de un identificador específico de la matriz de la etiqueta de propiedad, se excluirán todas las propiedades con ese identificador. Por ejemplo, la siguiente entrada en la matriz de la etiqueta de propiedad hace que todas las propiedades con un identificador de 0x8002 que se deben excluir, independientemente del tipo de: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
La etiqueta de propiedad de **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) no se puede incluir en la matriz _lpExcludeProps_ . 
  
La utilidad de la característica de **CopyTo** para excluir interfaces quizás no es tan obvia como la utilidad de exclusión de propiedades. Puede excluir una interfaz cuando se copia a un objeto que no tiene conocimiento de un grupo de propiedades. Por ejemplo, si copia propiedades de una carpeta a un archivo adjunto, las únicas propiedades que los datos adjuntos pueden trabajar con son las propiedades genéricas disponibles con cualquier implementación de [IMAPIProp](imapipropiunknown.md) . Mediante la exclusión de [IMAPIFolder](imapifolderimapicontainer.md) desde la operación de copia, los datos adjuntos no recibirá ninguna de las propiedades de carpeta más específicas. 
  
Cuando se usa el parámetro _rgiidExclude_ para excluir una interfaz, también excluye todas las interfaces derivadas de dicha interfaz. Por ejemplo, excluyendo [IMAPIContainer](imapicontainerimapiprop.md) hace que las carpetas o los contenedores de la libreta de direcciones que se deben excluir, según el tipo de proveedor. No excluya **IMAPIProp** o [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) debido a que muchas interfaces derivan de ellos. 
  
Omitir MAPI_E_COMPUTED devuelven errores en la estructura de **SPropProblemArray** en el parámetro _lppProblems_ . 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadFromMSG  <br/> |MFCMAPI usa el método **IMAPIProp::CopyTo** para copiar las propiedades de un archivo .msg a un objeto [IMAPIMessageSite](imapimessagesiteiunknown.md) .  <br/> |
|FolderDlg.cpp  <br/> |CFolderDlg::HandlePaste  <br/> |MFCMAPI usa el método **IMAPIProp::CopyTo** para copiar las propiedades de un mensaje de origen a un mensaje de destino durante una operación de pegado.  <br/> |
   
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

