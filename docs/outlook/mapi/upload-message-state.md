---
title: Cargar estado de mensaje
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 61cda23557a501a2651385d192f1dc7432ef1cb5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433804"
---
# <a name="upload-message-state"></a>Cargar estado de mensaje

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 En este tema se describe lo que sucede durante el estado del mensaje de carga de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |
|Estructura de datos relacionados:  <br/> |**[UPMSG](upmsg.md)** <br/> |
|Desde este estado:  <br/> |[Cargar el estado de la tabla](upload-table-state.md) <br/> |
|A este estado:  <br/> |Cargar el estado de la tabla  <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es una máquina de estado determinista. Un cliente que va de un estado a otro debe volver al primero desde el segundo. 
  
## <a name="description"></a>Description

Este estado inicia la carga de un elemento de Outlook (correo, calendario, contacto, tarea, nota o diario) nuevo o que se ha movido a la carpeta actual o que se ha modificado. Outlook inicializa la estructura de datos **UPMSG** de correpsonding con la información adecuada para el elemento que se va a agregar, mover o modificar. 
  
Si el elemento se ha agregado o movido, el cliente agrega o actualiza correctamente el elemento en el servidor. 
  
Si se ha modificado el elemento, Outlook especifica aún más en la estructura de datos **UPMSG** si las modificaciones están en un encabezado de mensaje (en cuyo caso el elemento es el encabezado del mensaje), en las propiedades del elemento o en el propio elemento que requiere la resolución de conflictos. A continuación, el cliente actualiza el elemento en el servidor. 
  
Cuando finaliza la carga del elemento, Outlook indica que el mensaje se ha cargado, por lo que no se procesará en una carga posterior. El almacén local vuelve al estado de la tabla de carga.
  
## <a name="see-also"></a>Consulte también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

