---
title: Estado inactivo
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
# <a name="idle-state"></a><span data-ttu-id="8911a-103">Estado inactivo</span><span class="sxs-lookup"><span data-stu-id="8911a-103">Idle State</span></span>

  
  
<span data-ttu-id="8911a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8911a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="8911a-105">En este tema se describe lo que sucede durante el estado de inactividad de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="8911a-105">This topic describes what happens during the idle state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="8911a-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="8911a-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8911a-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="8911a-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="8911a-108">**LR_SYNC_IDLE**</span><span class="sxs-lookup"><span data-stu-id="8911a-108">**LR_SYNC_IDLE**</span></span> <br/> |
|<span data-ttu-id="8911a-109">Estructura de datos relacionada:</span><span class="sxs-lookup"><span data-stu-id="8911a-109">Related Data Structure:</span></span>  <br/> | <span data-ttu-id="8911a-110">*Ninguna*</span><span class="sxs-lookup"><span data-stu-id="8911a-110">*None*</span></span>  <br/> |
|<span data-ttu-id="8911a-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="8911a-111">From this state:</span></span>  <br/> | <span data-ttu-id="8911a-112">*No aplicable*</span><span class="sxs-lookup"><span data-stu-id="8911a-112">*Not applicable*</span></span>  <br/> |
|<span data-ttu-id="8911a-113">A este estado:</span><span class="sxs-lookup"><span data-stu-id="8911a-113">To this state:</span></span>  <br/> |[<span data-ttu-id="8911a-114">Estado de sincronización</span><span class="sxs-lookup"><span data-stu-id="8911a-114">Synchronize state</span></span>](synchronize-state.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="8911a-115">La máquina de estado de replicación es una máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="8911a-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="8911a-116">Un cliente que va de un estado a otro debe volver al primero desde el segundo.</span><span class="sxs-lookup"><span data-stu-id="8911a-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="8911a-117">Description</span><span class="sxs-lookup"><span data-stu-id="8911a-117">Description</span></span>

<span data-ttu-id="8911a-118">No sucede nada en este estado.</span><span class="sxs-lookup"><span data-stu-id="8911a-118">Nothing happens in this state.</span></span> <span data-ttu-id="8911a-119">Un almacén local se encuentra en este estado antes de que se inicie la replicación y una vez completada la replicación.</span><span class="sxs-lookup"><span data-stu-id="8911a-119">A local store is in this state before replication is initiated and after replication is complete.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8911a-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8911a-120">See also</span></span>



[<span data-ttu-id="8911a-121">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="8911a-121">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="8911a-122">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="8911a-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="8911a-123">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="8911a-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="8911a-124">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="8911a-124">SYNCSTATE</span></span>](syncstate.md)

