---
title: Proveedor de transporte y modelo operativo de administrador de trabajos en cola MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b0f8d8f0-fed7-4a7c-bc40-e935f159591d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5987111844f087801c63989b905992900ff6909c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426628"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a><span data-ttu-id="1fcfc-103">Proveedor de transporte y modelo operativo de administrador de trabajos en cola MAPI</span><span class="sxs-lookup"><span data-stu-id="1fcfc-103">Transport Provider and MAPI Spooler Operational Model</span></span>

  
  
<span data-ttu-id="1fcfc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1fcfc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1fcfc-105">La inicialización, el inicio, el procesamiento, el apagado y la desinicialización del proveedor de transporte se realizan mediante una serie de llamadas de la cola MAPI al proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="1fcfc-105">Transport provider initialization, startup, processing, shutdown and deinitialization are accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="1fcfc-106">Las llamadas se ordenan de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="1fcfc-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="1fcfc-107">La cola MAPI llama a la función [XPProviderInit](xpproviderinit.md) , pasa un objeto de soporte, obtiene el objeto de proveedor y comprueba que el proveedor de transporte y la cola MAPI admiten un intervalo de números de versión MAPI compatible.</span><span class="sxs-lookup"><span data-stu-id="1fcfc-107">The MAPI spooler calls the [XPProviderInit](xpproviderinit.md) function, passes a support object, gets the provider object, and checks that the transport provider and MAPI spooler support a compatible range of MAPI version numbers.</span></span> 
    
2. <span data-ttu-id="1fcfc-108">La cola MAPI llama al método [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) de la interfaz [IXPProvider: IUnknown](ixpprovideriunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="1fcfc-108">The MAPI spooler calls the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method of the [IXPProvider : IUnknown](ixpprovideriunknown.md) interface.</span></span> <span data-ttu-id="1fcfc-109">Se establece una sesión entre la cola MAPI y el proveedor de transporte con las credenciales de la sección actual del perfil.</span><span class="sxs-lookup"><span data-stu-id="1fcfc-109">A session is established between the MAPI spooler and the transport provider with the credentials in the current section of the profile.</span></span> <span data-ttu-id="1fcfc-110">El proveedor de transporte devuelve un objeto de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="1fcfc-110">The transport provider returns a logon object.</span></span> 
    
3. <span data-ttu-id="1fcfc-111">La cola MAPI llama al método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="1fcfc-111">The MAPI spooler calls the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="1fcfc-112">El proveedor de transporte devuelve una lista de los identificadores únicos (UID) y los tipos de direcciones de correo electrónico que aceptará.</span><span class="sxs-lookup"><span data-stu-id="1fcfc-112">The transport provider returns a list of the unique identifiers (UIDs) and email address types it will accept.</span></span> 
    
4. <span data-ttu-id="1fcfc-113">El proveedor de transporte llama al método [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) para crear su fila en la tabla de estado de MAPI.</span><span class="sxs-lookup"><span data-stu-id="1fcfc-113">The transport provider calls the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to create its row in the MAPI status table.</span></span> 
    
5. <span data-ttu-id="1fcfc-114">La cola MAPI llama al método [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) para habilitar la transmisión y recepción de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1fcfc-114">The MAPI spooler calls the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method to enable message transmission and reception.</span></span> 
    
6. <span data-ttu-id="1fcfc-115">Si el proveedor de transporte lo solicita en su devolución para la llamada **TransportLogon** , la cola MAPI llama periódicamente al método [IXPLogon:: idle](ixplogon-idle.md) .</span><span class="sxs-lookup"><span data-stu-id="1fcfc-115">If requested by the transport provider in its return for the **TransportLogon** call, the MAPI spooler periodically calls the [IXPLogon::Idle](ixplogon-idle.md) method.</span></span> <span data-ttu-id="1fcfc-116">El procesamiento en inActividad es útil si el proveedor de transporte debe sondear el sistema de mensajería subyacente en busca de nuevos mensajes o realizar otras tareas de baja prioridad.</span><span class="sxs-lookup"><span data-stu-id="1fcfc-116">Idle processing is useful if the transport provider needs to poll the underlying messaging system for new messages or perform other low-priority tasks.</span></span> 
    
7. <span data-ttu-id="1fcfc-117">La cola MAPI y el proveedor de transporte envían y reciben mensajes.</span><span class="sxs-lookup"><span data-stu-id="1fcfc-117">The MAPI spooler and transport provider send and receive messages.</span></span> <span data-ttu-id="1fcfc-118">Para obtener más información, vea [modelo de envío de mensajes](message-submission-model.md) y modelo de recepción de [mensajes](message-reception-model.md).</span><span class="sxs-lookup"><span data-stu-id="1fcfc-118">For more information, see [Message Submission Model](message-submission-model.md) and [Message Reception Model](message-reception-model.md).</span></span> <span data-ttu-id="1fcfc-119">Los servicios de cola MAPI transportan solicitudes de transporte y llamadas en objetos de soporte, mensajes y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="1fcfc-119">The MAPI spooler services transport requests and calls on support, message, and attachment objects.</span></span>
    
8. <span data-ttu-id="1fcfc-120">La cola MAPI llama al método **TransportNotify** para deshabilitar la transmisión y recepción de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1fcfc-120">The MAPI spooler calls the **TransportNotify** method to disable message transmission and reception.</span></span> 
    
9. <span data-ttu-id="1fcfc-121">La cola MAPI libera los objetos de inicio de sesión y proveedor.</span><span class="sxs-lookup"><span data-stu-id="1fcfc-121">The MAPI spooler releases the logon and provider objects.</span></span> <span data-ttu-id="1fcfc-122">Para obtener más información, vea el método [IXPProvider:: Shutdown](ixpprovider-shutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="1fcfc-122">For more information, see the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method.</span></span> 
    

