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

## <a name="parameters"></a>Parámetros

 _lpIncludeProps_
  
> [entrada] Puntero a una matriz de etiquetas de propiedades que especifica las propiedades que se copian o se mueven. **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) no se puede incluir en la matriz. El _parámetro lpIncludeProps_ no puede ser **nulo.**
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal del indicador de progreso. 
    
 _lpProgress_
  
> [entrada] Puntero a una implementación de un indicador de progreso. Si **se** pasa null en el  _parámetro lpProgress,_ el indicador de progreso se muestra mediante la implementación mapi. El _parámetro lpProgress_ se omite a menos que MAPI_DIALOG marca esté establecida en el _parámetro ulFlags._ 
    
 _lpInterface_
  
> [entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se debe usar para tener acceso al objeto al que apunta el parámetro _lpDestObj._ El _parámetro lpInterface_ no debe ser **nulo.**
    
 _lpDestObj_
  
> [entrada] Puntero al objeto para recibir las propiedades copiadas o movida.
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla la operación de copia o movimiento. Se pueden establecer las siguientes marcas:
    
MAPI_DECLINE_OK 
  
> Si **CopyProps** llama al método [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md) para controlar la operación de copia o movimiento, debería devolverse inmediatamente con el valor de error MAPI_E_DECLINE_COPY. MAPI MAPI_DECLINE_OK marca para limitar la recursión. Los clientes no establecen esta marca. 
    
MAPI_DIALOG 
  
> Muestra un indicador de progreso.
    
MAPI_MOVE 
  
> **CopyProps debe** realizar una operación de movimiento en lugar de una operación de copia. Cuando no se establece esta marca, **CopyProps** realiza una operación de copia. 
    
MAPI_NOREPLACE 
  
> Las propiedades existentes en el objeto de destino no deben sobrescribirse. Cuando no se establece esta marca, **CopyProps** sobrescribe las propiedades existentes. 
    
 _lppProblems_
  
> [entrada, salida] En la entrada, un puntero a un puntero a una [estructura SPropProblemArray;](spropproblemarray.md) de lo **contrario, null**, que indica que no es necesario obtener información de error. Si  _lppProblems_ es un puntero válido en la entrada, **CopyProps** devuelve información detallada acerca de los errores al copiar una o más propiedades. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las propiedades se han copiado o movido correctamente.
    
MAPI_E_COLLISION 
  
> No se puede copiar un subobjeto porque un subobjeto con el mismo nombre para mostrar, definido por la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), ya existe en el objeto de destino. 
    
MAPI_E_DECLINE_COPY 
  
> El proveedor de servicios no implementa la operación de copia.
    
MAPI_E_FOLDER_CYCLE 
  
> El objeto de origen que realiza la operación de copia o movimiento directa o indirectamente contiene el objeto de destino. Es posible que se haya realizado un trabajo significativo antes de que se detectara esta condición, por lo que los objetos de origen y destino podrían modificarse parcialmente. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> La interfaz identificada por el  _parámetro lpInterface_ no es compatible con el objeto de destino. 
    
MAPI_E_NO_ACCESS 
  
> Se intentó obtener acceso a un objeto para el que el autor de la llamada no tiene permisos suficientes. Este error se devuelve si el objeto de destino es el mismo que el objeto de origen.
    
Los siguientes valores se pueden devolver en la **estructura SPropProblemArray,** pero no como valores **devueltos para CopyProps**. Estos errores se aplican a una sola propiedad.
  
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció MAPI_UNICODE marca y **CopyProps** no admite Unicode o MAPI_UNICODE no se estableció **y CopyProps** solo admite Unicode. 
    
MAPI_E_COMPUTED 
  
> El autor de la llamada no puede modificar la propiedad porque es una propiedad de solo lectura, calculada por el propietario del objeto de destino. Este error no es grave; el autor de la llamada debe permitir que continúe la operación de copia.
    
MAPI_E_INVALID_TYPE 
  
> El tipo de propiedad no es válido.
    
MAPI_E_UNEXPECTED_TYPE 
  
> El tipo de propiedad no es el tipo esperado por el autor de la llamada.
    
## <a name="remarks"></a>Comentarios

El **método IMAPIProp::CopyProps** copia o mueve las propiedades seleccionadas del objeto actual a un objeto de destino. **CopyProps se** usa principalmente para responder y reenviar mensajes, donde solo algunas de las propiedades del mensaje original viajan con la respuesta o la copia reenviada. 
  
Los subobjetos del objeto de origen se incluyen automáticamente en la operación y se copian o mueven en su totalidad, independientemente del uso de las propiedades indicadas por la estructura [SPropTagArray.](sproptagarray.md) De forma predeterminada, **CopyProps** sobrescribe las propiedades del objeto de destino que coinciden con las propiedades del objeto de origen. Si alguna de las propiedades copiadas o movida ya existe en el objeto de destino, las propiedades existentes se sobrescriben mediante las nuevas propiedades, a menos que la marca MAPI_NOREPLACE esté establecida en el parámetro _ulFlags._ La información existente en el objeto de destino que no se sobrescribe se deja sin tocar. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Puede proporcionar una implementación completa de **CopyProps** o confiar en la implementación que MAPI proporciona en su objeto de compatibilidad. Si desea usar la implementación MAPI, llame al **método IMAPISupport::D oCopyProps.** Sin embargo, si delega el procesamiento en **DoCopyProps** y se le pasa la marca MAPI_DECLINE_OK, evite la llamada de soporte técnico y devuelva MAPI_E_DECLINE_COPY en su lugar. MAPI le llamará con esta marca para evitar la posible recursión que puede producirse al copiar carpetas. 
  
Dado que la operación de copia puede ser larga, debe mostrar un indicador de progreso. Use la [implementación imapiprogress](imapiprogressiunknown.md) que se pasa en el parámetro  _lpProgress,_ si hay alguno. Si  _lpProgress_ es **nulo,** llame al método [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) para usar la implementación mapi. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

No establezca la marca MAPI_DECLINE_OK; MAPI lo usa en sus llamadas a implementaciones **copyProps** del proveedor de almacén de mensajes. 
  
Dado que las operaciones de copiar y mover pueden tardar tiempo, es aconsejable solicitar la visualización de un indicador de progreso estableciendo la marca MAPI_DIALOG progreso. Puede establecer el parámetro  _lpProgress_ en la implementación de **IMAPIProgress**, si tiene uno, o en **null**. Si  _lpProgress es_ **nulo,** **CopyProps** usará el indicador de progreso predeterminado proporcionado por MAPI. 
  
Puedes suprimir la presentación de un indicador de progreso si no estableces la MAPI_DIALOG indicador. **CopyProps omitirá** los  _parámetros ulUIParam_ y  _lpProgress_ y evitará mostrar el indicador. 
  
 **CopyProps puede** notificar errores globales e individuales, o errores que se producen con una o varias de las propiedades. Estos errores individuales se ponen en una **estructura SPropProblemArray.** Puede suprimir los informes de errores en el nivel de propiedad pasando **null**, en lugar de un puntero válido, para el parámetro de estructura de la matriz de problemas de propiedad. 
  
Si desea recibir información sobre errores, pase un puntero de estructura **SPropProblemArray** válido en el parámetro _lppProblems._ Cuando **CopyProps** devuelve S_OK, compruebe si hay errores posibles con propiedades individuales en la estructura. Cuando **CopyProps devuelve** un error, no se devuelve información en la **estructura SPropProblemArray.** En su lugar, llame [al método IMAPIProp::GetLastError](imapiprop-getlasterror.md) para recuperar información detallada del error. 
  
Si **CopyProps** devuelve S_OK, libera la estructura **SPropProblemArray** devuelta llamando a la [función MAPIFreeBuffer.](mapifreebuffer.md) 
  
Si va a copiar propiedades que son exclusivas del tipo de objeto de origen, debe asegurarse de que el objeto de destino es del mismo tipo. **CopyProps** no impide asociar propiedades que normalmente pertenecen a un tipo de objeto con otro tipo de objeto. Es usted el que debe copiar las propiedades que tienen sentido para el objeto de destino. Por ejemplo, no debe copiar las propiedades del mensaje en un contenedor de libreta de direcciones. 
  
Para asegurarse de que está copiando entre objetos del mismo tipo, compruebe que el objeto de origen y de destino sean del mismo tipo, ya sea comparando punteros de objeto o llamando al método [IUnknown::QueryInterface.](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) Establece el identificador de interfaz al que  _apunta lpInterface_ en la interfaz estándar para el objeto de origen. Asegúrese también de que el tipo de **objeto o PR_OBJECT_TYPE** propiedad ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) sea la misma para los dos objetos. Por ejemplo, si va a copiar desde un mensaje, establezca  _lpInterface_ en IID_IMessage y el PR_OBJECT_TYPE para ambos objetos en MAPI_MESSAGE. 
  
Si se pasa un puntero no válido en el  _parámetro lpDestObj,_ los resultados son impredecibles. 
  
Para copiar la lista de destinatarios de un mensaje, llame al método **CopyProps** del mensaje e incluya la propiedad **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) en la matriz de etiquetas de propiedad. Para copiar los datos adjuntos del mensaje, incluya **la PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). 
  
Para copiar la jerarquía o la tabla de contenido de un contenedor de carpeta o libreta de direcciones, incluya las propiedades **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) o **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) en la matriz de etiquetas de propiedades. Para incluir la tabla de contenido asociada de una carpeta, incluya la propiedad **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) en la matriz. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyNamedProps  <br/> |MFCMAPI usa el **método IMAPIProp::CopyProps** para copiar propiedades con nombre de un mensaje a otro.  <br/> |
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::OnPasteProperty  <br/> |MFCMAPI usa el **método IMAPIProp::CopyProps** para pegar una propiedad que se ha copiado de otro objeto.  <br/> |
   
## <a name="see-also"></a>Consulte también



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

