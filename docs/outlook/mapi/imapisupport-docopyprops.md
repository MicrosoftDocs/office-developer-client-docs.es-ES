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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: c93e01b1e4621cddc4c98d528e5f5339cba21dae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817486"
---
# <a name="imapisupportdocopyprops"></a>IMAPISupport::DoCopyProps

  
  
**Se aplica a**: Outlook 
  
Copia o mueve una o más propiedades de un objeto a otro objeto.
  
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

## <a name="parameters"></a>Sintaxis

 _lpSrcInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al objeto con las propiedades que se pueden copiar o mover.
    
 _lpSrcObj_
  
> [entrada] Un puntero al objeto que contiene las propiedades para ser copiado o movido.
    
 _lpIncludeProps_
  
> [entrada] Un puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene una matriz unidimensional de etiquetas de propiedad que indican las propiedades para copiar o mover. El parámetro _lpIncludeProps_ no puede ser NULL. 
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal del indicador de progreso.
    
 _lpProgress_
  
> [entrada] Un puntero a una implementación de un indicador de progreso. Si se pasa NULL en el parámetro _lpProgress_ , se muestra el indicador de progreso mediante el uso de la implementación de MAPI. El parámetro _lpProgress_ se omite a menos que la marca MAPI_DIALOG se establece en el parámetro _ulFlags indicado_ . 
    
 _lpDestInterface_
  
> [entrada] Un puntero para el identificador de interfaz que representa la interfaz que se usará para tener acceso al objeto para recibir las propiedades que se copian o se mueven.
    
 _lpDestObj_
  
> [entrada] Un puntero al objeto que se va a recibir las propiedades que se ha movido o copiadas.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se realiza la operación de copiar o mover. Se pueden establecer los siguientes indicadores:
    
MAPI_DIALOG 
  
> Muestra un indicador de progreso.
    
MAPI_MOVE 
  
> **DoCopyProps** debe realizar una operación de movimiento en lugar de una operación de copia. Cuando no se establece este marcador, **DoCopyProps** realiza una operación de copia. 
    
MAPI_NOREPLACE 
  
> No se deben sobrescribir las propiedades existentes en el objeto de destino. Cuando no se establece este marcador, **DoCopyProps** sobrescribe las propiedades existentes. 
    
 _lppProblems_
  
> [entrada, salida] En la entrada, un puntero a un puntero a una estructura [SPropProblemArray](spropproblemarray.md) ; de lo contrario, NULL, que indica que no hay necesidad de información de error. Si _lppProblems_ es un puntero válido en la entrada, **DoCopyProps** devuelve información detallada acerca de los errores de copiar una o más propiedades. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Propiedades se han copiado o movido correctamente.
    
MAPI_E_COLLISION 
  
> Una propiedad para ser copiado o movido ya existe en el objeto de destino y se establece la marca MAPI_NOREPLACE. 
    
MAPI_E_FOLDER_CYCLE 
  
> El objeto de origen, directa o indirectamente contiene el objeto de destino. Trabajo significativo es posible que se han realizado antes de que se ha detectado esta condición, por lo que los objetos de origen y de destino podrían modificarse parcialmente. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> La interfaz identificada mediante el parámetro _lpSrcInterface_ no es compatible con el objeto de origen o la interfaz identificada mediante el parámetro _lpDestInterface_ no es compatible con el objeto de destino. 
    
MAPI_E_NO_ACCESS 
  
> Se ha intentado tener acceso a un objeto para el que el autor de la llamada no tiene permisos suficientes. Este error se devuelve si el objeto de destino es el mismo que el objeto de origen.
    
Los siguientes valores se pueden devolver en la estructura de **SPropProblemArray** , pero no como valores devueltos por **DoCopyProps**. Estos errores se aplican a una sola propiedad.
  
MAPI_E_BAD_CHARWIDTH 
  
> Se ha establecido el indicador MAPI_UNICODE y **DoCopyProps** no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y **DoCopyProps** admite sólo Unicode. 
    
MAPI_E_COMPUTED 
  
> La propiedad no puede modificarse el autor de la llamada porque es una propiedad de solo lectura, calculada por el propietario del objeto de destino. Este error no es grave; el autor de la llamada debe permitir que la operación de copia continuar.
    
MAPI_E_INVALID_TYPE 
  
> El tipo de propiedad no es válido.
    
MAPI_E_UNEXPECTED_TYPE 
  
> El tipo de propiedad no es el tipo que espera el autor de la llamada.
    
## <a name="remarks"></a>Notas

El método **IMAPISupport::DoCopyProps** se implementa para objetos de soporte técnico de proveedor de almacén de mensajes. Los proveedores de almacén de mensajes pueden llamar a **DoCopyProps** para implementar el método [IMAPIProp::CopyProps](imapiprop-copyprops.md) para sus carpetas y mensajes. **DoCopyProps** copia o mueve las propiedades que se identifican en la matriz de etiqueta de propiedad que señala _lpIncludeProps_ y que están presentes en el objeto al que señala por _lpSrcObj_. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando se copian propiedades entre objetos del mismo tipo, como dos mensajes, los parámetros _lpSrcInterface_ y _lpDestInterface_ deben contener los mismos parámetros de identificador y _lpSrcObj_ y _lpDestObj_ de interfaz debe apuntar a los objetos del mismo tipo. Si _lpDestInterface_ se establece en NULL, **DoCopyProps** devuelve MAPI_E_INVALID_PARAMETER. Si se establece _lpDestInterface_ en un identificador de interfaz aceptable, pero el conjunto _lpDestObj_ a un puntero no válido, los resultados serán impredecibles. Es muy probable que se producirá un error en el proveedor. 
  
Establecer la marca MAPI_NOREPLACE si no desea que cualquiera de las propiedades en el objeto de destino se sobrescriban. Las propiedades en el objeto de destino que existen en el objeto de origen y no se sobrescriben no se eliminan o modifican.
  
Para copiar la lista de destinatarios de un mensaje, incluir la propiedad **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) en la matriz de etiqueta de la propiedad indicada por el parámetro _lpIncludeProps_ . Para copiar los datos adjuntos del mensaje, incluir la propiedad **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). 
  
Para copiar una carpeta o la jerarquía del contenedor de la libreta de direcciones o la tabla de contenido, incluir **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) o **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) en la matriz de la etiqueta de propiedad. Para incluir la tabla de contenido asociada de una carpeta, incluya la propiedad **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) en la matriz.
  
Si se copian o se mueven las subcarpetas, su contenido se copian o se mueven en su totalidad, independientemente del uso de las propiedades indicado por la estructura del **elemento SPropTagArray** . 
  
 **DoCopyProps** informes de errores global que se producen con la operación como un todo y errores individuales que se producen con una o varias de las propiedades. Estos errores individuales se colocan en una estructura **SPropProblemArray** . Puede suprimir informes en el nivel de propiedad pasando NULL, en lugar de un puntero válido para el parámetro de estructura de matriz de propiedad problema de error. 
  
Si desea recibir información acerca de los errores, pase un puntero de estructura **SPropProblemArray** válido en el parámetro _lppProblems_ . Cuando **DoCopyProps** devuelve S_OK, comprobar los posibles errores con las propiedades individuales de la estructura de. Cuando **DoCopyProps** devuelve un error, no se devuelve información de la estructura de **SPropProblemArray** . En su lugar, llame al método de [IMAPISupport::GetLastError](imapisupport-getlasterror.md) para recuperar información detallada del error. 
  
Si **DoCopyProps** devuelve S_OK, liberar la estructura **SPropProblemArray** devuelta por una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="see-also"></a>Ver también



[IMAPIProp::CopyProps](imapiprop-copyprops.md)
  
[IMAPISupport::CopyMessages](imapisupport-copymessages.md)
  
[IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[Propiedad canónico PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[Propiedad canónico PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[Propiedad canónico PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)
  
[Propiedad canónico PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)
  
[Propiedad canónico PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[Elemento SPropTagArray](sproptagarray.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

