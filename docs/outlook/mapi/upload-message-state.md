---
title: Cargar estado de los mensajes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 430734fe98799c386e71612355b194a6b8edf00a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575416"
---
# <a name="upload-message-state"></a>Cargar estado de los mensajes

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
 En este tema se describe qué ocurre durante el estado del mensaje de carga de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |
|Estructura de datos relacionados:  <br/> |**[UPMSG](upmsg.md)** <br/> |
|Desde este estado:  <br/> |[Cargar el estado de la tabla](upload-table-state.md) <br/> |
|En este estado:  <br/> |Cargar el estado de la tabla  <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es una máquina de estado determinista. Un cliente sale de un estado a otro finalmente debe volver a la primera desde el último. 
  
## <a name="description"></a>Descripción

Este estado inicia la carga de un elemento de Outlook (correo, calendario, contacto, tarea, nota o diario) que es nuevo o se ha movido a la carpeta actual, o que han sido modificado. Outlook inicializa la estructura de datos **UPMSG** de correpsonding con la información apropiada para el elemento, tal y como se agrega, mueve o modifica. 
  
Si el elemento se ha agregado o movido, el cliente, a continuación, adecuadamente agrega o actualiza el elemento en el servidor. 
  
Si el elemento se ha modificado, Outlook aún más especifica en la estructura de datos **UPMSG** si las modificaciones están en un encabezado de mensaje (en cuyo caso el elemento es el encabezado del mensaje), en las propiedades de elemento o en el propio elemento que requiere el conflicto resolución. El cliente, a continuación, actualiza el elemento en el servidor. 
  
Cuando finaliza la carga de elemento, Outlook notas que el mensaje se ha cargado, por lo que no se procesarán en una carga posterior. Devuelve el almacén local en el estado de la tabla de carga.
  
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[ESTADO DE SINCRONIZACIÓN](syncstate.md)

