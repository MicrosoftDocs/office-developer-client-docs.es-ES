---
title: Asignación de atributos de correo de Internet a las propiedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79d1d2ba-34fe-4851-918f-adbc69c20eee
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c0a71cbd3b6cdbef091e75ade5d190369a4626a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355821"
---
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a><span data-ttu-id="20f2f-103">Asignación de atributos de correo de Internet a las propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="20f2f-103">Mapping of Internet Mail Attributes to MAPI Properties</span></span>

  
  
<span data-ttu-id="20f2f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20f2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20f2f-105">Este apéndice describe cómo un proveedor de transporte MAPI o una puerta de enlace compatible con MAPI que se conecta a Internet deben traducir entre las propiedades de los mensajes MAPI y los atributos del mensaje del Protocolo simple de transferencia de correo (SMTP).</span><span class="sxs-lookup"><span data-stu-id="20f2f-105">This appendix describes how a MAPI transport provider or MAPI-aware gateway which connects to the Internet should translate between MAPI message properties and Simple Mail Transport Protocol (SMTP) message attributes.</span></span> <span data-ttu-id="20f2f-106">SMTP es el protocolo de mensajería que se usa en gran parte de Internet.</span><span class="sxs-lookup"><span data-stu-id="20f2f-106">SMTP is the messaging protocol used on much of the Internet.</span></span> <span data-ttu-id="20f2f-107">SMTP define un conjunto de encabezados de mensaje (el sobre del mensaje) y un formato de contenido de mensaje.</span><span class="sxs-lookup"><span data-stu-id="20f2f-107">SMTP defines a set of message headers — the message envelope — and a message content format.</span></span> <span data-ttu-id="20f2f-108">SMTP está completamente documentado en un conjunto de dos documentos, RFC 821 y RFC 822, que se pueden encontrar en una cantidad de sitios FTP y WWW en Internet.</span><span class="sxs-lookup"><span data-stu-id="20f2f-108">SMTP is fully documented in a set of two documents, RFC 821 and RFC 822, which can be found at a number of FTP and WWW sites on the Internet.</span></span>
  
<span data-ttu-id="20f2f-109">Para obtener información sobre el protocolo SMTP que se usa para comunicarse con agentes de correo basados en SMTP, consulte RFC 821, "Protocolo simple de [https://www.rfc-editor.org](https://www.rfc-editor.org)transferencia de correo" en.</span><span class="sxs-lookup"><span data-stu-id="20f2f-109">For information on the SMTP protocol used to communicate with SMTP-based mail agents, see RFC 821, "Simple Mail Transfer Protocol," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="20f2f-110">Para el direccionamiento y los encabezados de mensaje estándar, consulte RFC 822, "Standard para el formato de los mensajes de texto de [https://www.rfc-editor.org](https://www.rfc-editor.org)Internet arpa", en.</span><span class="sxs-lookup"><span data-stu-id="20f2f-110">For addressing and standard message headers, see RFC 822, "Standard for the Format of ARPA Internet Text Messages," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="20f2f-111">Para MIME, vea RFC 1521, "MIME (Extensiones multipropósito de correo Internet) Part One: mecanismos para especificar y describir el formato de los cuerpos de los mensajes de Internet [https://www.rfc-editor.org](https://www.rfc-editor.org), en.</span><span class="sxs-lookup"><span data-stu-id="20f2f-111">For MIME, see RFC 1521, "MIME (Multipurpose Internet Mail Extensions) Part One: Mechanisms for Specifying and Describing the Format of Internet Message Bodies," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="20f2f-112">El objetivo de asignar atributos de mensaje SMTP a las propiedades MAPI (y viceversa) es garantizar que el contenido completo de los mensajes MAPI, más allá de lo que se pueda codificar mediante atributos nativos de mensajes SMTP, se pueda intercambiar de manera confiable entre diferentes MAPI componentes que deben comunicarse a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="20f2f-112">The goal of mapping SMTP message attributes to MAPI properties (and vice versa) is to ensure that the full content of MAPI messages, over and above that which can be encoded using native SMTP message attributes, can be reliably exchanged among different MAPI components that must communicate over the Internet.</span></span> <span data-ttu-id="20f2f-113">Este documento se basa en el trabajo ya realizado en estos componentes de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="20f2f-113">This document is based on work already done on such components at Microsoft.</span></span> 
  
<span data-ttu-id="20f2f-114">En este documento se asume que está familiarizado con los transportes MAPI, TNEF y el correo SMTP.</span><span class="sxs-lookup"><span data-stu-id="20f2f-114">This document assumes familiarity with MAPI transports, TNEF, and SMTP mail.</span></span> <span data-ttu-id="20f2f-115">Se esfuerza por ser conciso en lugar de hacerlo abundantemente.</span><span class="sxs-lookup"><span data-stu-id="20f2f-115">It strives to be concise rather than abundantly clear.</span></span>
  
<span data-ttu-id="20f2f-116">Como Convención, "saliente" se refiere al correo que se desplaza desde un agente de UA o MTA compatible con MAPI a Internet y "entrante" se refiere al correo que viaja desde Internet a un componente MAPI.</span><span class="sxs-lookup"><span data-stu-id="20f2f-116">As a convention, "outbound" refers to mail traveling from a MAPI-compliant UA or MTA to the Internet, and "inbound" refers to mail traveling from the Internet to a MAPI component.</span></span>
  

