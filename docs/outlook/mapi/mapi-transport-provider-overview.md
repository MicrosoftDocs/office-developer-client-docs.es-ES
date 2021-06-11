---
title: Introducción al proveedor de transporte MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b193e819-749e-4642-8afc-dbc47b17b617
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 20b03f7c52ec86d1fb554bf69c53947c3dda4f36
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404578"
---
# <a name="mapi-transport-provider-overview"></a><span data-ttu-id="dc666-103">Introducción al proveedor de transporte MAPI</span><span class="sxs-lookup"><span data-stu-id="dc666-103">MAPI Transport Provider Overview</span></span>

  
  
<span data-ttu-id="dc666-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc666-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc666-105">Los proveedores de transporte controlan la transmisión y recepción de mensajes e implementan la seguridad, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="dc666-105">Transport providers handle message transmission and reception and implement security, if necessary.</span></span> <span data-ttu-id="dc666-106">También se encargan de las tareas necesarias de preprocesamiento y postprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="dc666-106">They also take care of any necessary preprocessing and postprocessing tasks.</span></span> <span data-ttu-id="dc666-107">Normalmente hay un proveedor de transporte para cada sistema de mensajería activo.</span><span class="sxs-lookup"><span data-stu-id="dc666-107">There is typically one transport provider for every active messaging system.</span></span>
  
<span data-ttu-id="dc666-108">Las aplicaciones cliente se comunican con el proveedor de transporte a través de un proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="dc666-108">Client applications communicate with the transport provider through a message store provider.</span></span> 
  
<span data-ttu-id="dc666-109">Los proveedores de transporte se registran con MAPI para controlar uno o varios tipos concretos de entradas de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="dc666-109">Transport providers register with MAPI to handle one or more particular types of recipient entries.</span></span> <span data-ttu-id="dc666-110">Cuando un mensaje está listo para enviarse, MAPI debe determinar qué proveedor de transporte debe controlar la transmisión.</span><span class="sxs-lookup"><span data-stu-id="dc666-110">When a message is ready to be sent, MAPI must determine which transport provider should handle the transmission.</span></span> <span data-ttu-id="dc666-111">Según el tipo de destinatario, MAPI incluso puede llamar a más de un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="dc666-111">Depending on the type of recipient, MAPI can even call upon more than one transport provider.</span></span> <span data-ttu-id="dc666-112">Si un proveedor de transporte no disponible es el único que puede controlar el destinatario, la transmisión de mensajes se pospondrá hasta que se pueda restablecer una conexión con ese proveedor.</span><span class="sxs-lookup"><span data-stu-id="dc666-112">If an unavailable transport provider is the only one that can handle the recipient, the message transmission will be postponed until a connection with that provider can be reestablished.</span></span>
  
<span data-ttu-id="dc666-113">Algunos sistemas de mensajería son sistemas seguros; todos los usuarios potenciales deben escribir un conjunto de credenciales válidas antes de permitir el acceso.</span><span class="sxs-lookup"><span data-stu-id="dc666-113">Some messaging systems are secure systems; all potential users are required to enter a set of valid credentials before access is permitted.</span></span> <span data-ttu-id="dc666-114">MAPI impide el acceso no autorizado a estos sistemas de mensajería segura al hacer que el proveedor de transporte valide las credenciales en el momento del inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="dc666-114">MAPI prevents unauthorized access to such secure messaging systems by having the transport provider validate credentials at logon time.</span></span> 
  

