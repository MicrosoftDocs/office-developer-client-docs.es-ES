---
title: Abrir entradas de la libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 017a62c0-49c6-47fb-acce-db58e6bb9cc5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6ebd6009700742e9b1159bc95ff0496c423e512c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422162"
---
# <a name="opening-address-book-entries"></a>Abrir entradas de la libreta de direcciones

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando un cliente o proveedor ha solicitado que se abra uno de los objetos, MAPI llama al método [IABLogon::OpenEntry del](iablogon-openentry.md) proveedor. MAPI determina que el identificador de entrada que representa el objeto de destino pertenece al proveedor examinando la parte [MAPIUID](mapiuid.md) del identificador de entrada y haciendo coincidir con **el MAPIUID** que el proveedor registró en la llamada a **IMAPISupport::SetProviderUID**. A continuación, MAPI llama **al método OpenEntry.** El proveedor debe responder recuperando el objeto correspondiente: un contenedor, una lista de distribución o un usuario de mensajería. 
  
Un identificador de entrada NULL indica una solicitud para abrir el contenedor raíz del proveedor de libreta de direcciones. Los clientes abren el contenedor raíz para tener acceso a su tabla de jerarquía y a sus destinatarios. Los proveedores de libretas de direcciones que solo suministran plantillas para crear destinatarios de uso único no admiten la llamada **OpenEntry** para el contenedor raíz. 
  
### <a name="to-implement-iablogonopenentry"></a>Para implementar IABLogon::OpenEntry
  
1. Compruebe que el identificador de entrada es un identificador válido compatible con el proveedor. Si no es un identificador de entrada válido, devuelve MAPI_E_INVALID_ENTRYID. 
    
2. Compruebe la marca que se pasa con el _parámetro ulFlags._ Si MAPI ha pasado en MAPI_MODIFY y el proveedor no permite que se modifiquen sus objetos, se produce un error y se devuelve el MAPI_E_ACCESS_DENIED error. 
    
3. Compruebe que la interfaz solicitada en el  _parámetro lpInterface_ es válida para el tipo de objeto que se le ha pedido al proveedor que abra. Si se ha pasado un parámetro no válido, se produce un error y se devuelve MAPI_E_INTERFACE_NOT_SUPPORTED de error. 
    
4. Si el  _parámetro cbEntryID_ es cero, se trata de una solicitud para abrir el contenedor raíz del proveedor. Crea el contenedor raíz y devuelve un puntero a su **implementación de interfaz IABContainer.** 
    
5. Si su proveedor implementa varios objetos de inicio de sesión, cada uno con su **propio MAPIUID** registrado, asigne el **MAPIUID** incluido en el identificador de entrada con el objeto de inicio de sesión adecuado. 
    
6. Determine qué tipo de objeto representa el identificador de entrada: un usuario de mensajería, una lista de distribución o un contenedor que pertenezca a su proveedor o a una lista de distribución o usuario de mensajería de uso único para que se pueda establecer el valor adecuado para el parámetro _lpulObjectType._ 
    
7. Cree el objeto del tipo adecuado y establezca las siguientes propiedades básicas:
    
    - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    - **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
8. Calcule **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) y **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) a partir de la información del identificador de entrada.
    
9. Devuelve un puntero a la implementación de la interfaz para el objeto. 
    

