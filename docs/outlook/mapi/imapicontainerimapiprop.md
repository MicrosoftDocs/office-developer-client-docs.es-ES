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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: e24f5ebd73a4652876282099f1460762c150b94d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817209"
---
# <a name="imapicontainer--imapiprop"></a>IMAPIContainer: IMAPIProp

  
  
**Se aplica a**: Outlook 
  
Administra las operaciones de alto nivel en objetos de contenedor como libretas de direcciones, listas de distribución y las carpetas. El [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md), [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md), y [IDistList: IMAPIContainer](idistlistimapicontainer.md) interfaces se derivan de **IMAPIContainer**.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuestos por:  <br/> |Carpeta, el contenedor de la libreta de direcciones y objetos de lista de distribución  <br/> |
|Se implementa mediante:  <br/> |Almacén de mensajes, la libreta de direcciones y los proveedores de transporte remoto  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIContainer  <br/> |
|Tipo de puntero:  <br/> |LPMAPICONTAINER  <br/> |
|Modelo de transacciones:  <br/> |Clase abstracta, que nunca se ha implementado  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[GetContentsTable](imapicontainer-getcontentstable.md) <br/> |Devuelve un puntero a la tabla de contenido del contenedor.  <br/> |
|[GetHierarchyTable](imapicontainer-gethierarchytable.md) <br/> |Devuelve un puntero a la tabla de jerarquía del contenedor.  <br/> |
|[OpenEntry](imapicontainer-openentry.md) <br/> |Abre un objeto en el contenedor, la devolución de un puntero de interfaz para aún más el acceso.  <br/> |
|[Es posible SetSearchCriteria](imapicontainer-setsearchcriteria.md) <br/> |Establece los criterios de búsqueda para el contenedor.  <br/> |
|[Es posible GetSearchCriteria](imapicontainer-getsearchcriteria.md) <br/> |Obtiene los criterios de búsqueda para el contenedor.  <br/> |
   
|**Propiedades necesarias**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |Es de lectura y escritura.  <br/> |
   
## <a name="see-also"></a>Ver también



[Interfaces MAPI](mapi-interfaces.md)

