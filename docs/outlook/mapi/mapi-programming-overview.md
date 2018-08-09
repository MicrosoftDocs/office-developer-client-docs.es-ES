---
title: Informaci�n general sobre programaci�n de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30ac637a-874f-4660-b5d0-d28d69486f64
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: 177bd84addb001970e52801fd2cddba3a8d81706
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818168"
---
# <a name="mapi-programming-overview"></a><span data-ttu-id="d5482-103">Informaci�n general sobre programaci�n de MAPI</span><span class="sxs-lookup"><span data-stu-id="d5482-103">MAPI Programming Overview</span></span>

  
  
<span data-ttu-id="d5482-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d5482-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d5482-105">Esta referencia de API de mensajería de Outlook (MAPI) de Microsoft se ha diseñado para C y los desarrolladores de C++ con una gran variedad de necesidades y experimentar con la mensajería.</span><span class="sxs-lookup"><span data-stu-id="d5482-105">This Microsoft Outlook Messaging API (MAPI) Reference is written for C and C++ developers with a variety of needs and experience with messaging.</span></span> <span data-ttu-id="d5482-106">Para los programadores que deseen utilizar MAPI para ampliar sus aplicaciones que tienen las características de mensajería, no es necesario ningún requisito de conocimientos específico.</span><span class="sxs-lookup"><span data-stu-id="d5482-106">For those developers who want to use MAPI to augment their applications that have messaging features, no specific prerequisite knowledge is required.</span></span> <span data-ttu-id="d5482-107">Es necesario un fondo de mensajería y el modelo de objetos de componentes (COM) a usar MAPI para crear aplicaciones de grupo de trabajo a gran escala o controladores para los servicios del sistema de mensajería especializados.</span><span class="sxs-lookup"><span data-stu-id="d5482-107">You need a background in messaging and the Component Object Model (COM) to use MAPI to create full-scale workgroup applications or drivers for specialized messaging system services.</span></span>
  
<span data-ttu-id="d5482-108">Antes de iniciar el trabajo de desarrollo, debe tener en cuenta la siguiente información acerca de cómo usar MAPI, el proceso de inicio de sesión, y cómo se crean y configuran perfiles y servicios de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d5482-108">Before starting development work, you should consider the following information about how to use MAPI, the logon process, and how profiles and message services are created and configured.</span></span>
  
<span data-ttu-id="d5482-109">La interfaz de programa de aplicaciones de mensajería (MAPI) es un amplio conjunto de funciones que pueden usar los desarrolladores para crear aplicaciones habilitadas para correo.</span><span class="sxs-lookup"><span data-stu-id="d5482-109">The Messaging Application Program Interface (MAPI) is an extensive set of functions that developers can use to create mail-enabled applications.</span></span> <span data-ttu-id="d5482-110">La biblioteca de función completa se conoce como MAPI.</span><span class="sxs-lookup"><span data-stu-id="d5482-110">The full function library is known as MAPI.</span></span> <span data-ttu-id="d5482-111">MAPI permite el control completo sobre el sistema de mensajería en el equipo cliente, la creación y la administración de los mensajes, la administración de los buzones de correo de cliente, proveedores de servicios y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="d5482-111">MAPI enables complete control over the messaging system on the client computer, creation and management of messages, management of the client mailbox, service providers, and so on.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d5482-112">MAPI extendida es el mismo que MAPI y se simplemente denomina MAPI en la documentación de MAPI.</span><span class="sxs-lookup"><span data-stu-id="d5482-112">Extended MAPI is the same as MAPI, and is simply referred to as MAPI in the MAPI documentation.</span></span> 
  
 <span data-ttu-id="d5482-113">**Simple MAPI**</span><span class="sxs-lookup"><span data-stu-id="d5482-113">**Simple MAPI**</span></span>
  
<span data-ttu-id="d5482-114">Simple MAPI proporciona un conjunto de funciones que permite agregar un nivel básico de funcionalidad de mensajería a las aplicaciones basadas en Windows de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d5482-114">Simple MAPI provides a set of functions that enables you to add a basic level of messaging functionality to Microsoft Windows-based applications.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="d5482-115">La función de Simple MAPI MAPISendMail es compatible con Microsoft Outlook 2013 y Microsoft Outlook 2010.</span><span class="sxs-lookup"><span data-stu-id="d5482-115">The Simple MAPI function MAPISendMail is supported by Microsoft Outlook 2013 and Microsoft Outlook 2010.</span></span> <span data-ttu-id="d5482-116">Otras funciones de Simple MAPI han quedado obsoletos en Windows.</span><span class="sxs-lookup"><span data-stu-id="d5482-116">Other Simple MAPI functions have been deprecated in Windows.</span></span> 
  

