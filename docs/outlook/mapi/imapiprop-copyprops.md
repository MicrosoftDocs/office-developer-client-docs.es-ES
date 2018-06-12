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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: ff8f13a1dcf678e1d05b6e8e083597156422b83d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817422"
---
# <a name="imapipropcopyprops"></a>IMAPIProp::CopyProps

  
  
**Se aplica a**: Outlook 
  
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

## <a name="parameters"></a>Sintaxis

 _lpIncludeProps_
  
> [entrada] Un puntero a una matriz de etiqueta de propiedad que especifica las propiedades para copiar o mover. **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) no se puede incluir en la matriz. El parámetro _lpIncludeProps_ no puede ser **null**.
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal del indicador de progreso. 
    
 _lpProgress_
  
> [entrada] Un puntero a una implementación de un indicador de progreso. Si se pasa **null** en el parámetro _lpProgress_ , se muestra el indicador de progreso mediante el uso de la implementación de MAPI. El parámetro _lpProgress_ se omite a menos que la marca MAPI_DIALOG se establece en el parámetro _ulFlags indicado_ . 
    
 _lpInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se debe utilizar para tener acceso al objeto al que apunta el parámetro _lpDestObj_ . El parámetro _lpInterface_ no debe ser **null**.
    
 _lpDestObj_
  
> [entrada] Un puntero al objeto que se va a recibir las propiedades que se ha movido o copiadas.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla la operación de copiar o mover. Se pueden establecer los siguientes indicadores:
    
MAPI_DECLINE_OK 
  
> Si **CopyProps** se llama al método de [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) para controlar la copia o la operación de movimiento, debe en su lugar devolver inmediatamente con el valor de error MAPI_E_DECLINE_COPY. Para limitar la recursividad, se establece la marca MAPI_DECLINE_OK de MAPI. Los clientes no establezca esta marca. 
    
MAPI_DIALOG 
  
> Muestra un indicador de progreso.
    
MAPI_MOVE 
  
> **CopyProps** debe realizar una operación de movimiento en lugar de una operación de copia. Cuando no se establece este marcador, **CopyProps** realiza una operación de copia. 
    
MAPI_NOREPLACE 
  
> No se deben sobrescribir las propiedades existentes en el objeto de destino. Cuando no se establece este marcador, **CopyProps** sobrescribe las propiedades existentes. 
    
 _lppProblems_
  
> [entrada, salida] En la entrada, un puntero a un puntero a una estructura [SPropProblemArray](spropproblemarray.md) ; en caso contrario, **null**, que indica que no es necesario para obtener información de error. Si _lppProblems_ es un puntero válido en la entrada, **CopyProps** devuelve información detallada acerca de los errores de copiar una o más propiedades. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las propiedades se hayan copiado o movido correctamente.
    
MAPI_E_COLLISION 
  
> No se puede copiar un subobjetos porque ya existe un subobjetos con el mismo nombre para mostrar, definido por la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), en el objeto de destino. 
    
MAPI_E_DECLINE_COPY 
  
> El proveedor de servicios no implementa la operación de copia.
    
MAPI_E_FOLDER_CYCLE 
  
> El objeto de origen a realizar la operación de copiar o mover directa o indirectamente contiene el objeto de destino. Trabajo significativo es posible que se han realizado antes de que se ha detectado esta condición, por lo que los objetos de origen y de destino podrían modificarse parcialmente. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> La interfaz identificada mediante el parámetro _lpInterface_ no es compatible con el objeto de destino. 
    
MAPI_E_NO_ACCESS 
  
> Se ha intentado tener acceso a un objeto para el que el autor de la llamada no tiene permisos suficientes. Este error se devuelve si el objeto de destino es el mismo que el objeto de origen.
    
Los siguientes valores se pueden devolver en la estructura de **SPropProblemArray** , pero no como valores devueltos por **CopyProps**. Estos errores se aplican a una sola propiedad.
  
MAPI_E_BAD_CHARWIDTH 
  
> Se ha establecido el indicador MAPI_UNICODE y **CopyProps** no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y **CopyProps** admite sólo Unicode. 
    
MAPI_E_COMPUTED 
  
> La propiedad no puede modificarse el autor de la llamada porque es una propiedad de solo lectura, calculada por el propietario del objeto de destino. Este error no es grave; el autor de la llamada debe permitir que la operación de copia continuar.
    
MAPI_E_INVALID_TYPE 
  
> El tipo de propiedad no es válido.
    
MAPI_E_UNEXPECTED_TYPE 
  
> El tipo de propiedad no es el tipo esperado por el autor de la llamada.
    
## <a name="remarks"></a>Notas

El método **IMAPIProp::CopyProps** copia o mueve las propiedades seleccionadas del objeto actual en un objeto de destino. **CopyProps** se usa principalmente para responder y reenviar los mensajes, donde solo algunas de las propiedades del mensaje original de viajes con la respuesta o reenvían copia. 
  
Los objetos secundarios en el objeto de origen automáticamente se incluyen en la operación y copiados o movidos en su totalidad, independientemente del uso de las propiedades indicado por la estructura del [elemento SPropTagArray](sproptagarray.md) . De forma predeterminada, **CopyProps** sobrescribe cualquier propiedades en el objeto de destino que coinciden con las propiedades del objeto de origen. Si cualquiera de las propiedades que se ha movido o copiadas ya existe en el objeto de destino, se sobrescriben las propiedades existentes por las nuevas propiedades, a menos que se establece la marca MAPI_NOREPLACE en el parámetro _ulFlags indicado_ . Información existente en el objeto de destino que no se sobrescribe se toca. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Puede proporcionar una implementación completa de **CopyProps** o se basan en la implementación que proporciona MAPI en su objeto de soporte técnico. Si desea utilizar la implementación de MAPI, llame al método **IMAPISupport::DoCopyProps** . Sin embargo, si delegar procesamiento a **DoCopyProps** y se pasa el indicador MAPI_DECLINE_OK, evitar la llamada de soporte técnico y devolver MAPI_E_DECLINE_COPY en su lugar. Se le llamará con esta marca de MAPI para evitar la recursividad posible que puede surgir al copiar las carpetas. 
  
Debido a que la operación de copia puede ser prolongada, debe mostrar un indicador de progreso. Utilice la implementación de [IMAPIProgress](imapiprogressiunknown.md) que se pasa en el parámetro _lpProgress_ , si hay alguno. Si _lpProgress_ es **null**, llame al método [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) para usar la implementación de MAPI. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

No se establece la marca MAPI_DECLINE_OK; se usa para MAPI en sus llamadas a las implementaciones de **CopyProps** del proveedor de almacén de mensajes. 
  
Debido a que las operaciones de copia y movimiento pueden tomar tiempo, es conveniente solicitar la visualización de un indicador de progreso estableciendo el indicador MAPI_DIALOG. Puede establecer el parámetro _lpProgress_ a la implementación de **IMAPIProgress**, si dispone de uno, o en **null**. Si _lpProgress_ es **null**, **CopyProps** usará el indicador de progreso predeterminada proporcionado por MAPI. 
  
Puede suprimir la visualización de un indicador de progreso no establecer el indicador MAPI_DIALOG. **CopyProps** omitirá los parámetros _ulUIParam_ y _lpProgress_ y evitar que se muestre el indicador. 
  
 **CopyProps** puede informar errores globales e individuales o errores que se producen con una o varias de las propiedades. Estos errores individuales se colocan en una estructura **SPropProblemArray** . Puede suprimir informes en el nivel de propiedad pasando **null**, en lugar de un puntero válido para el parámetro de estructura de matriz de propiedad problema de error. 
  
Si desea recibir información acerca de los errores, pase un puntero de estructura **SPropProblemArray** válido en el parámetro _lppProblems_ . Cuando **CopyProps** devuelve S_OK, comprobar los posibles errores con las propiedades individuales de la estructura de. Cuando **CopyProps** devuelve un error, no se devuelve información de la estructura de **SPropProblemArray** . En su lugar, llame al método de [IMAPIProp::GetLastError](imapiprop-getlasterror.md) para recuperar información detallada del error. 
  
Si **CopyProps** devuelve S_OK, liberar la estructura **SPropProblemArray** devuelta por una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Si va a copiar las propiedades que son únicas para el tipo de objeto de origen, debe asegurarse de que el objeto de destino es del mismo tipo. **CopyProps** impedir asociar propiedades que normalmente pertenecen a un tipo de objeto con otro tipo de objeto. Depende de usted para copiar las propiedades que tienen sentido para el objeto de destino. Por ejemplo, no debe copiar las propiedades del mensaje a un contenedor de la libreta de direcciones. 
  
Para asegurarse de que está copiando entre objetos del mismo tipo, compruebe que el objeto de origen y de destino son el mismo tipo, ya sea mediante la comparación de punteros a objetos o llamar al método [IUnknown:: QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) . Establecer el identificador de interfaz que señala _lpInterface_ a la interfaz estándar para el objeto de origen. Además, asegúrese de que el tipo de objeto o la propiedad de **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) es el mismo para los dos objetos. Por ejemplo, si va a copiar un mensaje, establecer _lpInterface_ a IID_IMessage y el **PR_OBJECT_TYPE** para ambos objetos a MAPI_MESSAGE. 
  
Si se pasa un puntero no válido en el parámetro _lpDestObj_ , los resultados serán impredecibles. 
  
Para copiar la lista de destinatarios de un mensaje, llamar al método **CopyProps** del mensaje e incluya la propiedad **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) en la matriz de la etiqueta de propiedad. Para copiar los datos adjuntos del mensaje, incluir la propiedad **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). 
  
Para copiar una carpeta o la jerarquía del contenedor de la libreta de direcciones o la tabla de contenido, que incluyen el **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) o las propiedades de **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) en el matriz de la etiqueta de propiedad. Para incluir la tabla de contenido asociada de una carpeta, incluya la propiedad **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) en la matriz. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyNamedProps  <br/> |MFCMAPI usa el método **IMAPIProp::CopyProps** para copiar las propiedades con nombre de un mensaje a otro.  <br/> |
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::OnPasteProperty  <br/> |MFCMAPI utiliza el método **IMAPIProp::CopyProps** para pegar una propiedad que se ha copiado desde otro objeto.  <br/> |
   
## <a name="see-also"></a>Ver también



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPIProgress: IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::CopyTo](imapiprop-copyto.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)
  
[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propiedad canónico PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[Propiedad canónico PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[Propiedad canónico PidTagDisplayName](pidtagdisplayname-canonical-property.md)
  
[Propiedad canónico PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)
  
[Propiedad canónico PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)
  
[Propiedad canónico PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[Propiedad canónico PidTagObjectType](pidtagobjecttype-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[Elemento SPropTagArray](sproptagarray.md)
  
[IMAPIProp: IUnknown](imapipropiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

