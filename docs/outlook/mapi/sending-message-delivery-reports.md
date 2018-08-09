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
ms.openlocfilehash: d94785df9becf46bbfad66465facea35202c6079
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820622"
---
# <a name="sending-message-delivery-reports"></a><span data-ttu-id="4646f-103">Enviar informes de entrega de mensajes</span><span class="sxs-lookup"><span data-stu-id="4646f-103">Sending Message Delivery Reports</span></span>

  
  
<span data-ttu-id="4646f-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4646f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4646f-105">Algunos sistemas de mensajería subyacentes admiten informes de entrega y otros no.</span><span class="sxs-lookup"><span data-stu-id="4646f-105">Some underlying messaging systems support delivery reports and some do not.</span></span> <span data-ttu-id="4646f-106">Cómo el proveedor de transporte determina si se pueden enviar informes de entrega o de no entrega de mensajes a las aplicaciones cliente es un detalle de implementación específico de los proveedores de transporte individual.</span><span class="sxs-lookup"><span data-stu-id="4646f-106">How the transport provider determines whether message delivery or nondelivery reports can be sent to client applications is an implementation detail specific to individual transport providers.</span></span> <span data-ttu-id="4646f-107">Si los informes de entrega se pueden enviar a las aplicaciones cliente, proveedores de transporte use el método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para notificar a MAPI de entrega de éxito o no para uno o más destinatarios.</span><span class="sxs-lookup"><span data-stu-id="4646f-107">If delivery reports can be sent to client applications, transport providers use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to notify MAPI of successful or unsuccessful delivery for one or more recipients.</span></span> <span data-ttu-id="4646f-108">MAPI, a continuación, genera informes de entrega o de no entrega correspondiente a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="4646f-108">MAPI then generates delivery or nondelivery reports corresponding to those recipients.</span></span> <span data-ttu-id="4646f-109">Los proveedores de transporte también pueden traducir informes de entrega y no entrega entrantes que son nativos para el sistema de mensajería en la entrega MAPI e informes de no entrega por medio de **StatusRecips**.</span><span class="sxs-lookup"><span data-stu-id="4646f-109">Transport providers can also translate incoming delivery and nondelivery reports that are native to the messaging system into MAPI delivery and nondelivery reports by means of **StatusRecips**.</span></span>
  

