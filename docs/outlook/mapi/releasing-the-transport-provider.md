---
title: Publicar el proveedor de transporte
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e0f37485-55c9-40f0-bc8c-48f7297f9f50
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: 41d953db8e00ff52cd09a27e2f7550f9f1879321
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386225"
---
# <a name="releasing-the-transport-provider"></a><span data-ttu-id="c9571-103">Publicar el proveedor de transporte</span><span class="sxs-lookup"><span data-stu-id="c9571-103">Releasing the Transport Provider</span></span>

 
  
<span data-ttu-id="c9571-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9571-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9571-105">Cuando MAPI o la cola MAPI termina de usar un objeto de inicio de sesión de transporte:</span><span class="sxs-lookup"><span data-stu-id="c9571-105">When MAPI or the MAPI spooler finishes using a transport logon object:</span></span>
  
1. <span data-ttu-id="c9571-106">MAPI o la cola MAPI llama (método [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) ) del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="c9571-106">MAPI or the MAPI spooler calls the transport provider's [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method.</span></span> 
    
2. <span data-ttu-id="c9571-107">El proveedor de transporte invalida el objeto de estado llamando al método [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) .</span><span class="sxs-lookup"><span data-stu-id="c9571-107">The transport provider invalidates the status object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method.</span></span> <span data-ttu-id="c9571-108">Si el proveedor de transporte invalida los objetos de mensaje que se va a enviados o recibidos en el momento de la llamada **TransportLogoff** dependen de los indicadores que se han pasado a **TransportLogoff**.</span><span class="sxs-lookup"><span data-stu-id="c9571-108">Whether the transport provider invalidates message objects that are being sent or received at the time of the **TransportLogoff** call depends on the flags that were passed to **TransportLogoff**.</span></span>
    
3. <span data-ttu-id="c9571-109">El proveedor de transporte llama a [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) (método) del objeto de soporte técnico para quitar la fila del proveedor de transporte de la tabla de estado y quitar de las tablas internas cualquier identificadores únicos (UID) que se han establecido con el [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) (método).</span><span class="sxs-lookup"><span data-stu-id="c9571-109">The transport provider calls the support object's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to remove the transport provider's row from the status table and remove from internal tables any unique identifiers (UIDs) that were set with the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="c9571-110">Se disminuye el recuento de objetos de inicio de sesión conocido activos en este objeto de proveedor.</span><span class="sxs-lookup"><span data-stu-id="c9571-110">It decrements the count of known logon objects active on this provider object.</span></span> <span data-ttu-id="c9571-111">Si el recuento llega a cero, MAPI llama al método [IXPProvider::Shutdown](ixpprovider-shutdown.md) y la **versión** en el objeto de proveedor.</span><span class="sxs-lookup"><span data-stu-id="c9571-111">If the count reaches zero, MAPI calls the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method and **Release** on the provider object.</span></span> <span data-ttu-id="c9571-112">Si éste era el último objeto de proveedor conocidos con este archivo DLL en este proceso, MAPI llama a la función **FreeLibrary** en el archivo DLL en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="c9571-112">If this was the last known provider object using this DLL on this process, MAPI calls the **FreeLibrary** function on the DLL at a later time.</span></span> <span data-ttu-id="c9571-113">Se libera memoria para el objeto de soporte técnico MAPI y devuelve el objeto compatible con el método de **versión** .</span><span class="sxs-lookup"><span data-stu-id="c9571-113">Memory for the MAPI support object is freed and the support object **Release** method returns.</span></span> 
    
4. <span data-ttu-id="c9571-114">El método **TransportLogoff** devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="c9571-114">The **TransportLogoff** method returns S_OK.</span></span> 
    
5. <span data-ttu-id="c9571-115">MAPI o la cola MAPI llama a **Release** en el objeto de inicio de sesión del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="c9571-115">MAPI or the MAPI spooler calls **Release** on the transport provider's logon object.</span></span> <span data-ttu-id="c9571-116">Se libera la memoria para el objeto.</span><span class="sxs-lookup"><span data-stu-id="c9571-116">The memory for the object is released.</span></span> 
    
6. <span data-ttu-id="c9571-117">MAPI o la cola MAPI llama **FreeLibrary** en el archivo DLL del proveedor.</span><span class="sxs-lookup"><span data-stu-id="c9571-117">MAPI or the MAPI spooler calls **FreeLibrary** on the provider DLL.</span></span> 
    
<span data-ttu-id="c9571-118">Para solidez, los objetos de inicio de sesión y proveedor deben ser capaces de controlar las llamadas de **versión** finales en ellos mismos sin tener primero sus **TransportLogoff** o métodos que se **cierre** llama.</span><span class="sxs-lookup"><span data-stu-id="c9571-118">For robustness, the logon and provider objects should be able to handle final **Release** calls on themselves without first having their **TransportLogoff** or **Shutdown** methods called.</span></span> <span data-ttu-id="c9571-119">Si se llama a **Release** en tales casos, los proveedores de transporte deben tratar las llamadas como si hubiera llamado **TransportLogoff** o **apagado** con un cero argumento seguido de **Release**.</span><span class="sxs-lookup"><span data-stu-id="c9571-119">If **Release** is called in such cases, transport providers should treat the calls as if **TransportLogoff** or **Shutdown** had been called with a zero argument followed by **Release**.</span></span>
  

