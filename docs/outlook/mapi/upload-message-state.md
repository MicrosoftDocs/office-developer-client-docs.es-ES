---
title: Cargar estado del mensaje
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
# <a name="upload-message-state"></a>Cargar estado del mensaje

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 En este tema se describe lo que ocurre durante el estado de carga del equipo de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |
|Estructura de datos relacionada:  <br/> |**[UPMSG](upmsg.md)** <br/> |
|Desde este estado:  <br/> |[Cargar estado de la tabla](upload-table-state.md) <br/> |
|A este estado:  <br/> |Cargar estado de la tabla  <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es un equipo de estado determinista. Un cliente que deja de estar en un estado a otro debe volver eventualmente a la primera parte de la segunda. 
  
## <a name="description"></a>Descripción

Este estado inicia la carga de un elemento de Outlook (correo, calendario, contacto, tarea, nota o diario) que es nuevo o se ha movido a la carpeta actual o que se ha modificado. Outlook inicializa la estructura de datos correpsonding **UPMSG** con la información adecuada para que el elemento se agregue, mueva o modifique. 
  
Si se ha agregado o movido el elemento, el cliente, a continuación, agrega o actualiza correctamente el elemento en el servidor. 
  
Si el elemento se ha modificado, Outlook especifica aún más la estructura de datos **UPMSG** si las modificaciones están en un encabezado de mensaje (en cuyo caso el elemento es el encabezado del mensaje), en las propiedades del elemento o en el propio elemento que requiere un conflicto. n. A continuación, el cliente actualiza el elemento en el servidor. 
  
Cuando finaliza el envío del elemento, Outlook indica que el mensaje se ha cargado para que no se procese en una carga posterior. El almacén local vuelve al estado cargar tabla.
  
## <a name="see-also"></a>Ver también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

