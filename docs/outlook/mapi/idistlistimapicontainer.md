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
ms.openlocfilehash: 7fee3c84d6a4d4a94397f5197f45637b0c7dd2be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817187"
---
# <a name="idistlist--imapicontainer"></a>IDistList : IMAPIContainer

  
  
**Hace referencia a**: Outlook 
  
Proporciona acceso a listas de distribución en dirección modificable contenedores de libretas. **IDistList** puede crear, copiar y eliminar listas de distribución, además de realizar la resolución de nombres. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuestos por:  <br/> |Objetos de lista de distribución  <br/> |
|Se implementa mediante:  <br/> |Proveedores de la libreta de direcciones  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IDistList  <br/> |
|Tipo de puntero:  <br/> |LPDISTLIST  <br/> |
|Modelo de transacciones:  <br/> |Negocian  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

Esta interfaz no tiene ningún método único.
  
|**Propiedades requeridas**|**Access**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Es de lectura y escritura.  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Es de lectura y escritura.  <br/> |
|**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Solo lectura  <br/> |
   
## <a name="remarks"></a>Comentarios

La interfaz de **IDistList** hereda de [IMAPIContainer](imapicontainerimapiprop.md) e incluye los mismos métodos que los contenedores de la libreta de direcciones. Por lo tanto, debido a que los métodos de la interfaz de **IDistList** son idénticos a las de la interfaz [IABContainer](iabcontainerimapicontainer.md) , no se duplican aquí. 
  
Una lista de distribución o un objeto que implementa **IDistList** es una colección de objetos de usuario de mensajería o destinatarios individuales. Una lista de distribución puede constar de todos los objetos de usuario mensajería, o algún usuario de mensajería y algunas listas de distribución. 
  
Normalmente, existen dos tipos de listas de distribución:
  
- En las listas de distribución se expanden por el sistema de mensajería subyacente. Este tipo de lista tiene una dirección, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) y es el mismo se trata como si fuese un destinatario individual. 
    
- Listas de distribución que existen en un contenedor local y se expanden por la aplicación cliente.
    
Propiedades de la lista de distribución opcional incluyen las siguientes:
  
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) 
    
- **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) 
    
Observe que **PR_ADDRTYPE** es necesario, pero no es de **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)). Eso es porque una lista de distribución sin una dirección de correo electrónico puede seguir recibiendo mensajes, pero se debe expandir la lista de miembros. Si se establece la propiedad **PR_ADDRTYPE** en MAPIPDL, MAPI realiza la expansión. Si **PR_ADDRTYPE** es un valor distinto de MAPIPDL, el proveedor de transporte lleva a cabo la expansión. 
  
Para obtener información adicional acerca de cómo usar los métodos **IDistList** , vea las entradas de referencia para los métodos paralelos de **IABContainer**.
  
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

