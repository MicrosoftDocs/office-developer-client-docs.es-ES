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
# <a name="sending-message-delivery-reports"></a>Enviar informes de entrega de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Algunos sistemas de mensajería subyacente admiten informes de entrega y otros no. El modo en que el proveedor de transporte determina si se pueden enviar informes de no entrega o entrega de mensajes a las aplicaciones cliente es un detalle de implementación específico de los proveedores de transporte individuales. Si se pueden enviar informes de entrega a las aplicaciones cliente, los proveedores de transporte usan el método [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) para notificar a MAPI la entrega correcta o incorrecta para uno o más destinatarios. MAPI, a continuación, genera informes de entrega o no entrega que corresponden a esos destinatarios. Los proveedores de transporte también pueden traducir los informes de entrega y de no entrega que son nativos para el sistema de mensajería en informes de no entrega y entrega MAPI por medio de **StatusRecips**.
  

