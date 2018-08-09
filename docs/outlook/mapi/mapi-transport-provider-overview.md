---
title: Información general sobre el proveedor de transporte MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b193e819-749e-4642-8afc-dbc47b17b617
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 11cd1040bb228d789248a89184572b87cd1688ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818236"
---
# <a name="mapi-transport-provider-overview"></a><span data-ttu-id="937ef-103">Información general sobre el proveedor de transporte MAPI</span><span class="sxs-lookup"><span data-stu-id="937ef-103">MAPI Transport Provider Overview</span></span>

  
  
<span data-ttu-id="937ef-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="937ef-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="937ef-105">Los proveedores de transporte controlan la recepción y transmisión de mensajes e implementan la seguridad, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="937ef-105">Transport providers handle message transmission and reception and implement security, if necessary.</span></span> <span data-ttu-id="937ef-106">También se ocupe de cualquier preprocesamiento necesarios y tareas de posprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="937ef-106">They also take care of any necessary preprocessing and postprocessing tasks.</span></span> <span data-ttu-id="937ef-107">No hay proveedor de transporte normalmente, uno para cada sistema de mensajería activa.</span><span class="sxs-lookup"><span data-stu-id="937ef-107">There is typically one transport provider for every active messaging system.</span></span>
  
<span data-ttu-id="937ef-108">Aplicaciones cliente se comunican con el proveedor de transporte a través de un proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="937ef-108">Client applications communicate with the transport provider through a message store provider.</span></span> 
  
<span data-ttu-id="937ef-109">Registran los proveedores de transporte con MAPI para manejar tipos específicos de una o varias de las entradas de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="937ef-109">Transport providers register with MAPI to handle one or more particular types of recipient entries.</span></span> <span data-ttu-id="937ef-110">Cuando un mensaje está listo para ser enviado, MAPI debe determinar qué proveedor de transporte debe controlar la transmisión.</span><span class="sxs-lookup"><span data-stu-id="937ef-110">When a message is ready to be sent, MAPI must determine which transport provider should handle the transmission.</span></span> <span data-ttu-id="937ef-111">Según el tipo de destinatario, MAPI incluso puede recurrir a más de un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="937ef-111">Depending on the type of recipient, MAPI can even call upon more than one transport provider.</span></span> <span data-ttu-id="937ef-112">Si un proveedor de transporte disponible es el único que puede controlar al destinatario, la transmisión del mensaje se se pospuso hasta que se puede restablecer una conexión con el proveedor.</span><span class="sxs-lookup"><span data-stu-id="937ef-112">If an unavailable transport provider is the only one that can handle the recipient, the message transmission will be postponed until a connection with that provider can be reestablished.</span></span>
  
<span data-ttu-id="937ef-113">Algunos sistemas de mensajería son los sistemas seguros; todos los usuarios potenciales tienen que escribir un conjunto de credenciales válidas para obtener acceso.</span><span class="sxs-lookup"><span data-stu-id="937ef-113">Some messaging systems are secure systems; all potential users are required to enter a set of valid credentials before access is permitted.</span></span> <span data-ttu-id="937ef-114">MAPI impide el acceso no autorizado a estos sistemas de mensajería seguros con el proveedor de transporte validar credenciales en tiempo de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="937ef-114">MAPI prevents unauthorized access to such secure messaging systems by having the transport provider validate credentials at logon time.</span></span> 
  

