---
title: Upload Estado de jerarquía
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39c4198-4913-5e86-900a-32e5ba5d801c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f789f4d7bbaf585d0d80f2208c35313542dfc191
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415428"
---
# <a name="upload-hierarchy-state"></a>Upload Estado de jerarquía

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 En este tema se describe lo que sucede durante el estado de la jerarquía de carga de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |
|Estructura de datos relacionada:  <br/> |**[UPHIER](uphier.md)** <br/> |
|Desde este estado:  <br/> |[Estado de sincronización](synchronize-state.md) <br/> |
|A este estado:  <br/> |[Upload de carpeta o](upload-folder-state.md)sincronizar el estado  <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es una máquina de estado determinista. Un cliente que se va de un estado a otro debe volver finalmente al primero desde el segundo. 
  
## <a name="description"></a>Descripción

Este estado inicia la carga de una jerarquía de árbol de carpetas que se ha especificado en un estado de sincronización anterior. Outlook determina el número de carpetas que se han creado o modificado en esa jerarquía e inicializa *cEnt* en **UPHIER**. Outlook también mantiene un recuento del número de carpetas cargadas con otro *miembro iEnt* . Para cargar cada una de las carpetas  *de cEnt,*  el cliente mueve el almacén local al estado de la carpeta de carga, volviendo al estado de jerarquía de carga cuando finaliza la carga de la carpeta. 
  
Cuando finaliza el estado de la jerarquía de carga, el almacén local vuelve al estado de sincronización.
  
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

