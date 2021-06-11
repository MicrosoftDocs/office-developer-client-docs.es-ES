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
ms.openlocfilehash: 0905fbe2ba584aef49c50152aaf448267d477c10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348961"
---
# <a name="iabcontainer--imapicontainer"></a>IABContainer : IMAPIContainer

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona acceso a contenedores de libreta de direcciones. MAPI y las aplicaciones cliente llaman a los métodos **de IABContainer** para realizar la resolución de nombres y crear, copiar y eliminar destinatarios. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuesto por:  <br/> |Objetos contenedor de libreta de direcciones  <br/> |
|Implementado por:  <br/> |Proveedores de libreta de direcciones  <br/> |
|Llamado por:  <br/> |MAPI y aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IABContainer  <br/> |
|Tipo de puntero:  <br/> |LPABCONT  <br/> |
|Modelo de transacciones:  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Orden de Vtable

|||
|:-----|:-----|
|[CreateEntry](iabcontainer-createentry.md) <br/> |Crea una nueva entrada, que puede ser un usuario de mensajería, una lista de distribución u otro contenedor.  <br/> |
|[CopyEntries](iabcontainer-copyentries.md) <br/> |Copia una o más entradas, normalmente usuarios de mensajería o listas de distribución.  <br/> |
|[DeleteEntries](iabcontainer-deleteentries.md) <br/> |Quita una o más entradas, normalmente usuarios de mensajería, listas de distribución u otros contenedores.  <br/> |
|[ResolveNames](iabcontainer-resolvenames.md) <br/> |Realiza la resolución de nombres para una o más entradas de destinatarios.  <br/> |
   
|**Propiedades requeridas**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |Lectura/escritura  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lectura/escritura  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Solo lectura  <br/> |
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

La **interfaz IABContainer** hereda indirectamente de la interfaz [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) a través de las interfaces [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) e [IMAPIProp : IUnknown.](imapipropiunknown.md) Los proveedores de libreta de direcciones implementan la **interfaz IABContainer.** 
  
Cualquier número de objetos de usuario de mensajería, listas de distribución y otros contenedores de libreta de direcciones puede existir en un contenedor de libreta de direcciones. Al igual que con cualquier contenedor, los clientes o proveedores de servicios pueden usar un contenedor de libreta de direcciones para abrir una de sus entradas o para recuperar una tabla de jerarquía o una tabla de contenido. Los contenedores de libreta de direcciones también proporcionan resolución de nombres y, según el proveedor, la capacidad de agregar, quitar o modificar entradas.
  
MAPI define un contenedor especial de libreta de direcciones denominado libreta de direcciones personal (PAB) que contiene entradas copiadas de otros contenedores. Un PAB siempre es modificable. Los usuarios suelen rellenar su PAB con entradas que designan los destinatarios con los que se comunican con más frecuencia. Una PAB también puede contener direcciones únicas y nuevos destinatarios que aún no forman parte de ningún contenedor de libreta de direcciones.
  
## <a name="see-also"></a>Vea también

- [Interfaces MAPI](mapi-interfaces.md)

