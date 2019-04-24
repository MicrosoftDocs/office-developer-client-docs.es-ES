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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322368"
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

## <a name="parameters"></a>Parameters

 _lpSrcInterface_
  
> a Un puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso al objeto con las propiedades que se van a copiar o mover.
    
 _lpSrcObj_
  
> a Un puntero al objeto que contiene las propiedades que se van a copiar o mover.
    
 _lpIncludeProps_
  
> a Un puntero a una estructura [SPropTagArray](sproptagarray.md) que contiene una matriz contada de etiquetas de propiedades que indican las propiedades que se deben copiar o mover. El parámetro _lpIncludeProps_ no puede ser nulo. 
    
 _ulUIParam_
  
> a Identificador de la ventana primaria del indicador de progreso.
    
 _lpProgress_
  
> a Un puntero a una implementación de un indicador de progreso. Si se pasa NULL en el parámetro _lpProgress_ , se muestra el indicador de progreso mediante la implementación de MAPI. El parámetro _lpProgress_ se omite a menos que se establezca la marca MAPI_DIALOG en el parámetro _ulFlags_ . 
    
 _lpDestInterface_
  
> a Puntero al identificador de interfaz que representa la interfaz que se va a utilizar para tener acceso al objeto para recibir las propiedades que se copian o se mueven.
    
 _lpDestObj_
  
> a Un puntero al objeto que va a recibir las propiedades que se han copiado o movido.
    
 _ulFlags_
  
> a Una máscara de máscara de marcadores que controla cómo se realiza la operación de copiar o mover. Se pueden establecer los siguientes indicadores:
    
MAPI_DIALOG 
  
> Muestra un indicador de progreso.
    
MAPI_MOVE 
  
> **DoCopyProps** debe realizar una operación de movimiento en lugar de una operación de copia. Cuando no se establece este indicador, **DoCopyProps** realiza una operación de copia. 
    
MAPI_NOREPLACE 
  
> Las propiedades existentes en el objeto de destino no se deben sobrescribir. Cuando no se establece este indicador, **DoCopyProps** sobrescribe las propiedades existentes. 
    
 _lppProblems_
  
> [in, out] En la entrada, un puntero a un puntero a una estructura [SPropProblemArray](spropproblemarray.md) ; de lo contrario, NULL, que indica que no es necesario información del error. Si _lppProblems_ es un puntero válido en la entrada, **DoCopyProps** devuelve información detallada sobre los errores al copiar una o más propiedades. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las propiedades se copiaron o movieron correctamente.
    
MAPI_E_COLLISION 
  
> Una propiedad que se va a copiar o mover ya existe en el objeto de destino y se ha establecido la marca MAPI_NOREPLACE. 
    
MAPI_E_FOLDER_CYCLE 
  
> El objeto de origen contiene directa o indirectamente el objeto de destino. Es posible que se haya realizado un trabajo significativo antes de que se detectara esta condición, por lo que los objetos de origen y de destino podrían modificarse parcialmente. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> La interfaz identificada por el parámetro _lpSrcInterface_ no es compatible con el objeto de origen, o la interfaz identificada por el parámetro _lpDestInterface_ no es compatible con el objeto de destino. 
    
MAPI_E_NO_ACCESS 
  
> Se intentó obtener acceso a un objeto para el que el autor de la llamada no tiene permisos suficientes. Este error se devuelve si el objeto de destino es el mismo que el objeto de origen.
    
Los valores siguientes se pueden devolver en la estructura **SPropProblemArray** , pero no como valores devueltos para **DoCopyProps**. Estos errores se aplican a una sola propiedad.
  
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció la marca MAPI_UNICODE y **DoCopyProps** no admite Unicode, o bien no se estableció MAPI_UNICODE y **DoCopyProps** solo admite Unicode. 
    
MAPI_E_COMPUTED 
  
> La propiedad no la puede modificar el autor de la llamada porque es una propiedad de solo lectura, calculada por el propietario del objeto de destino. Este error no es grave; el autor de la llamada debe permitir que continúe la operación de copia.
    
MAPI_E_INVALID_TYPE 
  
> El tipo de propiedad no es válido.
    
MAPI_E_UNEXPECTED_TYPE 
  
> El tipo de propiedad no es el tipo que el autor de la llamada espera.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::D ocopyprops** se implementa para los objetos de compatibilidad del proveedor de almacenamiento de mensajes. Los proveedores de almacenamiento de mensajes pueden llamar a **DoCopyProps** para implementar el método [IMAPIProp:: CopyProps](imapiprop-copyprops.md) para sus carpetas y mensajes. **DoCopyProps** copia o mueve las propiedades identificadas en la matriz de etiquetas de propiedad a la que señala _lpIncludeProps_ y que están presentes en el objeto al que apunta _lpSrcObj_. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando se copian propiedades entre objetos del mismo tipo, como dos mensajes, los parámetros _lpSrcInterface_ y _lpDestInterface_ deben contener el mismo identificador de interfaz y los parámetros _lpSrcObj_ y _lpDestObj_ debe apuntar a objetos del mismo tipo. Si _lpDestInterface_ se establece en null, **DoCopyProps** devuelve MAPI_E_INVALID_PARAMETER. Si establece _lpDestInterface_ en un identificador de interfaz aceptable, pero establece _lpDestObj_ en un puntero no válido, los resultados son imprevisibles. Lo más probable es que se produzca un error en el proveedor. 
  
Establezca la marca MAPI_NOREPLACE si no desea sobrescribir ninguna de las propiedades en el objeto de destino. Las propiedades del objeto de destino que existen en el objeto de origen y que no se sobrescriben no se eliminan ni se modifican.
  
Para copiar la lista de destinatarios de un mensaje, incluya la propiedad **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) en la matriz de etiquetas de propiedad señalada por el parámetro _lpIncludeProps_ . Para copiar los datos adjuntos del mensaje, incluya la propiedad **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). 
  
Para copiar una carpeta o tabla de contenido o de jerarquía de un contenedor de libreta de direcciones, incluya **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) o **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) en la matriz de etiquetas de propiedades. Para incluir la tabla Contents asociada de una carpeta, incluya la propiedad **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) en la matriz.
  
Si se copian o se mueven subcarpetas, su contenido se copia o se mueve en su totalidad, independientemente del uso de las propiedades indicadas por la estructura **SPropTagArray** . 
  
 **DoCopyProps** informa de los errores globales que se producen con la operación en su totalidad y los errores individuales que se producen con una o varias de las propiedades. Estos errores individuales se colocan en una estructura **SPropProblemArray** . Puede suprimir los informes de errores en el nivel de propiedad pasando NULL, en lugar de un puntero válido, para el parámetro de estructura de matriz con problemas de propiedad. 
  
Si desea recibir información sobre los errores, pase un puntero de estructura **SPropProblemArray** válido en el parámetro _lppProblems_ . Cuando **DoCopyProps** Devuelve S_OK, compruebe si hay posibles errores con propiedades individuales en la estructura. Cuando **DoCopyProps** devuelve un error, no se devuelve información en la estructura **SPropProblemArray** . En su lugar, llame al método [IMAPISupport:: GetLastError](imapisupport-getlasterror.md) para recuperar información detallada del error. 
  
Si **DoCopyProps** Devuelve S_OK, libere la estructura **SPropProblemArray** devuelta llamando a la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="see-also"></a>Vea también



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

