---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: Especifica dejar una copia de un mensaje en el servidor para una cuenta POP.
ms.openlocfilehash: e1bbddea0f10c07d630676960d1b330f6055e137
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410948"
---
# <a name="prop_pop_leave_on_server"></a><span data-ttu-id="92063-103">PROP_POP_LEAVE_ON_SERVER</span><span class="sxs-lookup"><span data-stu-id="92063-103">PROP_POP_LEAVE_ON_SERVER</span></span>

<span data-ttu-id="92063-104">Especifica dejar una copia de un mensaje en el servidor para una cuenta POP.</span><span class="sxs-lookup"><span data-stu-id="92063-104">Specifies leaving a copy of a message on the server for a POP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="92063-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="92063-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92063-106">Identificador:</span><span class="sxs-lookup"><span data-stu-id="92063-106">Identifier:</span></span>  <br/> |<span data-ttu-id="92063-107">0x1000</span><span class="sxs-lookup"><span data-stu-id="92063-107">0x1000</span></span>  <br/> |
|<span data-ttu-id="92063-108">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="92063-108">Property type:</span></span>  <br/> |<span data-ttu-id="92063-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="92063-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="92063-110">Etiqueta de propiedad:</span><span class="sxs-lookup"><span data-stu-id="92063-110">Property tag:</span></span>  <br/> |<span data-ttu-id="92063-111">0x10000003</span><span class="sxs-lookup"><span data-stu-id="92063-111">0x10000003</span></span>  <br/> |
|<span data-ttu-id="92063-112">Acceso:</span><span class="sxs-lookup"><span data-stu-id="92063-112">Access:</span></span>  <br/> |<span data-ttu-id="92063-113">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="92063-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92063-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="92063-114">Remarks</span></span>

<span data-ttu-id="92063-115">En la tabla siguiente se enumeran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="92063-115">The following table lists the possible values.</span></span> <span data-ttu-id="92063-116">Vea [Constantes (API de administración de cuentas)](constants-account-management-api.md) para obtener más información sobre las constantes.</span><span class="sxs-lookup"><span data-stu-id="92063-116">See [Constants (Account management API)](constants-account-management-api.md) for more information on the constants.</span></span> 
  
|<span data-ttu-id="92063-117">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="92063-117">**Possible values**</span></span>|<span data-ttu-id="92063-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="92063-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="92063-119">**LEAVE_ON_SERVER**</span><span class="sxs-lookup"><span data-stu-id="92063-119">**LEAVE_ON_SERVER**</span></span> <br/> |<span data-ttu-id="92063-120">Deja una copia del mensaje en el servidor POP después de descargarlo en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="92063-120">Leaves a copy of the message on the POP server after downloading the message to a device.</span></span>  <br/> |
|<span data-ttu-id="92063-121">**REMOVE_AFTER**</span><span class="sxs-lookup"><span data-stu-id="92063-121">**REMOVE_AFTER**</span></span> <br/> |<span data-ttu-id="92063-122">Quita el mensaje del servidor POP después de descargarlo en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="92063-122">Removes the message from the POP server after downloading it to a device.</span></span>  <br/> |
|<span data-ttu-id="92063-123">**REMOVE_ON_NUKE**</span><span class="sxs-lookup"><span data-stu-id="92063-123">**REMOVE_ON_NUKE**</span></span> <br/> |<span data-ttu-id="92063-124">Quita el mensaje del servidor POP solo después de que el usuario elimine el mensaje de la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="92063-124">Removes the message from the POP server only after the user deletes the message from the Deleted Items folder.</span></span>  <br/> |
|<span data-ttu-id="92063-125">**GET_REMOVE_AFTER_DAYS**( _ul_)</span><span class="sxs-lookup"><span data-stu-id="92063-125">**GET_REMOVE_AFTER_DAYS**( _ul_)</span></span>  <br/> |<span data-ttu-id="92063-126">Obtiene el número de días después de los cuales se quitará el mensaje del servidor POP.</span><span class="sxs-lookup"><span data-stu-id="92063-126">Gets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
|<span data-ttu-id="92063-127">**SET_REMOVE_AFTER_DAYS**( _días_)</span><span class="sxs-lookup"><span data-stu-id="92063-127">**SET_REMOVE_AFTER_DAYS**( _days_)</span></span>  <br/> |<span data-ttu-id="92063-128">Establece el número de días después de los cuales se quitará el mensaje del servidor POP.</span><span class="sxs-lookup"><span data-stu-id="92063-128">Sets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="92063-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="92063-129">See also</span></span>

- [<span data-ttu-id="92063-130">Administrar la descarga de mensajes de las cuentas POP3</span><span class="sxs-lookup"><span data-stu-id="92063-130">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="92063-131">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="92063-131">Constants (Account management API)</span></span>](constants-account-management-api.md)

