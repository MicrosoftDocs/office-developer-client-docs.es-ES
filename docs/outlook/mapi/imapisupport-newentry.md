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
ms.openlocfilehash: 3468e4a92787e440f230d60ab31f37526fe7d5e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405460"
---
# <a name="imapisupportnewentry"></a>IMAPISupport::NewEntry

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Agrega un nuevo destinatario directamente a un contenedor de libreta de direcciones o a la lista de destinatarios de un mensaje saliente.
  
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
  
> [entrada] Reservado; debe ser cero.
    
 _cbEIDContainer_
  
> a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEIDContainer_ . 
    
 _lpEIDContainer_
  
> a Un puntero al identificador de entrada del contenedor que va a recibir la nueva entrada. Si _cbEIDContainer_ es 0 y _lpEIDContainer_ es null, **NEWENTRY** crea un identificador de entrada único que es del mismo tipo que se genera mediante una llamada al método [IMAPISupport:: CreateOneOff](imapisupport-createoneoff.md) . 
    
 _cbEIDNewEntryTpl_
  
> a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEIDNewEntryTpl_ . 
    
 _lpEIDNewEntryTpl_
  
> a Un puntero al identificador de entrada de la plantilla que se va a utilizar para crear la nueva entrada. Si _cbEIDNewEntryTpl_ es 0 y _lpEIDNewEntryTpl_ es null, **NEWENTRY** muestra un cuadro de diálogo que permite al usuario seleccionar en una lista de plantillas para agregar nuevas entradas. 
    
 _lpcbEIDNewEntry_
  
> contempla Un puntero al recuento de bytes en el identificador de entrada al que apunta el parámetro _lppEIDNewEntry_ . 
    
 _lppEIDNewEntry_
  
> contempla Un puntero a un puntero al identificador de entrada de la entrada recién creada.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La nueva entrada se ha creado correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport:: NEWENTRY** se implementa para los objetos de compatibilidad del proveedor de la libreta de direcciones. Los proveedores de la libreta de direcciones llaman a **NEWENTRY** para crear una nueva entrada de la libreta de direcciones que se agregue directamente a un contenedor o para que se use para dirigir un mensaje saliente. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si desea que la nueva entrada se agregue a un contenedor específico, establezca _lpEIDContainer_ en el identificador de entrada del contenedor y _cbEIDContainer_ en el recuento de bytes en el identificador de entrada. 
  
Si desea que la nueva entrada se agregue a la lista de destinatarios de un mensaje saliente, establezca _lpEIDContainer_ en NULL y _cbEIDContainer_ en 0. 
  
Si desea permitir que el usuario de una aplicación cliente seleccione el tipo de entrada que se va a crear, pase 0 en _cbEIDNewEntryTpl_ y null en _lpEIDNewEntryTpl_. **NEWENTRY** muestra la tabla única de MAPI, una lista de plantillas que MAPI y cada proveedor de la libreta de direcciones en la sesión admiten. Cada plantilla puede crear una entrada de destinatario para uno o más tipos de dirección. 
  
Si desea conservar el identificador de entrada de la nueva entrada, pase punteros válidos en los parámetros _lpcbEIDNewEntry_ y _lppEIDNewEntry_ . Usted es responsable de liberar este identificador de entrada cuando termine con él llamando a la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Para usar una plantilla determinada para agregar una nueva entrada a un contenedor modificable, use el siguiente procedimiento:
  
1. Llame al método [IMAPISupport:: OpenEntry](imapisupport-openentry.md) para abrir el contenedor de destino y establezca el parámetro _lpEntryID_ en el identificador de entrada del contenedor. 
    
2. Llame al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) del contenedor de destino y establezca el parámetro _ulPropTag_ en **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) y el parámetro _lpiid_ en IID_IMAPITable. El contenedor devolverá una tabla única en la que se enumeran todas las plantillas compatibles para crear nuevas entradas. 
    
3. Recupere la fila que representa la plantilla para el tipo concreto de entrada que desea crear. La columna **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) indica el tipo de dirección que es compatible con la plantilla. 
    
4. Llame a **IMAPISupport:: NEWENTRY** y establezca el parámetro _lpEIDNewEntryTpl_ en el identificador de entrada de la plantilla seleccionada. El identificador de entrada es la **** columna 1 ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la fila de la plantilla en la tabla de uso único. Pase 0 en _cbEIDContainer_ y null en _lpEIDContainer_. Pase un puntero válido en el parámetro _lppEIDNewEntry_ si desea conservar el identificador de entrada de la nueva entrada. 
    
## <a name="see-also"></a>Ver también



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport::OpenEntry](imapisupport-openentry.md)
  
[Propiedad canónica PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

