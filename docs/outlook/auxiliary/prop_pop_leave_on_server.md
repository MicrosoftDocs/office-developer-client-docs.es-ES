---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: Especifica dejar una copia de un mensaje en el servidor para una cuenta POP.
ms.openlocfilehash: 9f986ff60a5824ece0a8bb91619323b58ec8b87a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816324"
---
# <a name="proppopleaveonserver"></a><span data-ttu-id="1d702-103">PROP_POP_LEAVE_ON_SERVER</span><span class="sxs-lookup"><span data-stu-id="1d702-103">PROP_POP_LEAVE_ON_SERVER</span></span>

<span data-ttu-id="1d702-104">Especifica dejar una copia de un mensaje en el servidor para una cuenta POP.</span><span class="sxs-lookup"><span data-stu-id="1d702-104">Specifies leaving a copy of a message on the server for a POP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1d702-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="1d702-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d702-106">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1d702-106">Identifier:</span></span>  <br/> |<span data-ttu-id="1d702-107">0 x 1000</span><span class="sxs-lookup"><span data-stu-id="1d702-107">0x1000</span></span>  <br/> |
|<span data-ttu-id="1d702-108">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="1d702-108">Property type:</span></span>  <br/> |<span data-ttu-id="1d702-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="1d702-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="1d702-110">Etiqueta de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="1d702-110">Property tag:</span></span>  <br/> |<span data-ttu-id="1d702-111">0x10000003</span><span class="sxs-lookup"><span data-stu-id="1d702-111">0x10000003</span></span>  <br/> |
|<span data-ttu-id="1d702-112">Access:</span><span class="sxs-lookup"><span data-stu-id="1d702-112">Access:</span></span>  <br/> |<span data-ttu-id="1d702-113">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d702-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1d702-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1d702-114">Remarks</span></span>

<span data-ttu-id="1d702-115">En la siguiente tabla se enumera los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="1d702-115">The following table lists the possible values.</span></span> <span data-ttu-id="1d702-116">Para obtener más información acerca de las constantes, vea [constantes (API de administración de cuenta)](constants-account-management-api.md) .</span><span class="sxs-lookup"><span data-stu-id="1d702-116">See [Constants (Account management API)](constants-account-management-api.md) for more information on the constants.</span></span> 
  
|<span data-ttu-id="1d702-117">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="1d702-117">**Possible values**</span></span>|<span data-ttu-id="1d702-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d702-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1d702-119">**LEAVE_ON_SERVER**</span><span class="sxs-lookup"><span data-stu-id="1d702-119">**LEAVE_ON_SERVER**</span></span> <br/> |<span data-ttu-id="1d702-120">Deja una copia del mensaje en el servidor POP después de descargar el mensaje a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d702-120">Leaves a copy of the message on the POP server after downloading the message to a device.</span></span>  <br/> |
|<span data-ttu-id="1d702-121">**REMOVE_AFTER**</span><span class="sxs-lookup"><span data-stu-id="1d702-121">**REMOVE_AFTER**</span></span> <br/> |<span data-ttu-id="1d702-122">Quita el mensaje del servidor POP después de descargar a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d702-122">Removes the message from the POP server after downloading it to a device.</span></span>  <br/> |
|<span data-ttu-id="1d702-123">**REMOVE_ON_NUKE**</span><span class="sxs-lookup"><span data-stu-id="1d702-123">**REMOVE_ON_NUKE**</span></span> <br/> |<span data-ttu-id="1d702-124">Quita el mensaje del servidor POP sólo después de que el usuario elimina el mensaje de la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="1d702-124">Removes the message from the POP server only after the user deletes the message from the Deleted Items folder.</span></span>  <br/> |
|<span data-ttu-id="1d702-125">**GET_REMOVE_AFTER_DAYS** ( _ul_)</span><span class="sxs-lookup"><span data-stu-id="1d702-125">**GET_REMOVE_AFTER_DAYS**( _ul_)</span></span>  <br/> |<span data-ttu-id="1d702-126">Obtiene el número de días después de que el mensaje se quitará el servidor POP.</span><span class="sxs-lookup"><span data-stu-id="1d702-126">Gets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
|<span data-ttu-id="1d702-127">**SET_REMOVE_AFTER_DAYS** ( _días_)</span><span class="sxs-lookup"><span data-stu-id="1d702-127">**SET_REMOVE_AFTER_DAYS**( _days_)</span></span>  <br/> |<span data-ttu-id="1d702-128">Establece el número de días después de que el mensaje se quitará el servidor POP.</span><span class="sxs-lookup"><span data-stu-id="1d702-128">Sets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1d702-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d702-129">See also</span></span>

- [<span data-ttu-id="1d702-130">Administrar la descarga de mensajes de las cuentas POP3</span><span class="sxs-lookup"><span data-stu-id="1d702-130">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="1d702-131">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="1d702-131">Constants (Account management API)</span></span>](constants-account-management-api.md)

