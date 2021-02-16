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

## <a name="parameters"></a>Parámetros

 _ulUIParam_
  
> [entrada] Identificador de la ventana principal del cuadro de diálogo.
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _cbEIDContainer_
  
> [entrada] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEIDContainer._ 
    
 _lpEIDContainer_
  
> [entrada] Puntero al identificador de entrada del contenedor para recibir la nueva entrada. Si _cbEIDContainer_ es 0 y _lpEIDContainer_ es NULL, **NewEntry** crea un identificador de entrada de uso único que es del mismo tipo que se genera mediante una llamada al método [IMAPISupport::CreateOneOff.](imapisupport-createoneoff.md) 
    
 _cbEIDNewEntryTpl_
  
> [entrada] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEIDNewEntryTpl._ 
    
 _lpEIDNewEntryTpl_
  
> [entrada] Puntero al identificador de entrada de la plantilla que se usará para crear la nueva entrada. Si  _cbEIDNewEntryTpl_ es 0 y  _lpEIDNewEntryTpl_ es NULL, **NewEntry** muestra un cuadro de diálogo que permite al usuario seleccionar de una lista de plantillas para agregar nuevas entradas. 
    
 _lpcbEIDNewEntry_
  
> [salida] Puntero al recuento de bytes en el identificador de entrada al que apunta el parámetro _lppEIDNewEntry._ 
    
 _lppEIDNewEntry_
  
> [salida] Puntero a un puntero al identificador de entrada de la entrada recién creada.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La nueva entrada se creó correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::NewEntry** se implementa para objetos de compatibilidad del proveedor de libreta de direcciones. Los proveedores de libretas de direcciones llaman a **NewEntry** para crear una nueva entrada de libreta de direcciones que se agregará directamente a un contenedor o que se usará para dirigir un mensaje saliente. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si quieres agregar la nueva entrada a un contenedor específico, establece  _lpEIDContainer_ en el identificador de entrada del contenedor y  _cbEIDContainer_ en el recuento de bytes en el identificador de entrada. 
  
Si quieres agregar la nueva entrada a la lista de destinatarios de un mensaje saliente, establece  _lpEIDContainer_ en NULL y  _cbEIDContainer_ en 0. 
  
Si desea permitir que el usuario de una aplicación cliente seleccione el tipo de entrada que se va a crear, pase 0 en  _cbEIDNewEntryTpl_ y NULL en  _lpEIDNewEntryTpl_. **NewEntry** muestra la tabla de uso único de MAPI, una lista de plantillas que MAPI y cada uno de los proveedores de libretas de direcciones admiten en la sesión. Cada plantilla puede crear una entrada de destinatario para uno o varios tipos de dirección. 
  
Si desea conservar el identificador de entrada de la nueva entrada, pase punteros válidos en los parámetros _lpcbEIDNewEntry_ e _lppEIDNewEntry._ Eres responsable de liberar este identificador de entrada cuando termines con él llamando a la [función MAPIFreeBuffer.](mapifreebuffer.md) 
  
Para usar una plantilla determinada para agregar una nueva entrada a un contenedor modificable, use el siguiente procedimiento:
  
1. Llame al [método IMAPISupport::OpenEntry](imapisupport-openentry.md) para abrir el contenedor de destino y establezca el parámetro  _lpEntryID_ en el identificador de entrada del contenedor. 
    
2. Llame al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del contenedor de destino y establezca el parámetro  _ulPropTag_ en **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) y el parámetro  _lpiid_ en IID_IMAPITable. El contenedor devolverá una tabla de uso único que enumera todas las plantillas que admite para crear nuevas entradas. 
    
3. Recupere la fila que representa la plantilla para el tipo concreto de entrada que desea crear. La **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) indica el tipo de dirección admitido por la plantilla. 
    
4. Llame **a IMAPISupport::NewEntry** y establezca el parámetro  _lpEIDNewEntryTpl_ en el identificador de entrada de la plantilla seleccionada. El identificador de entrada **es PR_ENTRYID** columna ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la fila de la plantilla en la tabla de un solo elemento. Pase 0 en  _cbEIDContainer y_ NULL en  _lpEIDContainer_. Pase un puntero válido en  _el parámetro lppEIDNewEntry_ si desea conservar el identificador de entrada de la nueva entrada. 
    
## <a name="see-also"></a>Consulte también



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport::OpenEntry](imapisupport-openentry.md)
  
[Propiedad canónica PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

