---
title: Control de sesi�n MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3bc4aea5-ab01-4ba5-a4ad-7a9a76c6bf55
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 98c4bd0dba630db32fdb2309be3d29ebc13b1131
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328227"
---
# <a name="mapi-session-handling"></a><span data-ttu-id="fe562-103">Control de sesi�n MAPI</span><span class="sxs-lookup"><span data-stu-id="fe562-103">MAPI Session Handling</span></span>

  
  
<span data-ttu-id="fe562-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe562-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe562-105">Antes de poder comunicarse con proveedores de servicios y un sistema de mensajería subyacente, debe establecer una sesión.</span><span class="sxs-lookup"><span data-stu-id="fe562-105">Before you can communicate with service providers and an underlying messaging system, you must establish a session.</span></span> <span data-ttu-id="fe562-106">Una sesión MAPI es un vínculo entre un cliente y otros componentes de MAPI.</span><span class="sxs-lookup"><span data-stu-id="fe562-106">A MAPI session is a link from a client to other MAPI components.</span></span> <span data-ttu-id="fe562-107">Como resultado de iniciar una sesión correctamente, MAPI vuelve a los clientes un puntero a un objeto de sesión (un objeto que implementa la interfaz **IMAPISession** .</span><span class="sxs-lookup"><span data-stu-id="fe562-107">As the result of successfully starting a session, MAPI returns to clients a pointer to a session object — an object that implements the **IMAPISession** interface.</span></span> <span data-ttu-id="fe562-108">Para obtener más información, vea [IMAPISession: IUnknown](imapisessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="fe562-108">For more information, see [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span> <span data-ttu-id="fe562-109">Puede usar los métodos de la interfaz **IMAPISession** para tener acceso a los objetos de la libreta de direcciones y los proveedores de almacenamiento de mensajes, tener acceso a varias tablas, Mostrar formularios, establecer las propiedades de los proveedores de transporte y realizar la administración de perfiles y del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="fe562-109">You can use the methods of the **IMAPISession** interface to access the objects of address book and message store providers, access several tables, display forms, set transport provider properties, and perform profile and message service administration.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="fe562-110">En esta sección</span><span class="sxs-lookup"><span data-stu-id="fe562-110">In this section</span></span>

[<span data-ttu-id="fe562-111">Inicio de una sesión MAPI</span><span class="sxs-lookup"><span data-stu-id="fe562-111">Starting a MAPI Session</span></span>](starting-a-mapi-session.md)
  
> <span data-ttu-id="fe562-112">Describe cómo iniciar una sesión MAPI e incluye vínculos a temas con información más detallada.</span><span class="sxs-lookup"><span data-stu-id="fe562-112">Describes how to start a MAPI session and includes links to topics with more detailed information.</span></span>
    
[<span data-ttu-id="fe562-113">Finalizar una sesión MAPI</span><span class="sxs-lookup"><span data-stu-id="fe562-113">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)
  
> <span data-ttu-id="fe562-114">Describe cómo finalizar una sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="fe562-114">Describes how to end a MAPI session.</span></span>
    
[<span data-ttu-id="fe562-115">Obtener acceso a objetos mediante la sesión</span><span class="sxs-lookup"><span data-stu-id="fe562-115">Accessing Objects by Using the Session</span></span>](accessing-objects-by-using-the-session.md)
  
> <span data-ttu-id="fe562-116">Describe cómo utilizar un puntero de sesión para tener acceso a objetos de sesión.</span><span class="sxs-lookup"><span data-stu-id="fe562-116">Describes how to use a session pointer to access session objects.</span></span>
    
[<span data-ttu-id="fe562-117">Recuperación de la identidad principal y del proveedor</span><span class="sxs-lookup"><span data-stu-id="fe562-117">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
> <span data-ttu-id="fe562-118">Describe las propiedades usadas para recuperar la identidad del proveedor y la principal.</span><span class="sxs-lookup"><span data-stu-id="fe562-118">Describes the properties used to retrieve primary and provider identity.</span></span>
    
[<span data-ttu-id="fe562-119">Tabla de estado y objetos de estado</span><span class="sxs-lookup"><span data-stu-id="fe562-119">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)
  
> <span data-ttu-id="fe562-120">Describe cómo tener acceso a la información de la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="fe562-120">Describes how to access information from the status table.</span></span>
    

