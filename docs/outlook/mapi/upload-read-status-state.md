---
title: Cargar estado de lectura de estado
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 41815a88fe1215d2a85a38592e04b0d0bbd43cc6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573050"
---
# <a name="upload-read-status-state"></a>Cargar estado de lectura de estado

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 En este tema se describe qué ocurre durante la carga leer el estado del estado de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |
|Estructura de datos relacionados:  <br/> |**[UPREAD](upread.md)** <br/> |
|Desde este estado:  <br/> |[Cargar el estado de la tabla](upload-table-state.md) <br/> |
|En este estado:  <br/> |Cargar el estado de la tabla  <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es una máquina de estado determinista. Un cliente sale de un estado a otro finalmente debe volver a la primera desde el último. 
  
## <a name="description"></a>Descripción

Este estado inicia carga el estado de lectura de elementos en una carpeta especificada en un estado de tabla de carga anterior. Durante este estado, Outlook inicializa la estructura de datos **UPREAD** asociada con información para esos elementos en la carpeta cuyo estado de lectura ha cambiado. El cliente, a continuación, actualiza el estado de lectura de estos elementos en el servidor como leídos o no leídos. 
  
Cuando finaliza este estado, Outlook borra la información interna sobre el estado de lectura del elemento, impide que el estado de lectura del elemento que se está cargando nuevamente. Devuelve el almacén local en el estado de la tabla de carga.
  
## <a name="see-also"></a>Recursos adicionales



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[ESTADO DE SINCRONIZACIÓN](syncstate.md)

