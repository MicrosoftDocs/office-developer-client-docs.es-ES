---
title: Enviar informes de entrega de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: abb12ec5-f0b7-488a-a75d-446f4be53e96
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2a31e7d088d5c1f94b272cb4d307f3aff99f32ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433083"
---
# <a name="sending-message-delivery-reports"></a><span data-ttu-id="bdefe-103">Enviar informes de entrega de mensajes</span><span class="sxs-lookup"><span data-stu-id="bdefe-103">Sending Message Delivery Reports</span></span>

  
  
<span data-ttu-id="bdefe-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bdefe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bdefe-105">Algunos sistemas de mensajería subyacentes admiten informes de entrega y otros no.</span><span class="sxs-lookup"><span data-stu-id="bdefe-105">Some underlying messaging systems support delivery reports and some do not.</span></span> <span data-ttu-id="bdefe-106">La forma en que el proveedor de transporte determina si los informes de entrega de mensajes o no entrega se pueden enviar a aplicaciones cliente es un detalle de implementación específico para proveedores de transporte individuales.</span><span class="sxs-lookup"><span data-stu-id="bdefe-106">How the transport provider determines whether message delivery or nondelivery reports can be sent to client applications is an implementation detail specific to individual transport providers.</span></span> <span data-ttu-id="bdefe-107">Si los informes de entrega se pueden enviar a aplicaciones cliente, los proveedores de transporte usan el método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para notificar a MAPI de una entrega correcta o incorrecta para uno o varios destinatarios.</span><span class="sxs-lookup"><span data-stu-id="bdefe-107">If delivery reports can be sent to client applications, transport providers use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to notify MAPI of successful or unsuccessful delivery for one or more recipients.</span></span> <span data-ttu-id="bdefe-108">A continuación, MAPI genera informes de entrega o no entrega correspondientes a esos destinatarios.</span><span class="sxs-lookup"><span data-stu-id="bdefe-108">MAPI then generates delivery or nondelivery reports corresponding to those recipients.</span></span> <span data-ttu-id="bdefe-109">Los proveedores de transporte también pueden traducir informes de entrega entrante y no entrega nativos del sistema de mensajería a informes de entrega MAPI y no entrega mediante **StatusRecips**.</span><span class="sxs-lookup"><span data-stu-id="bdefe-109">Transport providers can also translate incoming delivery and nondelivery reports that are native to the messaging system into MAPI delivery and nondelivery reports by means of **StatusRecips**.</span></span>
  

