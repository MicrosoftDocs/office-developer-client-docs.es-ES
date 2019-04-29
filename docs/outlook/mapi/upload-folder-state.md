---
title: Cargar estado de la carpeta
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c20f2998a2fef1ddb53b13708dcf56f9d7b50dbe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419572"
---
# <a name="upload-folder-state"></a>Cargar estado de la carpeta

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 En este tema se describe lo que ocurre durante el estado de la carpeta de carga de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |
|Estructura de datos relacionada:  <br/> |**[UPFLD](upfld.md)** <br/> |
|Desde este estado:  <br/> |[Cargar estado de la jerarquía](upload-hierarchy-state.md) <br/> |
|A este estado:  <br/> |Cargar estado de la jerarquía  <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es un equipo de estado determinista. Un cliente que deja de estar en un estado a otro debe volver eventualmente a la primera parte de la segunda. 
  
## <a name="description"></a>Descripción

Este estado inicia la carga de una carpeta en una jerarquía que se ha especificado en un estado de jerarquía de carga anterior. Durante este estado, Outlook proporciona el objeto de carpeta (si no se ha eliminado) y las marcas que indican el estado de la carpeta (nueva, movida, modificada o eliminada) como parte de la estructura de datos de **UPFLD** correspondiente. A continuación, el cliente carga esta información en el servidor. 
  
Si la carga se realiza correctamente, el cliente establece *ulFlags* en **UPFLD** en **UPF_OK**. A continuación, Outlook borra su información interna sobre la solicitud para cargar la carpeta. 
  
Cuando finaliza la carga de la carpeta, el almacén local vuelve al estado de carga de la jerarquía. Basándose en la estructura **[UPHIER](uphier.md)** correspondiente al estado de la jerarquía de carga anterior, Outlook determina si se debe continuar con la carga de la siguiente carpeta y preparar el siguiente estado de la carpeta de carga. 
  
> [!NOTE]
> Si el cliente solo necesita cargar una carpeta, el cliente puede iniciar la replicación mediante el [Estado Synchronize](synchronize-state.md) sin especificar el estado de carga de la jerarquía. El cliente establece determinados miembros de **[Sync](sync.md)** ( *ulFlags* a **UPS_UPLOAD_ONLY** y **UPS_ONE_FOLDER** y *FEID* en el identificador de la carpeta) para decir a Outlook que solo se cargará una carpeta. 
  
## <a name="see-also"></a>Ver también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

