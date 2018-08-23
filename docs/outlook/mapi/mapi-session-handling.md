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
ms.openlocfilehash: 8c82ff28dca4fc50c7801a533f7ad757b839cddf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568234"
---
# <a name="mapi-session-handling"></a><span data-ttu-id="47f15-103">Control de sesi�n MAPI</span><span class="sxs-lookup"><span data-stu-id="47f15-103">MAPI Session Handling</span></span>

  
  
<span data-ttu-id="47f15-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47f15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47f15-105">Para poder comunicarse con proveedores de servicios y un sistema de mensajería subyacente, debe establecer una sesión.</span><span class="sxs-lookup"><span data-stu-id="47f15-105">Before you can communicate with service providers and an underlying messaging system, you must establish a session.</span></span> <span data-ttu-id="47f15-106">Una sesión MAPI es un vínculo desde un cliente a otros componentes MAPI.</span><span class="sxs-lookup"><span data-stu-id="47f15-106">A MAPI session is a link from a client to other MAPI components.</span></span> <span data-ttu-id="47f15-107">Como resultado de inicio de una sesión correctamente, MAPI devuelve a los clientes un puntero a un objeto de sesión, un objeto que implementa la interfaz **IMAPISession** .</span><span class="sxs-lookup"><span data-stu-id="47f15-107">As the result of successfully starting a session, MAPI returns to clients a pointer to a session object — an object that implements the **IMAPISession** interface.</span></span> <span data-ttu-id="47f15-108">Para obtener más información, vea [IMAPISession: IUnknown](imapisessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="47f15-108">For more information, see [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span> <span data-ttu-id="47f15-109">Puede usar los métodos de la interfaz **IMAPISession** para tener acceso a los objetos de proveedores de almacenes de libreta de direcciones y el mensaje de dirección, obtener acceso a varias tablas, mostrar formularios, establecer propiedades del proveedor de transporte y realizar la administración del servicio de perfil y el mensaje.</span><span class="sxs-lookup"><span data-stu-id="47f15-109">You can use the methods of the **IMAPISession** interface to access the objects of address book and message store providers, access several tables, display forms, set transport provider properties, and perform profile and message service administration.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="47f15-110">En esta sección</span><span class="sxs-lookup"><span data-stu-id="47f15-110">In this section</span></span>

[<span data-ttu-id="47f15-111">Iniciar una sesión MAPI</span><span class="sxs-lookup"><span data-stu-id="47f15-111">Starting a MAPI Session</span></span>](starting-a-mapi-session.md)
  
> <span data-ttu-id="47f15-112">Describe cómo iniciar una sesión MAPI e incluye vínculos a temas con información más detallada.</span><span class="sxs-lookup"><span data-stu-id="47f15-112">Describes how to start a MAPI session and includes links to topics with more detailed information.</span></span>
    
[<span data-ttu-id="47f15-113">Finalizar una sesión MAPI</span><span class="sxs-lookup"><span data-stu-id="47f15-113">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)
  
> <span data-ttu-id="47f15-114">Se describe cómo finalizar una sesión de MAPI.</span><span class="sxs-lookup"><span data-stu-id="47f15-114">Describes how to end a MAPI session.</span></span>
    
[<span data-ttu-id="47f15-115">Obtener acceso a los objetos con la sesión</span><span class="sxs-lookup"><span data-stu-id="47f15-115">Accessing Objects by Using the Session</span></span>](accessing-objects-by-using-the-session.md)
  
> <span data-ttu-id="47f15-116">Describe cómo utilizar un puntero de sesión para tener acceso a objetos de la sesión.</span><span class="sxs-lookup"><span data-stu-id="47f15-116">Describes how to use a session pointer to access session objects.</span></span>
    
[<span data-ttu-id="47f15-117">Recuperar identidades de proveedor y principales</span><span class="sxs-lookup"><span data-stu-id="47f15-117">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
> <span data-ttu-id="47f15-118">Se describen las propiedades que se usan para recuperar principal y la identidad del proveedor.</span><span class="sxs-lookup"><span data-stu-id="47f15-118">Describes the properties used to retrieve primary and provider identity.</span></span>
    
[<span data-ttu-id="47f15-119">Tabla de estado y objetos de estado</span><span class="sxs-lookup"><span data-stu-id="47f15-119">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)
  
> <span data-ttu-id="47f15-120">Describe cómo obtener acceso a información desde la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="47f15-120">Describes how to access information from the status table.</span></span>
    

