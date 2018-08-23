---
title: Cargar estado de la carpeta
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ae8c3c4012874e1ca35761b103066cceebb1b165
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576753"
---
# <a name="upload-folder-state"></a>Cargar estado de la carpeta

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 En este tema se describe qué ocurre durante el estado de la carpeta de carga de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |
|Estructura de datos relacionados:  <br/> |**[UPFLD](upfld.md)** <br/> |
|Desde este estado:  <br/> |[Cargar el estado de la jerarquía](upload-hierarchy-state.md) <br/> |
|En este estado:  <br/> |Cargar el estado de la jerarquía  <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es una máquina de estado determinista. Un cliente sale de un estado a otro finalmente debe volver a la primera desde el último. 
  
## <a name="description"></a>Descripción

Este estado inicia la carga de una carpeta en una jerarquía que se haya especificado en un estado de jerarquía anterior de carga. Durante este estado, Outlook proporciona el objeto de carpeta (si no se ha eliminado) y los indicadores que indica el estado de la carpeta (nuevo, mover, modificar o eliminar) como parte de la estructura de datos **UPFLD** correspondiente. El cliente, a continuación, carga esta información en el servidor. 
  
Si la carga se realiza correctamente, el cliente establece *ulFlags* en **UPFLD** a **UPF_OK**. Outlook, a continuación, borra su información interna acerca de la solicitud para cargar la carpeta. 
  
Cuando finaliza la carga de la carpeta, el almacén local se devuelve en el estado de la jerarquía de carga. En función de la estructura **[UPHIER](uphier.md)** corresponde al estado de jerarquía anterior de carga, Outlook determina si para continuar con la carga de la carpeta siguiente y preparar para el estado de la carpeta de carga siguiente. 
  
> [!NOTE]
> Si el cliente necesita cargar sólo una carpeta, el cliente puede iniciar la replicación a través de la [sincronización de estado](synchronize-state.md) sin tener que especificar el estado de la jerarquía de carga. El cliente establece ciertos miembros de **[sincronización](sync.md)** : *ulFlags* para **UPS_UPLOAD_ONLY** y **UPS_ONE_FOLDER** y *feid* para el identificador de la carpeta indicar a Outlook que sólo una carpeta se cargará. 
  
## <a name="see-also"></a>Recursos adicionales



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[ESTADO DE SINCRONIZACIÓN](syncstate.md)

