---
title: Cargar estado de lectura de estado
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e8ad2acf019df3f07060c8e8c71a62afd3fca03c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282666"
---
# <a name="upload-read-status-state"></a>Cargar estado de lectura de estado

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 En este tema se describe lo que ocurre durante el estado de lectura de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |
|Estructura de datos relacionada:  <br/> |**[UPREAD](upread.md)** <br/> |
|Desde este estado:  <br/> |[Cargar estado de la tabla](upload-table-state.md) <br/> |
|A este estado:  <br/> |Cargar estado de la tabla  <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es un equipo de estado determinista. Un cliente que deja de estar en un estado a otro debe volver eventualmente a la primera parte de la segunda. 
  
## <a name="description"></a>Descripción

Este estado inicia la carga del estado de lectura de los elementos en una carpeta especificada en un estado de tabla de carga anterior. Durante este estado, Outlook inicializa la estructura de datos de **lectura** asociada con la información de los elementos en la carpeta cuyo estado de lectura ha cambiado. A continuación, el cliente actualiza el estado de lectura de estos elementos en el servidor como leídos o no leídos. 
  
Cuando finaliza este estado, Outlook borra la información interna sobre el estado de lectura del elemento, lo que evita que se vuelva a cargar el estado de lectura del elemento. El almacén local vuelve al estado cargar tabla.
  
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

