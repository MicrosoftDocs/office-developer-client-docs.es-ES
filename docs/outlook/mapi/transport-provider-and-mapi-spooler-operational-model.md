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
ms.openlocfilehash: 26d9982248fde015a584eb79cc248bafc5afc6bb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594036"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a><span data-ttu-id="8b234-103">Proveedor de transporte y modelo operativo de administrador de trabajos en cola MAPI</span><span class="sxs-lookup"><span data-stu-id="8b234-103">Transport Provider and MAPI Spooler Operational Model</span></span>

  
  
<span data-ttu-id="8b234-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b234-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b234-105">Inicialización del proveedor de transporte, inicio, procesamiento, cierre y deinitialization se llevan a cabo mediante una serie de llamadas desde la cola de MAPI para el proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="8b234-105">Transport provider initialization, startup, processing, shutdown and deinitialization are accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="8b234-106">Las llamadas se ordenan de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8b234-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="8b234-107">La cola MAPI llama a la función [XPProviderInit](xpproviderinit.md) , pasa un objeto de soporte técnico, obtiene el objeto de proveedor y comprueba que el proveedor de transporte y la cola MAPI admiten un números de versión compatible de intervalo de MAPI.</span><span class="sxs-lookup"><span data-stu-id="8b234-107">The MAPI spooler calls the [XPProviderInit](xpproviderinit.md) function, passes a support object, gets the provider object, and checks that the transport provider and MAPI spooler support a compatible range of MAPI version numbers.</span></span> 
    
2. <span data-ttu-id="8b234-108">La cola MAPI llama al método [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) de la [IXPProvider: IUnknown](ixpprovideriunknown.md) interfaz.</span><span class="sxs-lookup"><span data-stu-id="8b234-108">The MAPI spooler calls the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method of the [IXPProvider : IUnknown](ixpprovideriunknown.md) interface.</span></span> <span data-ttu-id="8b234-109">Se establece una sesión entre la cola MAPI y el proveedor de transporte con las credenciales en la sección del perfil actual.</span><span class="sxs-lookup"><span data-stu-id="8b234-109">A session is established between the MAPI spooler and the transport provider with the credentials in the current section of the profile.</span></span> <span data-ttu-id="8b234-110">El proveedor de transporte devuelve un objeto de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="8b234-110">The transport provider returns a logon object.</span></span> 
    
3. <span data-ttu-id="8b234-111">La cola MAPI llama al método de [IXPLogon::AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="8b234-111">The MAPI spooler calls the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="8b234-112">El proveedor de transporte devuelve una lista de los identificadores únicos (UID) y tipos de direcciones de correo electrónico que acepte.</span><span class="sxs-lookup"><span data-stu-id="8b234-112">The transport provider returns a list of the unique identifiers (UIDs) and email address types it will accept.</span></span> 
    
4. <span data-ttu-id="8b234-113">El proveedor de transporte llama al método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) para crear la fila correspondiente en la tabla de estado MAPI.</span><span class="sxs-lookup"><span data-stu-id="8b234-113">The transport provider calls the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to create its row in the MAPI status table.</span></span> 
    
5. <span data-ttu-id="8b234-114">La cola MAPI llama al método de [IXPLogon::TransportNotify](ixplogon-transportnotify.md) para habilitar la recepción y transmisión de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8b234-114">The MAPI spooler calls the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method to enable message transmission and reception.</span></span> 
    
6. <span data-ttu-id="8b234-115">Si solicitada por el proveedor de transporte de su devuelto de la llamada **TransportLogon** , la cola MAPI llama periódicamente el método [IXPLogon::Idle](ixplogon-idle.md) .</span><span class="sxs-lookup"><span data-stu-id="8b234-115">If requested by the transport provider in its return for the **TransportLogon** call, the MAPI spooler periodically calls the [IXPLogon::Idle](ixplogon-idle.md) method.</span></span> <span data-ttu-id="8b234-116">Procesamiento en inactividad es útil si el proveedor de transporte necesita sondean el sistema de mensajería subyacente para los mensajes nuevos o realizar otras tareas de prioridad baja.</span><span class="sxs-lookup"><span data-stu-id="8b234-116">Idle processing is useful if the transport provider needs to poll the underlying messaging system for new messages or perform other low-priority tasks.</span></span> 
    
7. <span data-ttu-id="8b234-117">La cola MAPI y el proveedor de transporte envían y reciben mensajes.</span><span class="sxs-lookup"><span data-stu-id="8b234-117">The MAPI spooler and transport provider send and receive messages.</span></span> <span data-ttu-id="8b234-118">Para obtener más información, vea [Modelo de envío de mensajes](message-submission-model.md) y [Modelo de recepción de mensajes](message-reception-model.md).</span><span class="sxs-lookup"><span data-stu-id="8b234-118">For more information, see [Message Submission Model](message-submission-model.md) and [Message Reception Model](message-reception-model.md).</span></span> <span data-ttu-id="8b234-119">La cola MAPI atiende las solicitudes de transporte y llama a los objetos de soporte técnico, mensajes y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="8b234-119">The MAPI spooler services transport requests and calls on support, message, and attachment objects.</span></span>
    
8. <span data-ttu-id="8b234-120">La cola MAPI llama el método **TransportNotify** para deshabilitar la recepción y transmisión de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8b234-120">The MAPI spooler calls the **TransportNotify** method to disable message transmission and reception.</span></span> 
    
9. <span data-ttu-id="8b234-121">La cola MAPI libera los objetos de inicio de sesión y proveedor.</span><span class="sxs-lookup"><span data-stu-id="8b234-121">The MAPI spooler releases the logon and provider objects.</span></span> <span data-ttu-id="8b234-122">Para obtener más información, vea el método [IXPProvider::Shutdown](ixpprovider-shutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="8b234-122">For more information, see the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method.</span></span> 
    

