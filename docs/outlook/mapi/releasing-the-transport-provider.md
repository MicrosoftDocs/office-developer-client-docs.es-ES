---
title: Liberar el proveedor de transporte
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e0f37485-55c9-40f0-bc8c-48f7297f9f50
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: 41d953db8e00ff52cd09a27e2f7550f9f1879321
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328388"
---
# <a name="releasing-the-transport-provider"></a><span data-ttu-id="31baa-103">Liberar el proveedor de transporte</span><span class="sxs-lookup"><span data-stu-id="31baa-103">Releasing the Transport Provider</span></span>

 
  
<span data-ttu-id="31baa-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31baa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31baa-105">Cuando MAPI o la cola MAPI terminen de usar un objeto de inicio de sesión de transporte:</span><span class="sxs-lookup"><span data-stu-id="31baa-105">When MAPI or the MAPI spooler finishes using a transport logon object:</span></span>
  
1. <span data-ttu-id="31baa-106">MAPI o la cola MAPI llama al método [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="31baa-106">MAPI or the MAPI spooler calls the transport provider's [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method.</span></span> 
    
2. <span data-ttu-id="31baa-107">El proveedor de transporte invalida el objeto de estado llamando al [método IMAPISupport::MakeInvalid.](imapisupport-makeinvalid.md)</span><span class="sxs-lookup"><span data-stu-id="31baa-107">The transport provider invalidates the status object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method.</span></span> <span data-ttu-id="31baa-108">Si el proveedor de transporte invalida los objetos de mensaje que se envían o reciben en el momento de la llamada **TransportLogoff** depende de las marcas que se pasaron a **TransportLogoff**.</span><span class="sxs-lookup"><span data-stu-id="31baa-108">Whether the transport provider invalidates message objects that are being sent or received at the time of the **TransportLogoff** call depends on the flags that were passed to **TransportLogoff**.</span></span>
    
3. <span data-ttu-id="31baa-109">El proveedor de transporte llama al método [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) del objeto de soporte técnico para quitar la fila del proveedor de transporte de la tabla de estado y quitar de las tablas internas cualquier identificador único (UID) que se estableció con el método [IMAPISupport::SetProviderUID.](imapisupport-setprovideruid.md)</span><span class="sxs-lookup"><span data-stu-id="31baa-109">The transport provider calls the support object's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to remove the transport provider's row from the status table and remove from internal tables any unique identifiers (UIDs) that were set with the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="31baa-110">Disminuye el número de objetos de inicio de sesión conocidos activos en este objeto de proveedor.</span><span class="sxs-lookup"><span data-stu-id="31baa-110">It decrements the count of known logon objects active on this provider object.</span></span> <span data-ttu-id="31baa-111">Si el recuento alcanza cero, MAPI llama al método [IXPProvider::Shutdown](ixpprovider-shutdown.md) y **Release** en el objeto del proveedor.</span><span class="sxs-lookup"><span data-stu-id="31baa-111">If the count reaches zero, MAPI calls the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method and **Release** on the provider object.</span></span> <span data-ttu-id="31baa-112">Si este fue el último objeto de proveedor conocido que usa esta DLL en este proceso, MAPI llama a la función **FreeLibrary** en la DLL más adelante.</span><span class="sxs-lookup"><span data-stu-id="31baa-112">If this was the last known provider object using this DLL on this process, MAPI calls the **FreeLibrary** function on the DLL at a later time.</span></span> <span data-ttu-id="31baa-113">Se libera la memoria del objeto de compatibilidad mapi y devuelve el método **Release** del objeto de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="31baa-113">Memory for the MAPI support object is freed and the support object **Release** method returns.</span></span> 
    
4. <span data-ttu-id="31baa-114">El **método TransportLogoff** devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="31baa-114">The **TransportLogoff** method returns S_OK.</span></span> 
    
5. <span data-ttu-id="31baa-115">MAPI o la cola MAPI llama **a Release** en el objeto de inicio de sesión del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="31baa-115">MAPI or the MAPI spooler calls **Release** on the transport provider's logon object.</span></span> <span data-ttu-id="31baa-116">Se libera la memoria del objeto.</span><span class="sxs-lookup"><span data-stu-id="31baa-116">The memory for the object is released.</span></span> 
    
6. <span data-ttu-id="31baa-117">MAPI o la cola MAPI llama **a FreeLibrary** en la DLL del proveedor.</span><span class="sxs-lookup"><span data-stu-id="31baa-117">MAPI or the MAPI spooler calls **FreeLibrary** on the provider DLL.</span></span> 
    
<span data-ttu-id="31baa-118">Para mayor solidez, los objetos de inicio  de sesión y proveedor deben poder controlar las llamadas finales de release por sí mismos sin tener primero sus métodos **TransportLogoff** o **Shutdown** llamados.</span><span class="sxs-lookup"><span data-stu-id="31baa-118">For robustness, the logon and provider objects should be able to handle final **Release** calls on themselves without first having their **TransportLogoff** or **Shutdown** methods called.</span></span> <span data-ttu-id="31baa-119">Si **se llama** a Release en estos casos, los proveedores de transporte deben tratar las llamadas como si se hubiera llamado a **TransportLogoff** o **Shutdown** con un argumento cero seguido de **Release**.</span><span class="sxs-lookup"><span data-stu-id="31baa-119">If **Release** is called in such cases, transport providers should treat the calls as if **TransportLogoff** or **Shutdown** had been called with a zero argument followed by **Release**.</span></span>
  

