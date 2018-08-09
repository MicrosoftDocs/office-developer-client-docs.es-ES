---
title: IAddrBookNewEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.NewEntry
api_type:
- COM
ms.assetid: 8d2d786b-e621-456d-b087-3373df6f8ac5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e9b9ae316749659c6fc6a043bfb72c49010ccc9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817151"
---
# <a name="iaddrbooknewentry"></a>IAddrBook::NewEntry

  
  
**Hace referencia a**: Outlook 
  
Agrega a un nuevo destinatario a un contenedor de la libreta de direcciones o a la lista de destinatarios de un mensaje saliente.
  
```cpp
HRESULT NewEntry(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cbEIDContainer,
  LPENTRYID lpEIDContainer,
  ULONG cbEIDNewEntryTpl,
  LPENTRYID lpEIDNewEntryTpl,
  ULONG FAR * lpcbEIDNewEntry,
  LPENTRYID FAR * lppEIDNewEntry
);
```

## <a name="parameters"></a>Parámetros

 _ulUIParam_
  
> [entrada] Identificador de la ventana primaria para el cuadro de diálogo.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla el tipo de texto que se usa. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> Las cadenas que se pasan en están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.
    
 _cbEIDContainer_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEIDContainer_ . 
    
 _lpEIDContainer_
  
> [entrada] Un puntero al identificador de entrada del contenedor donde es el destinatario nuevo que se va a agregar. Si el parámetro _cbEIDContainer_ es cero, el método **NewEntry** devuelve un identificador de entrada del destinatario y una lista de plantillas como si se llamó al método [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) . 
    
 _cbEIDNewEntryTpl_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEIDNewEntryTpl_ . 
    
 _lpEIDNewEntryTpl_
  
> [entrada] Un puntero a una plantilla de uso único que se usará para crear al nuevo destinatario. Si _cbEIDNewEntryTpl_ es cero y _lpEIDNewEntryTpl_ es NULL, **NewEntry** muestra un cuadro de diálogo con el que el usuario puede seleccionar de una lista de plantillas para agregar nuevas entradas. 
    
 _lpcbEIDNewEntry_
  
> [out] Un puntero para el número de bytes en el identificador de entrada indicado por el parámetro _lppEIDNewEntry_ . 
    
 _lppEIDNewEntry_
  
> [out] Un puntero a un puntero al identificador de entrada del destinatario nuevo.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se ha creado correctamente la nueva entrada de la libreta de direcciones.
    
## <a name="remarks"></a>Comentarios

El método **NewEntry** crea una nueva entrada de la libreta de direcciones, que se agregará directamente en un contenedor o que se utilizan para tratar un mensaje saliente. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si desea que la nueva entrada que se agregarán a un contenedor específico, establezca _lpEIDContainer_ en el contenedor identificador de entrada y _cbEIDContainer_ para el número de bytes en el identificador de entrada. 
  
Si desea que la nueva entrada que se agregará a la lista de destinatarios de un mensaje saliente, establezca _lpEIDContainer_ en NULL y _cbEIDContainer_ a cero. 
  
Si desea permitir que el usuario de una aplicación cliente para seleccionar el tipo de entrada que se creará, pase cero en _cbEIDNewEntryTpl_ y NULL en _lpEIDNewEntryTpl_. El método **NewEntry** muestra en la tabla de uso único de MAPI, una lista de plantillas admitidas por MAPI y por cada proveedor de la libreta de direcciones en la sesión. Cada plantilla puede crear una entrada para uno o varios tipos de dirección del destinatario. 
  
Si desea conservar el identificador de entrada de la nueva entrada, pase los parámetros _lpcbEIDNewEntry_ y _lppEIDNewEntry_ punteros válidos. Usted es responsable de liberar este identificador de entrada cuando haya terminado con él mediante una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Para usar una plantilla en particular para agregar una nueva entrada a un contenedor modificable, use el siguiente procedimiento:
  
1. Llame al método [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir el contenedor de destino y establezca el parámetro _lpEntryID_ en el identificador de entrada del contenedor. 
    
2. Llamar al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del contenedor de destino y establezca el parámetro _ulPropTag_ a **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) y el parámetro _lpiid_ a IID_IMAPITable. El contenedor devolverá una tabla de uso único que se enumera todas las plantillas que admite para la creación de nuevas entradas. 
    
3. Recuperar la fila que representa la plantilla para el tipo concreto de entrada que desea crear. La columna **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) indica el tipo de dirección que es compatible con la plantilla.
    
4. Llame al método **NewEntry** y establecer _lpEIDNewEntryTpl_ en el identificador de entrada de la plantilla seleccionada. El identificador de entrada será la columna de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la fila de la plantilla en la tabla de uso único. Pasar cero en _cbEIDContainer_ y NULL en _lpEIDContainer_. Pase un puntero válido en el parámetro _lppEIDNewEntry_ si desea conservar el identificador de entrada de la nueva entrada. 
    
## <a name="see-also"></a>Vea también



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[Propiedad canónica PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

