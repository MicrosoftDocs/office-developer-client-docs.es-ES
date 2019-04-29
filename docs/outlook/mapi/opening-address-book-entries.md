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
  
Cuando un cliente o proveedor solicita que se abra uno de los objetos, MAPI llama al método [IABLogon:: OpenEntry](iablogon-openentry.md) del proveedor. MAPI determina que el identificador de entrada que representa el objeto de destino pertenece al proveedor mediante el examen de la parte [MAPIUID](mapiuid.md) del identificador de entrada y su correspondencia con el **MAPIUID** que su proveedor ha registrado en la llamada a ** IMAPISupport:: SetProviderUID**. MAPI, a continuación, llama al método **OpenEntry** . El proveedor debe responder recuperando el objeto correspondiente: un contenedor, una lista de distribución o un usuario de mensajería. 
  
Un identificador de entrada NULL indica una solicitud para abrir el contenedor raíz del proveedor de la libreta de direcciones. Los clientes abren el contenedor raíz para acceder a su tabla de jerarquía y a sus destinatarios. Los proveedores de libreta de direcciones que solo proporcionan plantillas para crear destinatarios únicos no admiten la llamada **OpenEntry** para el contenedor raíz. 
  
### <a name="to-implement-iablogonopenentry"></a>Para implementar IABLogon:: OpenEntry
  
1. Compruebe que el identificador de entrada es un identificador válido que admite su proveedor. Si no es un identificador de entrada válido, devuelve MAPI_E_INVALID_ENTRYID. 
    
2. Compruebe la marca que se pasa con el parámetro _ulFlags_ . Si MAPI se ha pasado en MAPI_MODIFY y el proveedor no permite que se modifiquen sus objetos, se produce un error y se devuelve el valor de error MAPI_E_ACCESS_DENIED. 
    
3. Compruebe que la interfaz solicitada en el parámetro _lpInterface_ es válida para el tipo de objeto al que se ha solicitado que se abra el proveedor. Si se ha pasado un parámetro no válido, se produce un error y se devuelve el valor de error MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
4. Si el parámetro _cbEntryID_ es cero, se trata de una solicitud para abrir el contenedor raíz del proveedor. Cree el contenedor raíz y devuelva un puntero a su implementación de interfaz **IABContainer** . 
    
5. Si el proveedor implementa varios objetos de inicio de sesión, cada uno con su propio **MAPIUID**registrado, asigne el **MAPIUID** contenido en el identificador de entrada con el objeto de inicio de sesión adecuado. 
    
6. DeTermine el tipo de objeto que representa el identificador de entrada: un usuario de mensajería, una lista de distribución o un contenedor perteneciente a su proveedor o un usuario de mensajería de un solo uso o una lista de distribución para que se pueda establecer el valor adecuado para el _lpulObjectType_ parámetro. 
    
7. Cree el objeto del tipo adecuado y establezca las siguientes propiedades básicas:
    
    - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    - **** Es ([PidTagEntryId](pidtagentryid-canonical-property.md))
    - **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
8. Calcula **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) y **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) desde la información del identificador de entrada.
    
9. Devolver un puntero a la implementación de la interfaz para el objeto. 
    

