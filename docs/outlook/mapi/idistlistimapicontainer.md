---
title: IDistList IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IDistList
api_type:
- COM
ms.assetid: bd8e1ddb-3027-428b-8964-81614f80282d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 463d81a6692b6071cada0ad22e7343020563e41c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431550"
---
# <a name="idistlist--imapicontainer"></a>IDistList : IMAPIContainer

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona acceso a listas de distribución en contenedores modificables de libreta de direcciones. **IDistList puede** crear, copiar y eliminar listas de distribución, además de realizar la resolución de nombres. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuesto por:  <br/> |Objetos de lista de distribución  <br/> |
|Implementado por:  <br/> |Proveedores de libretas de direcciones  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IDistList  <br/> |
|Tipo de puntero:  <br/> |LPDISTLIST  <br/> |
|Modelo de transacción:  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Orden de tabla virtual

Esta interfaz no tiene ningún método único.
  
|**Propiedades requeridas**|**Access**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Lectura/escritura  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lectura/escritura  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Solo lectura  <br/> |
   
## <a name="remarks"></a>Comentarios

La **interfaz IDistList** hereda de [IMAPIContainer](imapicontainerimapiprop.md) e incluye los mismos métodos que los contenedores de libreta de direcciones. Por lo tanto, dado que los métodos de la **interfaz IDistList** son idénticos a los de la interfaz [IABContainer,](iabcontainerimapicontainer.md) no se duplican aquí. 
  
Una lista de distribución u objeto que implementa **IDistList** es una colección de objetos de usuario de mensajería o destinatarios individuales. Una lista de distribución puede constar de todos los objetos de usuario de mensajería o de algunos usuarios de mensajería y algunas listas de distribución. 
  
Normalmente hay dos tipos de listas de distribución:
  
- Listas de distribución expandida por el sistema de mensajería subyacente. Este tipo de lista tiene una dirección, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), y se trata igual que si fuera un destinatario individual. 
    
- Listas de distribución que existen en un contenedor local y que la aplicación cliente expande.
    
Entre las propiedades opcionales de la lista de distribución se incluyen las siguientes:
  
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) 
    
- **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) 
    
Observe que **PR_ADDRTYPE** es necesario, pero **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) no lo es. Esto se debe a que una lista de distribución sin una dirección de correo electrónico aún puede recibir mensajes, pero su lista de miembros debe expandirse. Si la **PR_ADDRTYPE** se establece en MAPIPDL, MAPI realiza la expansión. Si **PR_ADDRTYPE** es un valor distinto de MAPIPDL, el proveedor de transporte realiza la expansión. 
  
Para obtener información adicional sobre cómo usar los **métodos IDistList,** consulta las entradas de referencia de los métodos paralelos de **IABContainer**.
  
## <a name="see-also"></a>Consulte también



[Interfaces MAPI](mapi-interfaces.md)

