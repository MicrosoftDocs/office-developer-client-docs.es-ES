---
title: Upload Estado de eliminación
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dda9d23a572446a5fa79a9500eb69558b6e0debd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425844"
---
# <a name="upload-delete-status-state"></a>Upload Estado de eliminación

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 En este tema se describe lo que sucede durante el estado de eliminación de carga de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |
|Estructura de datos relacionada:  <br/> |**[UPDEL](updel.md)** <br/> |
|Desde este estado:  <br/> |[Upload de tabla](upload-table-state.md) <br/> |
|A este estado:  <br/> |Upload de tabla  <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es una máquina de estado determinista. Un cliente que sale de un estado a otro debe volver al primero desde el segundo. 
  
## <a name="description"></a>Descripción

Este estado inicia la actualización en un servidor de los elementos Outlook (correo, calendario, contacto, tarea, nota o diario) que se han eliminado en una carpeta de un almacén local especificado en un estado de tabla de carga anterior. Durante este estado, Outlook inicializa los miembros de la estructura de datos **UPDEL** asociada con información de los elementos que se han eliminado o movido de la carpeta. 
  
A continuación, el cliente elimina los elementos especificados en la carpeta del servidor. Para distinguir los elementos que se han movido en lugar de eliminarse, el cliente debe comprobar los *miembros de pupmov* identificados en la **estructura UPDEL.** 
  
Cuando finaliza este estado, Outlook borra la información interna que indica que el elemento se ha eliminado; por lo tanto, Outlook ya no tendrá un registro del elemento. El almacén local vuelve al estado de la tabla de carga.
  
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

