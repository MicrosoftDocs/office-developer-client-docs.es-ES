---
title: Upload Estado de tabla
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a2a9b3f214c76b8ec965c84c4731e0dc57e83352
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405824"
---
# <a name="upload-table-state"></a>Upload Estado de tabla

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 En este tema se describe lo que sucede durante el estado de la tabla de carga de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |
|Estructura de datos relacionada:  <br/> |**[UPTBL](uptbl.md)** <br/> |
|Desde este estado:  <br/> |[Sincronizar el estado de contenido](synchronize-contents-state.md) <br/> |
|A este estado:  <br/> |[Upload de mensaje,](upload-message-state.md)estado de [eliminación de carga,](upload-delete-status-state.md)estado de lectura [de](upload-read-status-state.md)carga o estado de sincronización de contenido  <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es una máquina de estado determinista. Un cliente que sale de un estado a otro debe volver al primero desde el segundo. 
  
## <a name="description"></a>Descripción

Este estado inicia la carga del contenido de una carpeta que se ha especificado en un estado de contenido de sincronización anterior. La carpeta puede ser una carpeta de correo, calendario, contactos, tareas, notas o diario. Durante este estado, Outlook crea una lista de elementos que se han agregado, modificado, movido, eliminado o marcado como leído, y prepara la información interna adecuada para el estado del mensaje de carga correspondiente, el estado de la eliminación de carga o el estado de lectura de carga.
  
Cuando finalice este estado, Outlook marca la carpeta como que su contenido esté sincronizado, de modo que el contenido no se vuelva a cargar hasta que se haga otra modificación. El almacén local vuelve al estado de sincronización de contenido.
  
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

