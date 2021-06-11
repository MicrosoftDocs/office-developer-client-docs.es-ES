---
title: Procesamiento personalizado con TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c015335a-8fcd-4b03-abb9-9b6b72000e13
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3ee219ec09116640903df75ce271f607972dd37e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430850"
---
# <a name="custom-processing-with-tnef"></a><span data-ttu-id="c79fe-103">Procesamiento personalizado con TNEF</span><span class="sxs-lookup"><span data-stu-id="c79fe-103">Custom processing with TNEF</span></span>

<span data-ttu-id="c79fe-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c79fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c79fe-105">Los proveedores de transporte pueden usar el procesamiento personalizado para procesar las propiedades de un archivo adjunto en sí, transmitir datos adjuntos por separado o transmitirlos a través del modelo de datos adjuntos del sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="c79fe-105">Transport providers can use custom processing to process the properties on an attachment itself, transmit attachments separately, or transmit them through the messaging system's attachment model.</span></span> <span data-ttu-id="c79fe-106">TNEF usa un mecanismo que permite al proveedor de transporte enviar los datos adjuntos aparte del mensaje y volver a conectarlos en el lado de recepción.</span><span class="sxs-lookup"><span data-stu-id="c79fe-106">TNEF uses a mechanism that enables the transport provider to send the attachments apart from the message and reconnect them on the receiving side.</span></span>
  

