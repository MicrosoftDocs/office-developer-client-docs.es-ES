---
title: Estado de sincronización de contenido
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3ebe1f5f48f9becdf01ea184c2b76fa2c8fa21e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438473"
---
# <a name="synchronize-contents-state"></a>Estado de sincronización de contenido

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 En este tema se describe lo que ocurre durante el estado Synchronize Contents de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC_CONTENTS** <br/> |
|Estructura de datos relacionada:  <br/> |**[SYNCCONT](synccont.md)** <br/> |
|Desde este estado:  <br/> |[Estado de sincronización](synchronize-state.md) <br/> |
|A este estado:  <br/> |[Descargar estado](download-table-state.md)de la tabla, [cargar estado](upload-table-state.md)de la tabla o estado de sincronización  <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es un equipo de estado determinista. Un cliente que deja de estar en un estado a otro debe volver eventualmente a la primera parte de la segunda. 
  
## <a name="description"></a>Descripción

Este estado inicia uno de los dos procesos de replicación: carga del contenido de las carpetas especificadas en un almacén local o una sincronización completa. En una sincronización completa, para cada una de las carpetas especificadas, el contenido se carga primero y, a continuación, se descarga. Según el valor de *ulFlags* establecido en la estructura de **[sincronización](sync.md)** correspondiente en el estado de sincronización anterior, Outlook inicializa [out] miembros en la estructura **SYNCCONT** para proporcionar información sobre el contenido. 
  
A través de la misma estructura **SYNCCONT** , el cliente obtiene el recuento de las carpetas que tienen contenido que se va a cargar o descargar. El cliente recorrerá cada una de estas carpetas moviendo el almacén local al estado cargar tabla para cargar una carpeta o moviendo el almacén local al estado Descargar tabla para descargar la carpeta. 
  
Además, el cliente obtiene los identificadores de entrada de las carpetas que requieren replicación.
  
Cuando finaliza este estado, Outlook limpia su información interna. El almacén local vuelve al estado Synchronize.
  
## <a name="see-also"></a>Ver también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

