---
title: Información general sobre programación de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30ac637a-874f-4660-b5d0-d28d69486f64
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: d69d15f0f635c81bea30401b3a6d6e3ccf620112
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328276"
---
# <a name="mapi-programming-overview"></a><span data-ttu-id="2a8ad-103">Información general sobre programación de MAPI</span><span class="sxs-lookup"><span data-stu-id="2a8ad-103">MAPI Programming Overview</span></span>

  
  
<span data-ttu-id="2a8ad-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a8ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a8ad-105">Esta referencia de la API de mensajería (MAPI) de Microsoft Outlook está escrita para desarrolladores de C y C++ con una gran variedad de necesidades y experiencia con la mensajería.</span><span class="sxs-lookup"><span data-stu-id="2a8ad-105">This Microsoft Outlook Messaging API (MAPI) Reference is written for C and C++ developers with a variety of needs and experience with messaging.</span></span> <span data-ttu-id="2a8ad-106">Para aquellos desarrolladores que quieran usar MAPI para aumentar las aplicaciones que tienen características de mensajería, no se necesita ningún conocimiento de requisitos previos específicos.</span><span class="sxs-lookup"><span data-stu-id="2a8ad-106">For those developers who want to use MAPI to augment their applications that have messaging features, no specific prerequisite knowledge is required.</span></span> <span data-ttu-id="2a8ad-107">Necesita un fondo de mensajería y el modelo de objetos componentes (COM) para usar MAPI para crear aplicaciones o controladores de grupo de trabajo a escala completa para los servicios del sistema de mensajería especializado.</span><span class="sxs-lookup"><span data-stu-id="2a8ad-107">You need a background in messaging and the Component Object Model (COM) to use MAPI to create full-scale workgroup applications or drivers for specialized messaging system services.</span></span>
  
<span data-ttu-id="2a8ad-108">Antes de iniciar el trabajo de desarrollo, debe tener en cuenta la siguiente información acerca de cómo usar MAPI, el proceso de inicio de sesión y cómo se crean y configuran los perfiles y los servicios de mensajes.</span><span class="sxs-lookup"><span data-stu-id="2a8ad-108">Before starting development work, you should consider the following information about how to use MAPI, the logon process, and how profiles and message services are created and configured.</span></span>
  
<span data-ttu-id="2a8ad-109">La interfaz de programación de aplicaciones de mensajería (MAPI) es un amplio conjunto de funciones que los programadores pueden usar para crear aplicaciones habilitadas para correo.</span><span class="sxs-lookup"><span data-stu-id="2a8ad-109">The Messaging Application Program Interface (MAPI) is an extensive set of functions that developers can use to create mail-enabled applications.</span></span> <span data-ttu-id="2a8ad-110">La biblioteca de funciones completa se conoce como MAPI.</span><span class="sxs-lookup"><span data-stu-id="2a8ad-110">The full function library is known as MAPI.</span></span> <span data-ttu-id="2a8ad-111">MAPI habilita el control total sobre el sistema de mensajería en el equipo cliente, la creación y la administración de mensajes, la administración del buzón de cliente, los proveedores de servicios, etc.</span><span class="sxs-lookup"><span data-stu-id="2a8ad-111">MAPI enables complete control over the messaging system on the client computer, creation and management of messages, management of the client mailbox, service providers, and so on.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2a8ad-112">La MAPI extendida es la misma que MAPI y simplemente se conoce como MAPI en la documentación de MAPI.</span><span class="sxs-lookup"><span data-stu-id="2a8ad-112">Extended MAPI is the same as MAPI, and is simply referred to as MAPI in the MAPI documentation.</span></span> 
  
 <span data-ttu-id="2a8ad-113">**Simple MAPI**</span><span class="sxs-lookup"><span data-stu-id="2a8ad-113">**Simple MAPI**</span></span>
  
<span data-ttu-id="2a8ad-114">Simple MAPI proporciona un conjunto de funciones que permite agregar un nivel básico de funcionalidad de mensajería a las aplicaciones basadas en Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2a8ad-114">Simple MAPI provides a set of functions that enables you to add a basic level of messaging functionality to Microsoft Windows-based applications.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="2a8ad-115">La función de MAPI simple MAPISendMail es compatible con Microsoft Outlook 2013 y Microsoft Outlook 2010.</span><span class="sxs-lookup"><span data-stu-id="2a8ad-115">The Simple MAPI function MAPISendMail is supported by Microsoft Outlook 2013 and Microsoft Outlook 2010.</span></span> <span data-ttu-id="2a8ad-116">Otras funciones MAPI sencillas han quedado en desuso en Windows.</span><span class="sxs-lookup"><span data-stu-id="2a8ad-116">Other Simple MAPI functions have been deprecated in Windows.</span></span> 
  

