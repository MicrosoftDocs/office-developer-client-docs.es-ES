---
title: IMAPIContainer IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer
api_type:
- COM
ms.assetid: d83fdd83-3e86-43c8-a73f-8e9e01b53371
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8be3b1857d539f81e42d2ac3e5813afa73513a16
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406125"
---
# <a name="imapicontainer--imapiprop"></a>IMAPIContainer : IMAPIProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Administra operaciones de alto nivel en objetos contenedor, como libretas de direcciones, listas de distribución y carpetas. Las [interfaces IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)y [IDistList : IMAPIContainer](idistlistimapicontainer.md) se derivan de **IMAPIContainer**.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuesto por:  <br/> |Carpeta, contenedor de libreta de direcciones y objetos de lista de distribución  <br/> |
|Implementado por:  <br/> |Proveedores de almacenamiento de mensajes, libreta de direcciones y transporte remoto  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIContainer  <br/> |
|Tipo de puntero:  <br/> |LPMAPICONTAINER  <br/> |
|Modelo de transacciones:  <br/> |Clase abstracta, nunca implementada  <br/> |
   
## <a name="vtable-order"></a>Orden de Vtable

|||
|:-----|:-----|
|[GetContentsTable](imapicontainer-getcontentstable.md) <br/> |Devuelve un puntero a la tabla de contenido del contenedor.  <br/> |
|[GetHierarchyTable](imapicontainer-gethierarchytable.md) <br/> |Devuelve un puntero a la tabla de jerarquía del contenedor.  <br/> |
|[OpenEntry](imapicontainer-openentry.md) <br/> |Abre un objeto en el contenedor y devuelve un puntero de interfaz para obtener más acceso.  <br/> |
|[SetSearchCriteria](imapicontainer-setsearchcriteria.md) <br/> |Establece criterios de búsqueda para el contenedor.  <br/> |
|[GetSearchCriteria](imapicontainer-getsearchcriteria.md) <br/> |Obtiene los criterios de búsqueda del contenedor.  <br/> |
   
|**Propiedades requeridas**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |Lectura/escritura  <br/> |
   
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

