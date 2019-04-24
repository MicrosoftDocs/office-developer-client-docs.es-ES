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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332840"
---
# <a name="sending-message-delivery-reports"></a><span data-ttu-id="5977c-103">Enviar informes de entrega de mensajes</span><span class="sxs-lookup"><span data-stu-id="5977c-103">Sending Message Delivery Reports</span></span>

  
  
<span data-ttu-id="5977c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5977c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5977c-105">Algunos sistemas de mensajería subyacente admiten informes de entrega y otros no.</span><span class="sxs-lookup"><span data-stu-id="5977c-105">Some underlying messaging systems support delivery reports and some do not.</span></span> <span data-ttu-id="5977c-106">El modo en que el proveedor de transporte determina si se pueden enviar informes de no entrega o entrega de mensajes a las aplicaciones cliente es un detalle de implementación específico de los proveedores de transporte individuales.</span><span class="sxs-lookup"><span data-stu-id="5977c-106">How the transport provider determines whether message delivery or nondelivery reports can be sent to client applications is an implementation detail specific to individual transport providers.</span></span> <span data-ttu-id="5977c-107">Si se pueden enviar informes de entrega a las aplicaciones cliente, los proveedores de transporte usan el método [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) para notificar a MAPI la entrega correcta o incorrecta para uno o más destinatarios.</span><span class="sxs-lookup"><span data-stu-id="5977c-107">If delivery reports can be sent to client applications, transport providers use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to notify MAPI of successful or unsuccessful delivery for one or more recipients.</span></span> <span data-ttu-id="5977c-108">MAPI, a continuación, genera informes de entrega o no entrega que corresponden a esos destinatarios.</span><span class="sxs-lookup"><span data-stu-id="5977c-108">MAPI then generates delivery or nondelivery reports corresponding to those recipients.</span></span> <span data-ttu-id="5977c-109">Los proveedores de transporte también pueden traducir los informes de entrega y de no entrega que son nativos para el sistema de mensajería en informes de no entrega y entrega MAPI por medio de **StatusRecips**.</span><span class="sxs-lookup"><span data-stu-id="5977c-109">Transport providers can also translate incoming delivery and nondelivery reports that are native to the messaging system into MAPI delivery and nondelivery reports by means of **StatusRecips**.</span></span>
  

