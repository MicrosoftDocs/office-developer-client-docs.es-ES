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
ms.openlocfilehash: 285da82d143524d2b2cf73ed3e5f1e3aeef6f9b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405103"
---
# <a name="iaddrbooknewentry"></a>IAddrBook::NewEntry

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Agrega un nuevo destinatario a un contenedor de libreta de direcciones o a la lista de destinatarios de un mensaje saliente.
  
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

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> a Identificador de la ventana principal del cuadro de diálogo.
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que controla el tipo de texto que se usa. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.
    
 _cbEIDContainer_
  
> a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEIDContainer_ . 
    
 _lpEIDContainer_
  
> a Un puntero al identificador de entrada del contenedor donde se agregará el nuevo destinatario. Si el parámetro _cbEIDContainer_ es cero, el método **NEWENTRY** devuelve un identificador de entrada de destinatario y una lista de plantillas como si se hubiera llamado al método [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) . 
    
 _cbEIDNewEntryTpl_
  
> a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEIDNewEntryTpl_ . 
    
 _lpEIDNewEntryTpl_
  
> a Un puntero a una plantilla de uso único que se usará para crear el nuevo destinatario. Si _cbEIDNewEntryTpl_ es cero y _lpEIDNewEntryTpl_ es null, **NEWENTRY** muestra un cuadro de diálogo con el que el usuario puede seleccionar de una lista de plantillas para agregar nuevas entradas. 
    
 _lpcbEIDNewEntry_
  
> contempla Un puntero al recuento de bytes en el identificador de entrada al que apunta el parámetro _lppEIDNewEntry_ . 
    
 _lppEIDNewEntry_
  
> contempla Un puntero a un puntero al identificador de entrada del nuevo destinatario.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La nueva entrada de la libreta de direcciones se creó correctamente.
    
## <a name="remarks"></a>Comentarios

El método **NEWENTRY** crea una nueva entrada de la libreta de direcciones, que se agrega directamente en un contenedor o que se va a usar para dirigir un mensaje saliente. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si desea que la nueva entrada se agregue a un contenedor específico, establezca _lpEIDContainer_ en el identificador de entrada del contenedor y _cbEIDContainer_ en el recuento de bytes en el identificador de entrada. 
  
Si desea que la nueva entrada se agregue a la lista de destinatarios de un mensaje saliente, establezca _lpEIDContainer_ en NULL y _cbEIDContainer_ en cero. 
  
Si desea permitir que el usuario de una aplicación cliente seleccione el tipo de entrada que se va a crear, pase cero en _cbEIDNewEntryTpl_ y null en _lpEIDNewEntryTpl_. El método **NEWENTRY** muestra la tabla de una sola desactivación, una lista de plantillas admitidas por MAPI y por cada proveedor de la libreta de direcciones en la sesión. Cada plantilla puede crear una entrada de destinatario para uno o más tipos de dirección. 
  
Si desea conservar el identificador de entrada de la nueva entrada, pase punteros válidos en los parámetros _lpcbEIDNewEntry_ y _lppEIDNewEntry_ . Usted es responsable de liberar este identificador de entrada cuando termine con él llamando a la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Para usar una plantilla determinada para agregar una nueva entrada a un contenedor modificable, use el siguiente procedimiento:
  
1. Llame al método [IMAPISession:: OpenEntry](imapisession-openentry.md) para abrir el contenedor de destino y establezca el parámetro _lpEntryID_ en el identificador de entrada del contenedor. 
    
2. Llame al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) del contenedor de destino y establezca el parámetro _ulPropTag_ en **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) y el parámetro _lpiid_ en IID_IMAPITable. El contenedor devolverá una tabla única en la que se enumeran todas las plantillas que admite para crear nuevas entradas. 
    
3. Recupere la fila que representa la plantilla para el tipo concreto de entrada que desea crear. La columna **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) indica el tipo de dirección que es compatible con la plantilla.
    
4. Llame al método **NEWENTRY** y establezca _lpEIDNewEntryTpl_ en el identificador de entrada de la plantilla seleccionada. El identificador de entrada será la columna **** 1 ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la fila de la plantilla en la tabla de uso único. Pase cero en _cbEIDContainer_ y null en _lpEIDContainer_. Pase un puntero válido en el parámetro _lppEIDNewEntry_ si desea conservar el identificador de entrada de la nueva entrada. 
    
## <a name="see-also"></a>Ver también



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[Propiedad canónica PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

