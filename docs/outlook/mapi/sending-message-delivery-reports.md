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
ms.openlocfilehash: 717494f30fd4d43e94a7c6a37770e2eab8ebb59e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593602"
---
# <a name="sending-message-delivery-reports"></a><span data-ttu-id="c3f70-103">Enviar informes de entrega de mensajes</span><span class="sxs-lookup"><span data-stu-id="c3f70-103">Sending Message Delivery Reports</span></span>

  
  
<span data-ttu-id="c3f70-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3f70-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3f70-105">Algunos sistemas de mensajería subyacentes admiten informes de entrega y otros no.</span><span class="sxs-lookup"><span data-stu-id="c3f70-105">Some underlying messaging systems support delivery reports and some do not.</span></span> <span data-ttu-id="c3f70-106">Cómo el proveedor de transporte determina si se pueden enviar informes de entrega o de no entrega de mensajes a las aplicaciones cliente es un detalle de implementación específico de los proveedores de transporte individual.</span><span class="sxs-lookup"><span data-stu-id="c3f70-106">How the transport provider determines whether message delivery or nondelivery reports can be sent to client applications is an implementation detail specific to individual transport providers.</span></span> <span data-ttu-id="c3f70-107">Si los informes de entrega se pueden enviar a las aplicaciones cliente, proveedores de transporte use el método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para notificar a MAPI de entrega de éxito o no para uno o más destinatarios.</span><span class="sxs-lookup"><span data-stu-id="c3f70-107">If delivery reports can be sent to client applications, transport providers use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to notify MAPI of successful or unsuccessful delivery for one or more recipients.</span></span> <span data-ttu-id="c3f70-108">MAPI, a continuación, genera informes de entrega o de no entrega correspondiente a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="c3f70-108">MAPI then generates delivery or nondelivery reports corresponding to those recipients.</span></span> <span data-ttu-id="c3f70-109">Los proveedores de transporte también pueden traducir informes de entrega y no entrega entrantes que son nativos para el sistema de mensajería en la entrega MAPI e informes de no entrega por medio de **StatusRecips**.</span><span class="sxs-lookup"><span data-stu-id="c3f70-109">Transport providers can also translate incoming delivery and nondelivery reports that are native to the messaging system into MAPI delivery and nondelivery reports by means of **StatusRecips**.</span></span>
  

