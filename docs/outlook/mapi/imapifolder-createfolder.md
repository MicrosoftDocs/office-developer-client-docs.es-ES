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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436765"
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
  
> [in] Tipo de carpeta que se debe crear. Se pueden establecer las siguientes marcas:
    
FOLDER_GENERIC 
  
> Se debe crear una carpeta genérica.
    
FOLDER_SEARCH 
  
> Se debe crear una carpeta de resultados de búsqueda.
    
 _lpszFolderName_
  
> [in] Puntero a una cadena que contiene el nombre de la nueva carpeta. Este nombre es la base de la propiedad PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de la nueva carpeta.
    
 _lpszFolderComment_
  
> [in] Puntero a una cadena que contiene un comentario asociado a la nueva carpeta. Esta cadena se convierte en el valor de la propiedad **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) de la nueva carpeta. Si se pasa NULL, la carpeta no tiene ningún comentario inicial.
    
 _lpInterface_
  
> [in] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la nueva carpeta. Si se pasa NULL, el proveedor del almacén de mensajes devuelve la interfaz de carpeta estándar, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md). Los clientes deben pasar NULL. Otros autores de llamadas pueden establecer el parámetro lpInterface en  _IID_IUnknown,_ IID_IMAPIProp, IID_IMAPIContainer o IID_IMAPIFolder. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se crea la carpeta. Se pueden establecer las siguientes marcas:
    
MAPI_DEFERRED_ERRORS 
  
> Permite **que CreateFolder** vuelva correctamente, posiblemente antes de que la nueva carpeta esté totalmente disponible para el cliente que realiza la llamada. Si la nueva carpeta no está disponible, realizar una llamada posterior a ella puede provocar un error. 
    
MAPI_UNICODE 
  
> El nombre de la carpeta está en formato Unicode. Si la MAPI_UNICODE no está establecida, el nombre de la carpeta está en formato ANSI.
    
OPEN_IF_EXISTS 
  
> Permite que el método se haga correctamente incluso si la carpeta denominada en el parámetro  _lpszFolderName_ ya existe abriendo la carpeta existente que tiene ese nombre. Tenga en cuenta que es posible que los proveedores de almacén de mensajes que permiten que las carpetas del mismo nombre tengan el mismo nombre no abran una carpeta existente si existe más de uno con el nombre proporcionado. 
    
 _lppFolder_
  
> [salida] Puntero a un puntero a la carpeta recién creada.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La nueva carpeta se ha creado o abierto correctamente, si se OPEN_IF_EXISTS marca.
    
MAPI_E_BAD_CHARWIDTH 
  
> La marca MAPI_UNICODE se estableció y la implementación no admite Unicode, o MAPI_UNICODE no se estableció y la implementación solo admite Unicode.
    
MAPI_E_COLLISION 
  
> Ya existe una carpeta con el nombre especificado en el _parámetro lpszFolderName._ Los nombres de carpeta deben ser únicos. 
    
## <a name="remarks"></a>Comentarios

El **método IMAPIFolder::CreateFolder** crea una subcarpeta en la carpeta actual y asigna un identificador de entrada a la nueva carpeta. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando **createFolder** devuelve, tenga en cuenta que es posible que el identificador de entrada de la nueva carpeta no esté disponible. Algunos proveedores de almacén de mensajes no hacen que los identificadores de entrada estén disponibles hasta después de llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la nueva carpeta para guardarlo de forma permanente. Esto es especialmente cierto si ha establecido la MAPI_DEFERRED_ERRORS marca. 
  
Tenga en cuenta que algunos proveedores de almacén de mensajes siempre apuntan el parámetro _lppFolder_ a la interfaz estándar de la carpeta, independientemente del valor que pase para el parámetro _lpInterface._ Dado que el puntero de interfaz que se devuelve puede no ser del tipo que espera, llame al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la nueva carpeta para recuperar la propiedad **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)). Si es necesario, convierte el puntero en un tipo más adecuado antes de realizar otras llamadas.
  
La mayoría de los proveedores de almacén de mensajes requieren que el nombre de la nueva carpeta sea único con respecto a los nombres de sus carpetas del mismo nivel. Puede controlar el valor MAPI_E_COLLISION error, que se devuelve si no se sigue esta regla. 
  
Para determinar el identificador de entrada de la carpeta recién creada, llame al método **IMAPIProp::GetProps** de la nueva carpeta para recuperar su propiedad **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnCreateSubFolder  <br/> |MFCMAPI usa el **método CMsgStoreDlg::OnCreateSubFolder** para crear nuevas carpetas en MFCMAPI.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

