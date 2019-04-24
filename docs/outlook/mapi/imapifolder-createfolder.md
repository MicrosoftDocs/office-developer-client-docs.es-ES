---
title: IMAPIFolderCreateFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CreateFolder
api_type:
- COM
ms.assetid: 39d07fc8-09aa-4122-af32-b02f2c893d29
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 606d780aa59e363c30ddc7a5b562db64d845ccb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280081"
---
# <a name="imapifoldercreatefolder"></a>IMAPIFolder::CreateFolder

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una subcarpeta nueva.
  
```cpp
HRESULT CreateFolder(
  ULONG ulFolderType,
  LPSTR lpszFolderName,
  LPSTR lpszFolderComment,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMAPIFOLDER FAR * lppFolder
);
```

## <a name="parameters"></a>Parameters

 _ulFolderType_
  
> a El tipo de carpeta que se va a crear. Se pueden establecer los siguientes indicadores:
    
FOLDER_GENERIC 
  
> Se debe crear una carpeta genérica.
    
FOLDER_SEARCH 
  
> Debe crearse una carpeta de resultados de búsqueda.
    
 _lpszFolderName_
  
> a Un puntero a una cadena que contiene el nombre de la nueva carpeta. Este nombre es la base de la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de la nueva carpeta.
    
 _lpszFolderComment_
  
> a Un puntero a una cadena que contiene un comentario asociado a la nueva carpeta. Esta cadena se convierte en el valor de la propiedad **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) de la nueva carpeta. Si se pasa NULL, la carpeta no tiene comentario inicial.
    
 _lpInterface_
  
> a Un puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso a la nueva carpeta. Al pasar NULL, el proveedor de almacén de mensajes devuelve la interfaz de carpeta estándar, [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). Los clientes deben pasar NULL. Otros llamadores pueden establecer el parámetro _lpInterface_ en IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer o IID_IMAPIFolder. 
    
 _ulFlags_
  
> a Una máscara de máscara de marcas que controla cómo se crea la carpeta. Se pueden establecer los siguientes indicadores:
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **CreateFolder** vuelva correctamente, posiblemente antes de que la nueva carpeta esté completamente disponible para el cliente que realiza la llamada. Si la nueva carpeta no está disponible, realizar una llamada subsiguiente a ella puede provocar un error. 
    
MAPI_UNICODE 
  
> El nombre de la carpeta está en formato Unicode. Si no se establece la marca MAPI_UNICODE, el nombre de la carpeta está en formato ANSI.
    
OPEN_IF_EXISTS 
  
> Permite que el método tenga éxito incluso si la carpeta especificada en el parámetro _lpszFolderName_ ya existe abriendo la carpeta existente que tiene ese nombre. Tenga en cuenta que es posible que los proveedores de almacenamiento de mensajes que permiten que las carpetas relacionadas tengan el mismo nombre no puedan abrir una carpeta existente si existe más de una con el nombre proporcionado. 
    
 _lppFolder_
  
> contempla Un puntero a un puntero a la carpeta que se acaba de crear.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La nueva carpeta se ha creado o abierto correctamente, si se ha establecido la marca OPEN_IF_EXISTS.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció la marca MAPI_UNICODE y la implementación no admite Unicode, o no se estableció MAPI_UNICODE y la implementación solo admite Unicode.
    
MAPI_E_COLLISION 
  
> Ya existe una carpeta con el nombre especificado en el parámetro _lpszFolderName_ . Los nombres de carpeta deben ser únicos. 
    
## <a name="remarks"></a>Comentarios

El método **IMAPIFolder:: CreateFolder** crea una subcarpeta en la carpeta actual y asigna un identificador de entrada a la nueva carpeta. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando **CreateFolder** Return, tenga en cuenta que es posible que el identificador de entrada para la nueva carpeta no esté disponible. Algunos proveedores de almacenamiento de mensajes no hacen que los identificadores de entrada estén disponibles hasta que se llama al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) de la nueva carpeta para guardarlo de forma permanente. Esto es especialmente cierto si ha establecido la marca MAPI_DEFERRED_ERRORS. 
  
Tenga en cuenta que algunos proveedores de almacenamiento de mensajes siempre señalan el parámetro _lppFolder_ a la interfaz estándar de la carpeta, independientemente del valor que se pase para el parámetro _lpInterface_ . Dado que el puntero de interfaz que se devuelve puede que no sea del tipo que espera, llame al método [IMAPIProp:: GetProps](imapiprop-getprops.md) de la nueva carpeta para recuperar la propiedad **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)). Si es necesario, convierta el puntero en un tipo más apropiado antes de realizar otras llamadas.
  
La mayoría de los proveedores de almacenamiento de mensajes requieren que el nombre de la nueva carpeta sea único con respecto a los nombres de sus carpetas relacionadas. Ser capaz de controlar el valor de error MAPI_E_COLLISION, que se devuelve si no se sigue esta regla. 
  
Para determinar el identificador de entrada de la carpeta recién creada, llame al método **IMAPIProp:: GetProps** de la nueva carpeta para recuperar **** su propiedad ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MsgStoreDlg. cpp  <br/> |CMsgStoreDlg:: OnCreateSubFolder  <br/> |MFCMAPI usa el método **CMsgStoreDlg:: OnCreateSubFolder** para crear nuevas carpetas en MFCMAPI.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

