---
title: Utilizar objetos seguros para subprocesos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e688db5e-d1a1-4afc-998f-b3d31eb6239b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 49a94b785a51b4b0c3082832145250eec0745a19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580981"
---
# <a name="using-thread-safe-objects"></a><span data-ttu-id="b6678-103">Utilizar objetos seguros para subprocesos</span><span class="sxs-lookup"><span data-stu-id="b6678-103">Using Thread-Safe Objects</span></span>

  
  
<span data-ttu-id="b6678-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6678-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6678-105">Las aplicaciones cliente pueden asumir que objetos usan directamente o como las devoluciones de llamada siempre son seguros para subprocesos, excepto en los casos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b6678-105">Client applications can assume that objects used directly or as callbacks are always thread-safe except in the following cases:</span></span>
  
- <span data-ttu-id="b6678-106">Objeto de estado del proveedor de transporte obtenido a través de una llamada de cliente a [IMAPISession::OpenEntry](imapisession-openentry.md) con un identificador de entrada de fila de tabla de estado del proveedor.</span><span class="sxs-lookup"><span data-stu-id="b6678-106">A transport provider's status object obtained through a client call to [IMAPISession::OpenEntry](imapisession-openentry.md) with an entry identifier from the provider's status table row.</span></span> 
    
- <span data-ttu-id="b6678-107">Todos los objetos de formulario MAPI obtenidos a través de una llamada de cliente a [MAPIOpenFormMgr](mapiopenformmgr.md).</span><span class="sxs-lookup"><span data-stu-id="b6678-107">All MAPI form objects obtained through a client call to [MAPIOpenFormMgr](mapiopenformmgr.md).</span></span> <span data-ttu-id="b6678-108">Objetos de formulario siguen las reglas del modelo de apartamento y deben usar los clientes ellas y todos los objetos contenidos por ellos sólo en el subproceso que los creó.</span><span class="sxs-lookup"><span data-stu-id="b6678-108">Form objects obey apartment model rules and clients must use them and all objects contained by them only on the thread that created them.</span></span>
    
<span data-ttu-id="b6678-109">Cuando un cliente obtiene acceso a la fila del proveedor de transporte de la tabla de estado que incluye el identificador de entrada del objeto de estado asociado, el cliente puede llamar a **OpenEntry** con ese identificador de entrada para abrir el objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="b6678-109">When a client accesses a transport provider's row in the status table that includes the entry identifier of the associated status object, the client can call **OpenEntry** with that entry identifier to open the status object.</span></span> <span data-ttu-id="b6678-110">Este objeto de estado no es seguros para subprocesos, debido a que los proveedores de transporte se ejecutan en el contexto de la cola MAPI y no mantienen un contexto independiente para su objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="b6678-110">This status object is not thread-safe because transport providers run in the context of the MAPI spooler and do not maintain a separate context for their status object.</span></span> <span data-ttu-id="b6678-111">El objeto de estado presta atención a las reglas del modelo de apartamento y clientes deben usar sólo en el subproceso que lo creó.</span><span class="sxs-lookup"><span data-stu-id="b6678-111">The status object obeys apartment model rules and clients must use it only on the thread that created it.</span></span> 
  
<span data-ttu-id="b6678-112">Un cliente también debe invocar [MAPIInitialize](mapiinitialize.md) en cada subproceso antes de usar los objetos MAPI y [MAPIUninitialize](mapiuninitialize.md) una vez finalizada que usan.</span><span class="sxs-lookup"><span data-stu-id="b6678-112">A client must also invoke [MAPIInitialize](mapiinitialize.md) on every thread before using any MAPI objects and [MAPIUninitialize](mapiuninitialize.md) when that use is complete.</span></span> <span data-ttu-id="b6678-113">Estas llamadas deben realizarse incluso si los objetos que se va a utilizar se pasan al subproceso de un origen externo.</span><span class="sxs-lookup"><span data-stu-id="b6678-113">These calls should be made even if the objects to be used are passed to the thread from an external source.</span></span> <span data-ttu-id="b6678-114">**MAPIInitialize** y **MAPIUninitialize** se pueden llamar desde cualquier parte excepto desde dentro de una función de Win32 **DllMain** , una función que se invoca mediante el sistema cuando se inicializan y se termina procesos y subprocesos, o tras las llamadas a la ** LoadLibrary** y funciones de **FreeLibrary** .</span><span class="sxs-lookup"><span data-stu-id="b6678-114">**MAPIInitialize** and **MAPIUninitialize** can be called from anywhere except from within a Win32 **DllMain** function, a function that is invoked by the system when processes and threads are initialized and terminated, or upon calls to the **LoadLibrary** and **FreeLibrary** functions.</span></span> 
  
<span data-ttu-id="b6678-115">Nunca se deben suponer indirecta utilizar objetos como seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="b6678-115">Indirect use objects should never be assumed to be thread-safe.</span></span> <span data-ttu-id="b6678-116">Uso indirecto objetos son devueltos por los métodos que requieren punteros de interfaz de destino como parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="b6678-116">Indirect use objects are returned by methods that require destination interface pointers as input parameters.</span></span> <span data-ttu-id="b6678-117">Ejemplos de estos métodos son **IMAPIProp::CopyTo** y **CopyProps**, **IMAPIFolder::CopyFolder** y **CopyMessage**y **IMsgServiceAdmin::CopyMsgService**.</span><span class="sxs-lookup"><span data-stu-id="b6678-117">Examples of such methods are **IMAPIProp::CopyTo** and **CopyProps**, **IMAPIFolder::CopyFolder** and **CopyMessage**, and **IMsgServiceAdmin::CopyMsgService**.</span></span> <span data-ttu-id="b6678-118">Si desea que un proveedor de servicios para llamar a este tipo de objeto desde un subproceso distinto de aquél en el que se ha pasado, el proveedor es responsable de forma explícita el cálculo de referencias del objeto.</span><span class="sxs-lookup"><span data-stu-id="b6678-118">If a service provider wants to call such an object from a thread other than the one on which it was passed, the provider is responsible for explicitly marshaling the object.</span></span>
  

