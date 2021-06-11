---
title: Estado de inactividad
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3db4ead7e2485bbbae82f2a07659c934b394d6d5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419481"
---
# <a name="idle-state"></a><span data-ttu-id="a3a97-103">Estado de inactividad</span><span class="sxs-lookup"><span data-stu-id="a3a97-103">Idle State</span></span>

  
  
<span data-ttu-id="a3a97-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3a97-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="a3a97-105">En este tema se describe lo que sucede durante el estado de inactividad de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="a3a97-105">This topic describes what happens during the idle state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a3a97-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="a3a97-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a3a97-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="a3a97-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="a3a97-108">**LR_SYNC_IDLE**</span><span class="sxs-lookup"><span data-stu-id="a3a97-108">**LR_SYNC_IDLE**</span></span> <br/> |
|<span data-ttu-id="a3a97-109">Estructura de datos relacionada:</span><span class="sxs-lookup"><span data-stu-id="a3a97-109">Related Data Structure:</span></span>  <br/> | <span data-ttu-id="a3a97-110">*Ninguna*</span><span class="sxs-lookup"><span data-stu-id="a3a97-110">*None*</span></span>  <br/> |
|<span data-ttu-id="a3a97-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="a3a97-111">From this state:</span></span>  <br/> | <span data-ttu-id="a3a97-112">*No aplicable*</span><span class="sxs-lookup"><span data-stu-id="a3a97-112">*Not applicable*</span></span>  <br/> |
|<span data-ttu-id="a3a97-113">A este estado:</span><span class="sxs-lookup"><span data-stu-id="a3a97-113">To this state:</span></span>  <br/> |[<span data-ttu-id="a3a97-114">Estado de sincronización</span><span class="sxs-lookup"><span data-stu-id="a3a97-114">Synchronize state</span></span>](synchronize-state.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="a3a97-115">La máquina de estado de replicación es una máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="a3a97-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="a3a97-116">Un cliente que sale de un estado a otro debe volver al primero desde el segundo.</span><span class="sxs-lookup"><span data-stu-id="a3a97-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="a3a97-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3a97-117">Description</span></span>

<span data-ttu-id="a3a97-118">No ocurre nada en este estado.</span><span class="sxs-lookup"><span data-stu-id="a3a97-118">Nothing happens in this state.</span></span> <span data-ttu-id="a3a97-119">Un almacén local está en este estado antes de iniciar la replicación y después de que se complete la replicación.</span><span class="sxs-lookup"><span data-stu-id="a3a97-119">A local store is in this state before replication is initiated and after replication is complete.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a3a97-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3a97-120">See also</span></span>



[<span data-ttu-id="a3a97-121">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="a3a97-121">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="a3a97-122">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="a3a97-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="a3a97-123">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="a3a97-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="a3a97-124">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="a3a97-124">SYNCSTATE</span></span>](syncstate.md)

