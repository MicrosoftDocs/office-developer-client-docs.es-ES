---
title: IMAPISupportNewEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.NewEntry
api_type:
- COM
ms.assetid: 588d002b-8412-4ab9-9757-04ad89e0a6f8
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d978b7a6bd8af9a505fa025aef2e5da68308468f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588597"
---
# <a name="imapisupportnewentry"></a>IMAPISupport::NewEntry

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Agrega a un nuevo destinatario directamente a un contenedor de la libreta de direcciones o a la lista de destinatarios de un mensaje saliente.
  
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
  
> [entrada] Identificador de la ventana principal del cuadro de diálogo.
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _cbEIDContainer_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEIDContainer_ . 
    
 _lpEIDContainer_
  
> [entrada] Un puntero al identificador de entrada del contenedor para recibir la nueva entrada. Si _cbEIDContainer_ es 0 y _lpEIDContainer_ es NULL, **NewEntry** crea un identificador de entrada único que es el mismo tipo que es generado por una llamada al método [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) . 
    
 _cbEIDNewEntryTpl_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEIDNewEntryTpl_ . 
    
 _lpEIDNewEntryTpl_
  
> [entrada] Un puntero al identificador de entrada de la plantilla que se usará para crear la nueva entrada. Si _cbEIDNewEntryTpl_ es 0 y _lpEIDNewEntryTpl_ es NULL, **NewEntry** muestra un cuadro de diálogo que permite al usuario seleccionar de una lista de plantillas para agregar nuevas entradas. 
    
 _lpcbEIDNewEntry_
  
> [out] Un puntero para el número de bytes en el identificador de entrada indicado por el parámetro _lppEIDNewEntry_ . 
    
 _lppEIDNewEntry_
  
> [out] Un puntero a un puntero al identificador de entrada de la entrada recién creada.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se ha creado correctamente la nueva entrada.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::NewEntry** se implementa para objetos de compatibilidad con de proveedor de la libreta de direcciones. Los proveedores de la libreta de direcciones, llame a **NewEntry** para crear una nueva entrada de la libreta de direcciones que se agregará directamente en un contenedor o que se utilizan para tratar un mensaje saliente. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si desea que la nueva entrada que se agregarán a un contenedor específico, establezca _lpEIDContainer_ en el contenedor identificador de entrada y _cbEIDContainer_ para el número de bytes en el identificador de entrada. 
  
Si desea que la nueva entrada que se agregará a la lista de destinatarios de un mensaje saliente, establezca _lpEIDContainer_ en NULL y _cbEIDContainer_ en 0. 
  
Si desea permitir que el usuario de una aplicación cliente para seleccionar el tipo de entrada que se creará, pase 0 en _cbEIDNewEntryTpl_ y NULL en _lpEIDNewEntryTpl_. **NewEntry** se muestra en la tabla de uso único de MAPI, una lista de plantillas que admiten MAPI y cada uno de los proveedores de la libreta de direcciones en la sesión. Cada plantilla puede crear una entrada para uno o varios tipos de dirección del destinatario. 
  
Si desea conservar el identificador de entrada de la nueva entrada, pase los parámetros _lpcbEIDNewEntry_ y _lppEIDNewEntry_ punteros válidos. Usted es responsable de liberar este identificador de entrada cuando haya terminado con él mediante una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Para usar una plantilla en particular para agregar una nueva entrada a un contenedor modificable, use el siguiente procedimiento:
  
1. Llame al método [IMAPISupport::OpenEntry](imapisupport-openentry.md) para abrir el contenedor de destino y establezca el parámetro _lpEntryID_ en el identificador de entrada del contenedor. 
    
2. Llamar al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del contenedor de destino y establezca el parámetro _ulPropTag_ a **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) y el parámetro _lpiid_ a IID_IMAPITable. El contenedor devolverá una tabla de uso único que se enumera todas las plantillas que admite para la creación de nuevas entradas. 
    
3. Recuperar la fila que representa la plantilla para el tipo concreto de entrada que desea crear. La columna **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) indica el tipo de dirección que es compatible con la plantilla. 
    
4. Llamar a **IMAPISupport::NewEntry** y establezca el parámetro _lpEIDNewEntryTpl_ en el identificador de entrada de la plantilla seleccionada. El identificador de entrada es la columna de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la fila de la plantilla en la tabla de uso único. Pase 0 en _cbEIDContainer_ y NULL en _lpEIDContainer_. Pase un puntero válido en el parámetro _lppEIDNewEntry_ si desea conservar el identificador de entrada de la nueva entrada. 
    
## <a name="see-also"></a>Recursos adicionales



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport::OpenEntry](imapisupport-openentry.md)
  
[Propiedad canónica PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

