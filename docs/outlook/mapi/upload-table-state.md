---
title: Cargar estado de la tabla
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bd54c30e8701a13637235e28ddcfef4c21d10a2b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576984"
---
# <a name="upload-table-state"></a>Cargar estado de la tabla

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 En este tema se describe qué ocurre durante el estado de la tabla de carga de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |
|Estructura de datos relacionados:  <br/> |**[UPTBL](uptbl.md)** <br/> |
|Desde este estado:  <br/> |[Sincronizar el estado del contenido](synchronize-contents-state.md) <br/> |
|En este estado:  <br/> |[Cargar el estado del mensaje](upload-message-state.md), [estado de estado de eliminación de carga](upload-delete-status-state.md), [leer el estado del estado de carga](upload-read-status-state.md), o sincronizar el estado del contenido  <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es una máquina de estado determinista. Un cliente sale de un estado a otro finalmente debe volver a la primera desde el último. 
  
## <a name="description"></a>Descripción

Este estado inicia carga el contenido de una carpeta que se haya especificado en un estado de contenido de sincronizar anterior. La carpeta puede ser una carpeta de correo, calendario, contactos, tareas, notas o diario. Durante este estado, Outlook crea una lista de elementos que se han agregado, modificado, movido, eliminado o marcado como leído y prepara la información interna adecuada para el estado del mensaje carga correspondiente, cargar el estado de eliminar o cargar el estado de lectura estado.
  
Cuando finaliza este estado, Outlook marca la carpeta como tener su contenido sincronizado, por lo que el contenido no se cargará nuevo hasta que se realiza otra modificación. Devuelve el almacén local en el estado del contenido de sincronizar.
  
## <a name="see-also"></a>Recursos adicionales



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[ESTADO DE SINCRONIZACIÓN](syncstate.md)

