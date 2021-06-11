---
title: Upload Estado de lectura
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e8ad2acf019df3f07060c8e8c71a62afd3fca03c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431543"
---
# <a name="upload-read-status-state"></a>Upload Estado de lectura

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 En este tema se describe lo que sucede durante el estado de lectura de carga de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |
|Estructura de datos relacionada:  <br/> |**[UPREAD](upread.md)** <br/> |
|Desde este estado:  <br/> |[Upload de tabla](upload-table-state.md) <br/> |
|A este estado:  <br/> |Upload de tabla  <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es una máquina de estado determinista. Un cliente que sale de un estado a otro debe volver al primero desde el segundo. 
  
## <a name="description"></a>Descripción

Este estado inicia la carga del estado de lectura de los elementos de una carpeta especificada en un estado de tabla de carga anterior. Durante este estado, Outlook la estructura de datos **UPREAD** asociada con la información de los elementos de la carpeta cuyo estado de lectura ha cambiado. A continuación, el cliente actualiza el estado de lectura de estos elementos en el servidor como leídos o no leídos. 
  
Cuando finaliza este estado, Outlook borra la información interna sobre el estado de lectura del elemento, lo que impide que el estado de lectura del elemento se cargue de nuevo. El almacén local vuelve al estado de la tabla de carga.
  
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

