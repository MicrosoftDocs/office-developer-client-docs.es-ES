---
title: Entradas de la libreta de direcciones de apertura
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 017a62c0-49c6-47fb-acce-db58e6bb9cc5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: cd86b9cc86f30aac75b732b97208933de4d336e9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566435"
---
# <a name="opening-address-book-entries"></a>Entradas de la libreta de direcciones de apertura

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando un cliente o proveedor ha solicitado que se abra uno de los objetos, MAPI llama al método [IABLogon::OpenEntry](iablogon-openentry.md) de su proveedor. MAPI determina que el identificador de entrada que representa el objeto de destino pertenece a su proveedor de examinando la parte [MAPIUID](mapiuid.md) del identificador de entrada y coincidencia a **MAPIUID** que su proveedor registrado en la llamada a ** IMAPISupport::SetProviderUID**. MAPI, a continuación, llama al método **OpenEntry** . El proveedor debe responder, se recupera el objeto correspondiente: un contenedor, una lista de distribución o un usuario de mensajería. 
  
Un identificador de entrada NULL indica una solicitud para abrir el contenedor de raíz del proveedor de libreta de direcciones. Los clientes de abren el contenedor de raíz para tener acceso a su tabla de jerarquía y sus destinatarios. Los proveedores de la libreta de direcciones que sólo proporcionar plantillas para la creación de los destinatarios de este tipo no admite la llamada **OpenEntry** para el contenedor raíz. 
  
### <a name="to-implement-iablogonopenentry"></a>Para implementar IABLogon::OpenEntry
  
1. Compruebe que el identificador de entrada es un identificador válido que admita el proveedor. Si no es un identificador de entrada válido, devolver MAPI_E_INVALID_ENTRYID. 
    
2. Comprobar la marca que se pasa con el parámetro _ulFlags indicado_ . Si ha pasado MAPI en MAPI_MODIFY y su proveedor no admite sus objetos que desea modificar, se producirá un error y devolver el valor de error MAPI_E_ACCESS_DENIED. 
    
3. Compruebe que la interfaz solicitada en el parámetro _lpInterface_ es válida para el tipo de objeto que se le ha pedido para abrir su proveedor. Si se ha pasado un parámetro no válido, se producirá un error y devolver el valor de error MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
4. Si el parámetro _cbEntryID_ es cero, esto es una solicitud para abrir el contenedor de raíz de su proveedor. Crear el contenedor de raíz y devolver un puntero a su implementación de la interfaz **IABContainer** . 
    
5. Si su proveedor implementa varios objetos de inicio de sesión, cada uno con su propio registrado **MAPIUID**, mapa la **MAPIUID** contenidos en el identificador de entrada con el objeto de inicio de sesión adecuado. 
    
6. Determinar qué tipo del objeto que representa el identificador de entrada: un usuario, lista de distribución o contenedor que pertenecen a su proveedor o una dirección de uso único mensajería usuario o lista de distribución para que se puede establecer el valor apropiado para la _lpulObjectType_ mensajería parámetro. 
    
7. Crear el objeto del tipo adecuado y establezca las propiedades básicas siguientes:
    
    - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    - **Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    - **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
8. Calcular **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) y **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de la información en el identificador de entrada.
    
9. Devolver un puntero a la implementación de la interfaz para el objeto. 
    

