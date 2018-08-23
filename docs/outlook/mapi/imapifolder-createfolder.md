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
ms.openlocfilehash: 694f7ec5715a7348c9bd90c28d14f30d43d19974
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581786"
---
# <a name="imapifoldercreatefolder"></a>IMAPIFolder::CreateFolder

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una nueva subcarpeta.
  
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

## <a name="parameters"></a>Parámetros

 _ulFolderType_
  
> [entrada] El tipo de carpeta que se va a crear. Se pueden establecer los siguientes indicadores:
    
FOLDER_GENERIC 
  
> Se debe crear una carpeta genérica.
    
FOLDER_SEARCH 
  
> Se debe crear una carpeta de resultados de búsqueda.
    
 _lpszFolderName_
  
> [entrada] Un puntero a una cadena que contiene el nombre para la nueva carpeta. Este nombre es la base para la propiedad de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de la nueva carpeta.
    
 _lpszFolderComment_
  
> [entrada] Un puntero a una cadena que contiene un comentario asociado a la nueva carpeta. Esta cadena se convierte en el valor de propiedad de **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) de la nueva carpeta. Si se pasa NULL, la carpeta no tiene ningún comentario inicial.
    
 _lpInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la nueva carpeta. Pasando NULL hace que el proveedor de almacenamiento de mensajes devolver la interfaz de carpeta estándar, [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). Los clientes deben pasar NULL. Otros autores de llamadas pueden establecer el parámetro _lpInterface_ para IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer o IID_IMAPIFolder. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se crea la carpeta. Se pueden establecer los siguientes indicadores:
    
MAPI_DEFERRED_ERRORS 
  
> Permite **CreateFolder** devolver de correctamente, posiblemente antes de que la nueva carpeta es completamente disponible para el cliente de la llamada. Si la nueva carpeta no está disponible, realizar una llamada posterior a él puede provocar un error. 
    
MAPI_UNICODE. 
  
> El nombre de la carpeta está en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., el nombre de la carpeta está en formato ANSI.
    
OPEN_IF_EXISTS 
  
> Permite que el método se realice correctamente, incluso si la carpeta denominada en el parámetro _lpszFolderName_ ya existe, abra la carpeta existente que tiene ese nombre. Tenga en cuenta que los proveedores de almacén de mensajes que permiten carpetas que tienen el mismo nombre de elemento del mismo nivel no pueden abrir una carpeta existente si existe más de uno con el nombre proporcionado. 
    
 _lppFolder_
  
> [out] Un puntero a un puntero a la carpeta recién creada.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La nueva carpeta se ha creado o abierto, si se establece la marca OPEN_IF_EXISTS correctamente.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.
    
MAPI_E_COLLISION 
  
> Una carpeta que tiene el nombre indicado en el parámetro _lpszFolderName_ ya existe. Los nombres de carpeta deben ser únicos. 
    
## <a name="remarks"></a>Comentarios

El método **IMAPIFolder::CreateFolder** crea una subcarpeta en la carpeta actual y asigna un identificador de entrada a la nueva carpeta. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando se devuelve **CreateFolder** , tenga en cuenta que es posible que el identificador de entrada para la nueva carpeta no estén disponible. Algunos proveedores de almacén de mensajes no hace los identificadores de entrada disponible hasta después de llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la carpeta nueva para guardar de forma permanente. Esto es especialmente útil si ha establecido el indicador MAPI_DEFERRED_ERRORS. 
  
Tenga en cuenta que algunos proveedores de almacenes de mensaje elija siempre el parámetro _lppFolder_ interfaz estándar de la carpeta, independientemente del valor que se pasa para el parámetro _lpInterface_ . Debido a que el puntero de interfaz que se devuelve no puede ser del tipo que se esperaba, llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la carpeta nueva para recuperar la propiedad **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)). Si es necesario, convertir el puntero a un tipo más apropiado antes de realizar otras llamadas.
  
La mayoría de los proveedores de almacén de mensajes requieren el nombre de la nueva carpeta por qué ser únicos con respecto a los nombres de las carpetas del mismo nivel. Ser capaz de controlar el valor de error MAPI_E_COLLISION, que se devuelve si no se sigue esta regla. 
  
Para determinar el identificador de entrada de la carpeta recién creada, llamar al método **IMAPIProp::GetProps** de la carpeta nueva para recuperar su propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnCreateSubFolder  <br/> |MFCMAPI utiliza el método **CMsgStoreDlg::OnCreateSubFolder** para crear nuevas carpetas en MFCMAPI.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

