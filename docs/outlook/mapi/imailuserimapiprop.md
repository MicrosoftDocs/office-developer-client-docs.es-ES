---
title: IMailUser IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMailUser
api_type:
- COM
ms.assetid: 74c25870-62d9-484a-9a99-4dc35c52479e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a0e109fe95120483e700bab5b82f6d7cb75e2e28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436597"
---
# <a name="imailuser--imapiprop"></a>IMailUser : IMAPIProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona acceso a las muchas propiedades asociadas con los usuarios de mensajería. La **interfaz IMailUser** se implementa mediante objetos de usuario de mensajería. **IMailUser** hereda de la [interfaz IMAPIProp : IUnknown](imapipropiunknown.md) y no tiene métodos únicos propios. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuesto por:  <br/> |Objetos de usuario de mensajería  <br/> |
|Implementado por:  <br/> |Proveedores de libretas de direcciones  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IMailUser  <br/> |
|Tipo de puntero:  <br/> |LPMAILUSER  <br/> |
|Modelo de transacción:  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Orden de tabla virtual

Esta interfaz no tiene ningún método único.
  
|**Propiedades requeridas**|**Access**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Lectura/escritura  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lectura/escritura  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Lectura/escritura  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Solo lectura  <br/> |
   
## <a name="remarks"></a>Comentarios

Cinco de las propiedades necesarias se conocen como propiedades de dirección base para los destinatarios:
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_SEARCH_KEY**
    
Estas propiedades se consideran especiales porque muchos otros grupos de propiedades similares se basan en este grupo base. Los demás grupos se usan para describir un destinatario en varios roles, como el remitente original o delegado de un mensaje. Para obtener más información acerca de estas propiedades y cómo usarlas, vea [Tipos de direcciones MAPI](mapi-address-types.md).
  
Los usuarios de mensajería pueden mostrar una colección de sus propiedades si admiten **la PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). **PR_DETAILS_TABLE** es una tabla para mostrar que describe el diseño de un cuadro de diálogo de detalles o una página de propiedades con fichas que muestra la información de la propiedad del destinatario. MAPI crea cuadros de diálogo de detalles cuando un cliente llama al [método IAddrBook::D etails.](iaddrbook-details.md) 
  
Los objetos de usuario de mensajería pueden tener otras propiedades opcionales asociadas. MAPI define muchas propiedades que proporcionan información de direccionamiento adicional sobre un usuario de mensajería. Todas estas propiedades son cadenas de caracteres. En la siguiente lista se muestran las propiedades más usadas:
  
- **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) 
    
- **PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md)) 
    
- **PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md)) 
    
- **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) 
    
- **PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md)) 
    
- **PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md)) 
    
- **PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md)) 
    
Para obtener una lista completa de propiedades, vea [Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md).
  
## <a name="see-also"></a>Consulte también



[Interfaces MAPI](mapi-interfaces.md)

