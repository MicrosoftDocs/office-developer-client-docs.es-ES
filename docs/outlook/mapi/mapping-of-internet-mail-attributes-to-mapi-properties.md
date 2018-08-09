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
ms.openlocfilehash: 4d1bc5fc5a5e304d81ab4252a527d0e52b0d6e3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/21/2018
ms.locfileid: "19818298"
---
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a><span data-ttu-id="f094d-103">Asignación de atributos de correo de Internet a las propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f094d-103">Mapping of Internet Mail Attributes to MAPI Properties</span></span>

  
  
<span data-ttu-id="f094d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f094d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f094d-105">En este apéndice se describe cómo debe traducir una puerta de enlace compatible con MAPI que se conecta a Internet o un proveedor de transporte MAPI entre las propiedades de mensaje MAPI y los atributos de mensaje de Protocolo Simple de transferencia de correo (SMTP).</span><span class="sxs-lookup"><span data-stu-id="f094d-105">This appendix describes how a MAPI transport provider or MAPI-aware gateway which connects to the Internet should translate between MAPI message properties and Simple Mail Transport Protocol (SMTP) message attributes.</span></span> <span data-ttu-id="f094d-106">SMTP es el protocolo de mensajería que se usa en gran parte de Internet.</span><span class="sxs-lookup"><span data-stu-id="f094d-106">SMTP is the messaging protocol used on much of the Internet.</span></span> <span data-ttu-id="f094d-107">SMTP define un conjunto de encabezados de mensaje: el sobre del mensaje y un formato de contenido del mensaje.</span><span class="sxs-lookup"><span data-stu-id="f094d-107">SMTP defines a set of message headers — the message envelope — and a message content format.</span></span> <span data-ttu-id="f094d-108">SMTP está totalmente documentado en un conjunto de dos documentos, RFC 821 y RFC 822, que se encuentra en un número de sitios FTP y WWW en Internet.</span><span class="sxs-lookup"><span data-stu-id="f094d-108">SMTP is fully documented in a set of two documents, RFC 821 and RFC 822, which can be found at a number of FTP and WWW sites on the Internet.</span></span>
  
<span data-ttu-id="f094d-109">Para obtener información sobre el protocolo SMTP utilizado para comunicar con los agentes de correo basado en SMTP, consulte RFC 821, "Simple Mail Transfer Protocol," en [http://www.rfc-editor.org](http://www.rfc-editor.org).</span><span class="sxs-lookup"><span data-stu-id="f094d-109">For information on the SMTP protocol used to communicate with SMTP-based mail agents, see RFC 821, "Simple Mail Transfer Protocol," at [http://www.rfc-editor.org](http://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="f094d-110">Para los encabezados de mensaje de asignación de direcciones y estándar, consulte RFC 822, "Estándar para el formato de ARPA Internet mensajes de texto," en [http://www.rfc-editor.org](http://www.rfc-editor.org).</span><span class="sxs-lookup"><span data-stu-id="f094d-110">For addressing and standard message headers, see RFC 822, "Standard for the Format of ARPA Internet Text Messages," at [http://www.rfc-editor.org](http://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="f094d-111">Para MIME, vea RFC 1521, "MIME (Extensiones multipropósito de correo Internet) parte uno: mecanismos para especificar y que describe el formato de cuerpos de mensaje de Internet," en [http://www.rfc-editor.org](http://www.rfc-editor.org).</span><span class="sxs-lookup"><span data-stu-id="f094d-111">For MIME, see RFC 1521, "MIME (Multipurpose Internet Mail Extensions) Part One: Mechanisms for Specifying and Describing the Format of Internet Message Bodies," at [http://www.rfc-editor.org](http://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="f094d-112">Es el objetivo de la asignación de atributos de mensaje SMTP a las propiedades de MAPI (y viceversa) para asegurarse de que el contenido completo de los mensajes MAPI, además de que se puede codificar con atributos de mensaje SMTP nativos, puede intercambiarse de forma confiable entre diferente MAPI componentes que deben comunicarse a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="f094d-112">The goal of mapping SMTP message attributes to MAPI properties (and vice versa) is to ensure that the full content of MAPI messages, over and above that which can be encoded using native SMTP message attributes, can be reliably exchanged among different MAPI components that must communicate over the Internet.</span></span> <span data-ttu-id="f094d-113">Este documento se basa en el trabajo ya realizado en esos componentes en Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f094d-113">This document is based on work already done on such components at Microsoft.</span></span> 
  
<span data-ttu-id="f094d-114">Este documento se da por supuesto familiaridad con los transportes MAPI, TNEF y SMTP correo.</span><span class="sxs-lookup"><span data-stu-id="f094d-114">This document assumes familiarity with MAPI transports, TNEF, and SMTP mail.</span></span> <span data-ttu-id="f094d-115">Se esfuerza por ser conciso en lugar de bastante claro.</span><span class="sxs-lookup"><span data-stu-id="f094d-115">It strives to be concise rather than abundantly clear.</span></span>
  
<span data-ttu-id="f094d-116">Como una convención, "saliente" hace referencia al correo viajan desde una UA compatible con MAPI o MTA a Internet y "entrada" hace referencia al correo de viaje desde Internet a un componente MAPI.</span><span class="sxs-lookup"><span data-stu-id="f094d-116">As a convention, "outbound" refers to mail traveling from a MAPI-compliant UA or MTA to the Internet, and "inbound" refers to mail traveling from the Internet to a MAPI component.</span></span>
  

