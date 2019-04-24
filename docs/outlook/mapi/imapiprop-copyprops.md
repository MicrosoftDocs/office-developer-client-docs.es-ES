---
title: IMAPIPropCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyProps
api_type:
- COM
ms.assetid: f65da1c8-d49b-44e8-8c66-9c53d088d334
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7319f1abb4a74ee17b0a4a1220215c29434d256b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345510"
---
# <a name="imapipropcopyprops"></a>IMAPIProp::CopyProps

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Copia o mueve las propiedades seleccionadas. 
  
```cpp
HRESULT CopyProps(
  LPSPropTagArray lpIncludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parameters

 _lpIncludeProps_
  
> a Un puntero a una matriz de etiquetas de propiedad que especifica las propiedades que se deben copiar o mover. **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) no se puede incluir en la matriz. El parámetro _lpIncludeProps_ no puede ser **nulo**.
    
 _ulUIParam_
  
> a Identificador de la ventana primaria del indicador de progreso. 
    
 _lpProgress_
  
> a Un puntero a una implementación de un indicador de progreso. Si se pasa **null** en el parámetro _lpProgress_ , se muestra el indicador de progreso mediante la implementación de MAPI. El parámetro _lpProgress_ se omite a menos que se establezca la marca MAPI_DIALOG en el parámetro _ulFlags_ . 
    
 _lpInterface_
  
> a Un puntero al identificador de interfaz (IID) que representa la interfaz que se debe usar para obtener acceso al objeto al que apunta el parámetro _lpDestObj_ . El parámetro _lpInterface_ no debe ser **nulo**.
    
 _lpDestObj_
  
> a Un puntero al objeto que va a recibir las propiedades que se han copiado o movido.
    
 _ulFlags_
  
> a Una máscara de máscara de marcadores que controla la operación de copiar o mover. Se pueden establecer los siguientes indicadores:
    
MAPI_DECLINE_OK 
  
> Si **CopyProps** llama al método [IMAPISupport::D ocopyprops](imapisupport-docopyprops.md) para controlar la operación de copia o movimiento, en su lugar debe volver inmediatamente con el valor de error MAPI_E_DECLINE_COPY. MAPI establece la marca MAPI_DECLINE_OK para limitar la recursividad. Los clientes no establecen esta marca. 
    
MAPI_DIALOG 
  
> Muestra un indicador de progreso.
    
MAPI_MOVE 
  
> **CopyProps** debe realizar una operación de movimiento en lugar de una operación de copia. Cuando no se establece este indicador, **CopyProps** realiza una operación de copia. 
    
MAPI_NOREPLACE 
  
> Las propiedades existentes en el objeto de destino no se deben sobrescribir. Cuando no se establece este indicador, **CopyProps** sobrescribe las propiedades existentes. 
    
 _lppProblems_
  
> [in, out] En la entrada, un puntero a un puntero a una estructura [SPropProblemArray](spropproblemarray.md) ; de lo contrario, **null**, que indica que no se necesita información de error. Si _lppProblems_ es un puntero válido en la entrada, **CopyProps** devuelve información detallada sobre los errores al copiar una o más propiedades. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las propiedades se han copiado o movido correctamente.
    
MAPI_E_COLLISION 
  
> No se puede copiar un subobjeto porque ya existe un subobjeto con el mismo nombre para mostrar, definido por la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), en el objeto de destino. 
    
MAPI_E_DECLINE_COPY 
  
> El proveedor de servicios no implementa la operación de copia.
    
MAPI_E_FOLDER_CYCLE 
  
> El objeto de origen que realiza la operación de copia o movimiento contiene directa o indirectamente el objeto de destino. Es posible que se haya realizado un trabajo significativo antes de que se detectara esta condición, por lo que los objetos de origen y de destino podrían modificarse parcialmente. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> La interfaz identificada por el parámetro _lpInterface_ no es compatible con el objeto de destino. 
    
MAPI_E_NO_ACCESS 
  
> Se intentó obtener acceso a un objeto para el que el autor de la llamada no tiene permisos suficientes. Este error se devuelve si el objeto de destino es el mismo que el objeto de origen.
    
Los valores siguientes se pueden devolver en la estructura **SPropProblemArray** , pero no como valores devueltos para **CopyProps**. Estos errores se aplican a una sola propiedad.
  
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció la marca MAPI_UNICODE y **CopyProps** no admite Unicode, o bien no se estableció MAPI_UNICODE y **CopyProps** solo admite Unicode. 
    
MAPI_E_COMPUTED 
  
> La propiedad no la puede modificar el autor de la llamada porque es una propiedad de solo lectura, calculada por el propietario del objeto de destino. Este error no es grave; el autor de la llamada debe permitir que continúe la operación de copia.
    
MAPI_E_INVALID_TYPE 
  
> El tipo de propiedad no es válido.
    
MAPI_E_UNEXPECTED_TYPE 
  
> El tipo de propiedad no es el tipo que espera el autor de la llamada.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIProp:: CopyProps** copia o mueve las propiedades seleccionadas del objeto actual a un objeto de destino. **CopyProps** se usa principalmente para responder y reenviar mensajes, donde solo algunas de las propiedades del mensaje original viajan con la copia de respuesta o reenviada. 
  
Todos los subobjetos del objeto de origen se incluyen automáticamente en la operación y se copian o se mueven en su totalidad, independientemente del uso de las propiedades indicadas por la estructura [SPropTagArray](sproptagarray.md) . De forma predeterminada, **CopyProps** sobrescribe las propiedades del objeto de destino que coinciden con las propiedades del objeto de origen. Si alguna de las propiedades que se han copiado o movido ya existe en el objeto de destino, las propiedades existentes se sobrescriben con las nuevas propiedades, a menos que la marca MAPI_NOREPLACE se establezca en el parámetro _ulFlags_ . La información existente en el objeto de destino que no se sobrescribe permanece inalterada. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Puede proporcionar una implementación completa de **CopyProps** o confiar en la implementación que proporciona MAPI en su objeto de soporte. Si desea usar la implementación de MAPI, llame al método **IMAPISupport::D ocopyprops** . Sin embargo, si realiza el procesamiento de delegado en **DoCopyProps** y se le pasa la marca MAPI_DECLINE_OK, evite la llamada de soporte técnico y devuelva MAPI_E_DECLINE_COPY en su lugar. Se le llamará con este indicador mediante MAPI para evitar la posible recursividad que puede producirse al copiar carpetas. 
  
Como la operación de copia puede ser prolongada, debe mostrar un indicador de progreso. Use la implementación de [método imapiprogress](imapiprogressiunknown.md) que se pasa en el parámetro _lpProgress_ , si hay alguno. Si _lpProgress_ es **null**, llame al método [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) para usar la implementación de MAPI. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

No establezca la marca MAPI_DECLINE_OK; MAPI la usa en sus llamadas a las implementaciones de **CopyProps** del proveedor de almacenamiento de mensajes. 
  
Como las operaciones de copiar y mover pueden tardar algún tiempo, es aconsejable solicitar la presentación de un indicador de progreso mediante la configuración de la marca MAPI_DIALOG. Puede establecer el parámetro _lpProgress_ en su implementación de **método imapiprogress**, si tiene uno, o en **null**. Si _lpProgress_ es **null**, **CopyProps** usará el indicador de progreso predeterminado proporcionado por MAPI. 
  
Puede suprimir la presentación de un indicador de progreso si no se configura la marca MAPI_DIALOG. **CopyProps** omitirá los parámetros _ulUIParam_ y _lpProgress_ y evitará que se muestre el indicador. 
  
 **CopyProps** puede informar de errores globales y individuales, o errores que se producen con una o varias de las propiedades. Estos errores individuales se colocan en una estructura **SPropProblemArray** . Puede suprimir los informes de errores en el nivel de propiedad pasando **null**, en lugar de un puntero válido, para el parámetro de estructura de matriz con problemas de propiedad. 
  
Si desea recibir información sobre los errores, pase un puntero de estructura **SPropProblemArray** válido en el parámetro _lppProblems_ . Cuando **CopyProps** Devuelve S_OK, compruebe si hay posibles errores con propiedades individuales en la estructura. Cuando **CopyProps** devuelve un error, no se devuelve información en la estructura **SPropProblemArray** . En su lugar, llame al método [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) para recuperar información detallada del error. 
  
Si **CopyProps** Devuelve S_OK, libere la estructura **SPropProblemArray** devuelta llamando a la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Si va a copiar propiedades que son exclusivas del tipo de objeto de origen, debe asegurarse de que el objeto de destino es del mismo tipo. **CopyProps** no impide que se asocien propiedades que, por lo general, pertenecen a un tipo de objeto con otro tipo de objeto. El usuario debe copiar las propiedades que tengan sentido para el objeto de destino. Por ejemplo, no debe copiar las propiedades de los mensajes en un contenedor de libretas de direcciones. 
  
Para asegurarse de que está copiando objetos del mismo tipo, compruebe que el objeto de origen y el de destino son el mismo tipo, ya sea comparando los punteros de objeto o llamando al método [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) . Establezca el identificador de interfaz al que apunta _lpInterface_ en la interfaz estándar del objeto de origen. Además, asegúrese de que el tipo de objeto o la propiedad **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) es la misma para los dos objetos. Por ejemplo, si copia de un mensaje, establezca _lpInterface_ en IID_IMessage y el **PR_OBJECT_TYPE** para ambos objetos en MAPI_MESSAGE. 
  
Si se pasa un puntero no válido en el parámetro _lpDestObj_ , los resultados son imprevisibles. 
  
Para copiar la lista de destinatarios de un mensaje, llame al método **CopyProps** del mensaje e incluya la propiedad **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) en la matriz de etiquetas de propiedades. Para copiar los datos adjuntos del mensaje, incluya la propiedad **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). 
  
Para copiar una carpeta o una tabla de contenido o jerarquía de contenedor de libreta de direcciones, incluya las propiedades **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) o **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) en el matriz de etiquetas de propiedades. Para incluir la tabla Contents asociada de una carpeta, incluya la propiedad **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) en la matriz. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |CopyNamedProps  <br/> |MFCMAPI usa el método **IMAPIProp:: CopyProps** para copiar las propiedades con nombre de un mensaje a otro.  <br/> |
|SingleMAPIPropListCtrl. cpp  <br/> |CSingleMAPIPropListCtrl:: OnPasteProperty  <br/> |MFCMAPI usa el método **IMAPIProp:: CopyProps** para pegar una propiedad que se ha copiado de otro objeto.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::CopyTo](imapiprop-copyto.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)
  
[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propiedad canónica PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[Propiedad canónica PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[Propiedad canónica PidTagDisplayName](pidtagdisplayname-canonical-property.md)
  
[Propiedad canónica PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)
  
[Propiedad canónica PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)
  
[Propiedad canónica PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[Propiedad canónica PidTagObjectType](pidtagobjecttype-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

