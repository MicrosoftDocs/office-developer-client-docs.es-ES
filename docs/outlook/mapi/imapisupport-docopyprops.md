---
title: IMAPISupportDoCopyProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyProps
api_type:
- COM
ms.assetid: 2446ef52-578a-4004-9719-de9b0207ccad
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 24107ae1926c8590da6a823a354eeae72d72f248
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405586"
---
# <a name="imapisupportdocopyprops"></a>IMAPISupport::DoCopyProps

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Copia o mueve una o varias propiedades de un objeto a otro objeto.
  
```cpp
HRESULT DoCopyProps(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  LPSPropTagArray lpIncludeProps,
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
  
> [entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para tener acceso al objeto con las propiedades que se van a copiar o mover.
    
 _lpSrcObj_
  
> [entrada] Puntero al objeto que contiene las propiedades que se van a copiar o mover.
    
 _lpIncludeProps_
  
> [entrada] Puntero a una estructura [SPropTagArray](sproptagarray.md) que contiene una matriz contada de etiquetas de propiedad que indican las propiedades que se copian o se mueven. El  _parámetro lpIncludeProps_ no puede ser NULL. 
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal del indicador de progreso.
    
 _lpProgress_
  
> [entrada] Puntero a una implementación de un indicador de progreso. Si se pasa NULL en el  _parámetro lpProgress,_ el indicador de progreso se muestra mediante la implementación mapi. El _parámetro lpProgress_ se omite a menos que MAPI_DIALOG marca esté establecida en el _parámetro ulFlags._ 
    
 _lpDestInterface_
  
> [entrada] Puntero al identificador de interfaz que representa la interfaz que se va a usar para tener acceso al objeto y recibir las propiedades que se copian o mueven.
    
 _lpDestObj_
  
> [entrada] Puntero al objeto para recibir las propiedades copiadas o movida.
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla cómo se realiza la operación de copia o movimiento. Se pueden establecer las siguientes marcas:
    
MAPI_DIALOG 
  
> Muestra un indicador de progreso.
    
MAPI_MOVE 
  
> **DoCopyProps debe** realizar una operación de movimiento en lugar de una operación de copia. Cuando no se establece esta marca, **DoCopyProps** realiza una operación de copia. 
    
MAPI_NOREPLACE 
  
> Las propiedades existentes en el objeto de destino no deben sobrescribirse. Cuando no se establece esta marca, **DoCopyProps** sobrescribe las propiedades existentes. 
    
 _lppProblems_
  
> [entrada, salida] En la entrada, un puntero a un puntero a una [estructura SPropProblemArray;](spropproblemarray.md) de lo contrario, NULL, que indica que no es necesario obtener información de error. Si  _lppProblems_ es un puntero válido en la entrada, **DoCopyProps** devuelve información detallada acerca de los errores al copiar una o más propiedades. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las propiedades se copiaron o se movieron correctamente.
    
MAPI_E_COLLISION 
  
> Ya existe una propiedad que se va a copiar o mover en el objeto de destino y se MAPI_NOREPLACE marca. 
    
MAPI_E_FOLDER_CYCLE 
  
> El objeto de origen contiene directa o indirectamente el objeto de destino. Es posible que se haya realizado un trabajo significativo antes de que se detectara esta condición, por lo que los objetos de origen y destino podrían modificarse parcialmente. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> La interfaz identificada por el parámetro  _lpSrcInterface_ no es compatible con el objeto de origen o la interfaz identificada por el parámetro  _lpDestInterface_ no es compatible con el objeto de destino. 
    
MAPI_E_NO_ACCESS 
  
> Se intentó obtener acceso a un objeto para el que el autor de la llamada no tiene permisos suficientes. Este error se devuelve si el objeto de destino es el mismo que el objeto de origen.
    
Los siguientes valores se pueden devolver en la estructura **SPropProblemArray,** pero no como valores devueltos para **DoCopyProps**. Estos errores se aplican a una sola propiedad.
  
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció MAPI_UNICODE marca y **DoCopyProps** no admite Unicode o MAPI_UNICODE no se estableció y **DoCopyProps** solo admite Unicode. 
    
MAPI_E_COMPUTED 
  
> El autor de la llamada no puede modificar la propiedad porque es una propiedad de solo lectura, calculada por el propietario del objeto de destino. Este error no es grave; el autor de la llamada debe permitir que continúe la operación de copia.
    
MAPI_E_INVALID_TYPE 
  
> El tipo de propiedad no es válido.
    
MAPI_E_UNEXPECTED_TYPE 
  
> El tipo de propiedad no es el tipo que espera el autor de la llamada.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::D oCopyProps** se implementa para objetos de compatibilidad del proveedor de almacenamiento de mensajes. Los proveedores de almacenamiento de mensajes pueden llamar **a DoCopyProps** para implementar el método [IMAPIProp::CopyProps](imapiprop-copyprops.md) para sus carpetas y mensajes. **DoCopyProps** copia o mueve las propiedades identificadas en la matriz de etiquetas de propiedades a las que apunta  _lpIncludeProps_ y que están presentes en el objeto al que apunta  _lpSrcObj_. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Al copiar propiedades entre objetos del mismo tipo, como dos mensajes, los parámetros  _lpSrcInterface_ y  _lpDestInterface_ deben contener el mismo identificador de interfaz y los parámetros  _lpSrcObj_ y  _lpDestObj_ deben apuntar a objetos del mismo tipo. Si  _lpDestInterface_ se establece en NULL, **DoCopyProps** devuelve MAPI_E_INVALID_PARAMETER. Si establece  _lpDestInterface_ en un identificador de interfaz aceptable, pero  _establece lpDestObj_ en un puntero no válido, los resultados son impredecibles. Lo más probable es que el proveedor falle. 
  
Establezca la MAPI_NOREPLACE si no desea que se sobrescriba ninguna de las propiedades del objeto de destino. Las propiedades del objeto de destino que existen en el objeto de origen y que no se sobrescriben no se eliminan ni modifican.
  
Para copiar la lista de destinatarios de un mensaje, incluya la propiedad **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) en la matriz de etiquetas de propiedad a la que apunta el parámetro _lpIncludeProps._ Para copiar los datos adjuntos del mensaje, incluya **la PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). 
  
Para copiar la jerarquía o la tabla de contenido de un contenedor de carpeta o libreta de direcciones, incluya **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) o **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) en la matriz de etiquetas de propiedades. Para incluir la tabla de contenido asociada de una carpeta, incluya la propiedad **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) en la matriz.
  
Si se copian o mueven subcarpetas, su contenido se copia o mueve en su totalidad, independientemente del uso de las propiedades indicadas por la estructura **SPropTagArray.** 
  
 **DoCopyProps notifica** los errores globales que se producen con la operación en su totalidad y los errores individuales que se producen con una o varias de las propiedades. Estos errores individuales se ponen en una **estructura SPropProblemArray.** Puede suprimir los informes de errores en el nivel de propiedad pasando NULL, en lugar de un puntero válido, para el parámetro de estructura de la matriz de problemas de propiedad. 
  
Si desea recibir información sobre errores, pase un puntero de estructura **SPropProblemArray** válido en el parámetro _lppProblems._ Cuando **DoCopyProps** devuelve S_OK, compruebe si hay errores posibles con propiedades individuales en la estructura. Cuando **DoCopyProps devuelve** un error, no se devuelve información en la **estructura SPropProblemArray.** En su lugar, llame [al método IMAPISupport::GetLastError](imapisupport-getlasterror.md) para recuperar información detallada del error. 
  
Si **DoCopyProps devuelve** S_OK, libera la estructura **SPropProblemArray** devuelta llamando a la [función MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="see-also"></a>Consulte también



[IMAPIProp::CopyProps](imapiprop-copyprops.md)
  
[IMAPISupport::CopyMessages](imapisupport-copymessages.md)
  
[IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[Propiedad canónica PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[Propiedad canónica PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[Propiedad canónica PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)
  
[Propiedad canónica PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)
  
[Propiedad canónica PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

