---
title: Cargar estado de la tabla
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
# <a name="upload-table-state"></a>Cargar estado de la tabla

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 En este tema se describe lo que sucede durante el estado de carga de la tabla de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |
|Estructura de datos relacionada:  <br/> |**[UPTBL](uptbl.md)** <br/> |
|Desde este estado:  <br/> |[Estado de sincronización de contenido](synchronize-contents-state.md) <br/> |
|A este estado:  <br/> |[Estado del mensaje de carga](upload-message-state.md), cargar estado de [eliminación](upload-delete-status-state.md), [cargar estado de lectura](upload-read-status-state.md)o sincronizar estado de contenido  <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es un equipo de estado determinista. Un cliente que deja de estar en un estado a otro debe volver eventualmente a la primera parte de la segunda. 
  
## <a name="description"></a>Descripción

Este estado inicia la carga del contenido de una carpeta que se ha especificado en el estado de sincronizar contenido anterior. La carpeta puede ser una carpeta de correo, calendario, contactos, tareas, notas o diario. Durante este estado, Outlook crea una lista de elementos que se han agregado, modificado, movido, eliminado o marcado como leído y prepara la información interna adecuada para el estado de mensaje de carga correspondiente, carga el estado de eliminación de carga o carga estado de lectura. Estado.
  
Cuando finaliza este estado, Outlook marca la carpeta como que su contenido está sincronizado, por lo que el contenido no se cargará de nuevo hasta que se realice otra modificación. El almacén local vuelve al estado Synchronize Contents.
  
## <a name="see-also"></a>Ver también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

