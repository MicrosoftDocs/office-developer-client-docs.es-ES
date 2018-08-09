---
title: IABContainer IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer
api_type:
- COM
ms.assetid: 1f5ce6e0-b79a-4da2-b014-8c00cd72912e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0eb6d62b64595474957415e94275d0ac52cc2b6b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817085"
---
# <a name="iabcontainer--imapicontainer"></a>IABContainer : IMAPIContainer

**Hace referencia a**: Outlook 
  
Proporciona acceso a los contenedores de la libreta de direcciones. MAPI y las aplicaciones cliente llame a los métodos de **IABContainer** para realizar la resolución de nombres y para crear, copiar y eliminación a los destinatarios. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuestos por:  <br/> |Objetos de contenedor de la libreta de direcciones  <br/> |
|Se implementa mediante:  <br/> |Proveedores de la libreta de direcciones  <br/> |
|Llamado por:  <br/> |MAPI y las aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IABContainer  <br/> |
|Tipo de puntero:  <br/> |LPABCONT  <br/> |
|Modelo de transacciones:  <br/> |Negocian  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[CreateEntry](iabcontainer-createentry.md) <br/> |Crea una nueva entrada, que puede ser un usuario de mensajería, una lista de distribución u otro contenedor.  <br/> |
|[CopyEntries](iabcontainer-copyentries.md) <br/> |Copia las entradas de uno o más, los usuarios normalmente mensajería o listas de distribución.  <br/> |
|[DeleteEntries](iabcontainer-deleteentries.md) <br/> |Quita una o más entradas, normalmente otros contenedores, listas de distribución o a los usuarios de mensajería.  <br/> |
|[ResolveNames](iabcontainer-resolvenames.md) <br/> |Realiza la resolución de nombres para una o más entradas de destinatarios.  <br/> |
   
|**Propiedades requeridas**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |Es de lectura y escritura.  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Es de lectura y escritura.  <br/> |
|**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Solo lectura  <br/> |
   
|**Propiedades opcionales**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Solo lectura  <br/> |
   
## <a name="remarks"></a>Comentarios

La interfaz de **IABContainer** indirectamente hereda de la interfaz [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) a través de la [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) y [IMAPIProp: IUnknown](imapipropiunknown.md) interfaces. Los proveedores de la libreta de direcciones implementan la interfaz de **IABContainer** . 
  
Puede existir cualquier número de objetos de mensajería de usuario, listas de distribución y otros contenedores de libretas de direcciones en un contenedor de la libreta de direcciones. Al igual que con cualquier contenedor, los clientes o proveedores de servicios pueden usar un contenedor de la libreta de direcciones para abrir una de sus entradas o para recuperar una tabla de jerarquías o una tabla de contenido. Contenedores de la libreta de direcciones también proporcionan resolución de nombres y, según el proveedor, la capacidad de agregar, quitar o modificar las entradas.
  
MAPI define un contenedor de libreta de direcciones especial denominado la libreta de direcciones personales (PAB) que contiene las entradas que se copió desde otros contenedores. Una PAB siempre es modificable. Normalmente, los usuarios rellenan su PAB con las entradas de la designación de los destinatarios con el que se comunican con más frecuencia. Una PAB también puede contener direcciones de uso único y nuevos destinatarios todavía no está una parte de cualquier contenedor de la libreta de direcciones.
  
## <a name="see-also"></a>Vea también

- [Interfaces MAPI](mapi-interfaces.md)

