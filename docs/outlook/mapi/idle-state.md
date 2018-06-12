---
title: Estado de inactividad
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: dbe81a2a27f302a38eba6f3c5045df905d8db682
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817171"
---
# <a name="idle-state"></a><span data-ttu-id="ce79b-103">Estado de inactividad</span><span class="sxs-lookup"><span data-stu-id="ce79b-103">Idle State</span></span>

  
  
<span data-ttu-id="ce79b-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ce79b-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="ce79b-105">En este tema se describe qué ocurre durante el estado de inactividad de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="ce79b-105">This topic describes what happens during the idle state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="ce79b-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="ce79b-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ce79b-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="ce79b-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="ce79b-108">**LR_SYNC_IDLE**</span><span class="sxs-lookup"><span data-stu-id="ce79b-108">**LR_SYNC_IDLE**</span></span> <br/> |
|<span data-ttu-id="ce79b-109">Estructura de datos relacionados:</span><span class="sxs-lookup"><span data-stu-id="ce79b-109">Related Data Structure:</span></span>  <br/> | <span data-ttu-id="ce79b-110">*None*</span><span class="sxs-lookup"><span data-stu-id="ce79b-110">*None*</span></span>  <br/> |
|<span data-ttu-id="ce79b-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="ce79b-111">From this state:</span></span>  <br/> | <span data-ttu-id="ce79b-112">*No es aplicable.*</span><span class="sxs-lookup"><span data-stu-id="ce79b-112">*Not applicable*</span></span>  <br/> |
|<span data-ttu-id="ce79b-113">En este estado:</span><span class="sxs-lookup"><span data-stu-id="ce79b-113">To this state:</span></span>  <br/> |[<span data-ttu-id="ce79b-114">Sincronizar estado</span><span class="sxs-lookup"><span data-stu-id="ce79b-114">Synchronize state</span></span>](synchronize-state.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="ce79b-115">La máquina de estado de replicación es una máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="ce79b-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="ce79b-116">Un cliente sale de un estado a otro finalmente debe volver a la primera desde el último.</span><span class="sxs-lookup"><span data-stu-id="ce79b-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="ce79b-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce79b-117">Description</span></span>

<span data-ttu-id="ce79b-118">En este estado no ocurre nada.</span><span class="sxs-lookup"><span data-stu-id="ce79b-118">Nothing happens in this state.</span></span> <span data-ttu-id="ce79b-119">Un almacén local está en este estado antes de que se inicia la replicación y una vez completada la replicación.</span><span class="sxs-lookup"><span data-stu-id="ce79b-119">A local store is in this state before replication is initiated and after replication is complete.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ce79b-120">Ver también</span><span class="sxs-lookup"><span data-stu-id="ce79b-120">See also</span></span>



[<span data-ttu-id="ce79b-121">Acerca de la API de replicación</span><span class="sxs-lookup"><span data-stu-id="ce79b-121">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="ce79b-122">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="ce79b-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="ce79b-123">Acerca de la máquina de estado de replicación</span><span class="sxs-lookup"><span data-stu-id="ce79b-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="ce79b-124">ESTADO DE SINCRONIZACIÓN</span><span class="sxs-lookup"><span data-stu-id="ce79b-124">SYNCSTATE</span></span>](syncstate.md)

