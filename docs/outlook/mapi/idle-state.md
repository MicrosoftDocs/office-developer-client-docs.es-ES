---
title: Estado inactivo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7b74ecb44d9a38fc73ceed4077d6f7a939f92f5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591803"
---
# <a name="idle-state"></a><span data-ttu-id="484af-103">Estado inactivo</span><span class="sxs-lookup"><span data-stu-id="484af-103">Idle State</span></span>

  
  
<span data-ttu-id="484af-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="484af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="484af-105">En este tema se describe qué ocurre durante el estado de inactividad de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="484af-105">This topic describes what happens during the idle state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="484af-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="484af-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="484af-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="484af-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="484af-108">**LR_SYNC_IDLE**</span><span class="sxs-lookup"><span data-stu-id="484af-108">**LR_SYNC_IDLE**</span></span> <br/> |
|<span data-ttu-id="484af-109">Estructura de datos relacionados:</span><span class="sxs-lookup"><span data-stu-id="484af-109">Related Data Structure:</span></span>  <br/> | <span data-ttu-id="484af-110">*None*</span><span class="sxs-lookup"><span data-stu-id="484af-110">*None*</span></span>  <br/> |
|<span data-ttu-id="484af-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="484af-111">From this state:</span></span>  <br/> | <span data-ttu-id="484af-112">*No disponible*</span><span class="sxs-lookup"><span data-stu-id="484af-112">*Not applicable*</span></span>  <br/> |
|<span data-ttu-id="484af-113">En este estado:</span><span class="sxs-lookup"><span data-stu-id="484af-113">To this state:</span></span>  <br/> |[<span data-ttu-id="484af-114">Sincronizar estado</span><span class="sxs-lookup"><span data-stu-id="484af-114">Synchronize state</span></span>](synchronize-state.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="484af-115">La máquina de estado de replicación es una máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="484af-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="484af-116">Un cliente sale de un estado a otro finalmente debe volver a la primera desde el último.</span><span class="sxs-lookup"><span data-stu-id="484af-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="484af-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="484af-117">Description</span></span>

<span data-ttu-id="484af-118">En este estado no ocurre nada.</span><span class="sxs-lookup"><span data-stu-id="484af-118">Nothing happens in this state.</span></span> <span data-ttu-id="484af-119">Un almacén local está en este estado antes de que se inicia la replicación y una vez completada la replicación.</span><span class="sxs-lookup"><span data-stu-id="484af-119">A local store is in this state before replication is initiated and after replication is complete.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="484af-120">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="484af-120">See also</span></span>



[<span data-ttu-id="484af-121">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="484af-121">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="484af-122">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="484af-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="484af-123">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="484af-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="484af-124">ESTADO DE SINCRONIZACIÓN</span><span class="sxs-lookup"><span data-stu-id="484af-124">SYNCSTATE</span></span>](syncstate.md)

