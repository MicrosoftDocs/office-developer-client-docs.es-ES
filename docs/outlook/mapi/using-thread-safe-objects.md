---
title: Uso de Thread-Safe objetos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e688db5e-d1a1-4afc-998f-b3d31eb6239b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 611e0a49f0fd8df8fe40205a33ed5501055c3d45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425172"
---
# <a name="using-thread-safe-objects"></a><span data-ttu-id="54e74-103">Uso de Thread-Safe objetos</span><span class="sxs-lookup"><span data-stu-id="54e74-103">Using Thread-Safe Objects</span></span>

  
  
<span data-ttu-id="54e74-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54e74-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54e74-105">Las aplicaciones cliente pueden suponer que los objetos usados directamente o como devoluciones de llamada siempre son seguros para subprocesos, excepto en los siguientes casos:</span><span class="sxs-lookup"><span data-stu-id="54e74-105">Client applications can assume that objects used directly or as callbacks are always thread-safe except in the following cases:</span></span>
  
- <span data-ttu-id="54e74-106">Objeto de estado de un proveedor de transporte obtenido a través de una llamada de cliente a [IMAPISession::OpenEntry con](imapisession-openentry.md) un identificador de entrada de la fila de tabla de estado del proveedor.</span><span class="sxs-lookup"><span data-stu-id="54e74-106">A transport provider's status object obtained through a client call to [IMAPISession::OpenEntry](imapisession-openentry.md) with an entry identifier from the provider's status table row.</span></span> 
    
- <span data-ttu-id="54e74-107">Todos los objetos de formulario MAPI obtenidos a través de una llamada de cliente a [MAPIOpenFormMgr](mapiopenformmgr.md).</span><span class="sxs-lookup"><span data-stu-id="54e74-107">All MAPI form objects obtained through a client call to [MAPIOpenFormMgr](mapiopenformmgr.md).</span></span> <span data-ttu-id="54e74-108">Los objetos de formulario cumplen las reglas del modelo de departamentos y los clientes deben usarlos y todos los objetos contenidos en ellos solo en el subproceso que las creó.</span><span class="sxs-lookup"><span data-stu-id="54e74-108">Form objects obey apartment model rules and clients must use them and all objects contained by them only on the thread that created them.</span></span>
    
<span data-ttu-id="54e74-109">Cuando un cliente tiene acceso a la fila de un proveedor de transporte en la tabla de estado que incluye el identificador de entrada del objeto de estado asociado, el cliente puede llamar a **OpenEntry** con ese identificador de entrada para abrir el objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="54e74-109">When a client accesses a transport provider's row in the status table that includes the entry identifier of the associated status object, the client can call **OpenEntry** with that entry identifier to open the status object.</span></span> <span data-ttu-id="54e74-110">Este objeto de estado no es seguro para subprocesos porque los proveedores de transporte se ejecutan en el contexto de la cola MAPI y no mantienen un contexto independiente para su objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="54e74-110">This status object is not thread-safe because transport providers run in the context of the MAPI spooler and do not maintain a separate context for their status object.</span></span> <span data-ttu-id="54e74-111">El objeto de estado cumple las reglas del modelo de departamentos y los clientes solo deben usarlo en el subproceso que lo creó.</span><span class="sxs-lookup"><span data-stu-id="54e74-111">The status object obeys apartment model rules and clients must use it only on the thread that created it.</span></span> 
  
<span data-ttu-id="54e74-112">Un cliente también debe invocar [MAPIInitialize](mapiinitialize.md) en cada subproceso antes de usar cualquier objeto MAPI y [MAPIUninitialize](mapiuninitialize.md) cuando se complete ese uso.</span><span class="sxs-lookup"><span data-stu-id="54e74-112">A client must also invoke [MAPIInitialize](mapiinitialize.md) on every thread before using any MAPI objects and [MAPIUninitialize](mapiuninitialize.md) when that use is complete.</span></span> <span data-ttu-id="54e74-113">Estas llamadas deben realizarse incluso si los objetos que se van a usar se pasan al subproceso desde un origen externo.</span><span class="sxs-lookup"><span data-stu-id="54e74-113">These calls should be made even if the objects to be used are passed to the thread from an external source.</span></span> <span data-ttu-id="54e74-114">Se puede llamar a **MAPIInitialize** y **MAPIUninitialize** desde cualquier lugar excepto desde dentro de una función **DllMain** de Win32, una función que invoca el sistema cuando se inicializan y finalizan procesos y subprocesos, o cuando se llaman a las funciones **LoadLibrary** y **FreeLibrary.**</span><span class="sxs-lookup"><span data-stu-id="54e74-114">**MAPIInitialize** and **MAPIUninitialize** can be called from anywhere except from within a Win32 **DllMain** function, a function that is invoked by the system when processes and threads are initialized and terminated, or upon calls to the **LoadLibrary** and **FreeLibrary** functions.</span></span> 
  
<span data-ttu-id="54e74-115">Nunca se debe suponer que los objetos de uso indirecto son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="54e74-115">Indirect use objects should never be assumed to be thread-safe.</span></span> <span data-ttu-id="54e74-116">Los métodos que requieren punteros de interfaz de destino como parámetros de entrada devuelven objetos de uso indirecto.</span><span class="sxs-lookup"><span data-stu-id="54e74-116">Indirect use objects are returned by methods that require destination interface pointers as input parameters.</span></span> <span data-ttu-id="54e74-117">Algunos ejemplos de estos métodos son **IMAPIProp::CopyTo** y **CopyProps**, **IMAPIFolder::CopyFolder** y **CopyMessage** e **IMsgServiceAdmin::CopyMsgService**.</span><span class="sxs-lookup"><span data-stu-id="54e74-117">Examples of such methods are **IMAPIProp::CopyTo** and **CopyProps**, **IMAPIFolder::CopyFolder** and **CopyMessage**, and **IMsgServiceAdmin::CopyMsgService**.</span></span> <span data-ttu-id="54e74-118">Si un proveedor de servicios desea llamar a un objeto de este tipo desde un subproceso distinto del que se pasó, el proveedor es responsable de calcular explícitamente las referencias del objeto.</span><span class="sxs-lookup"><span data-stu-id="54e74-118">If a service provider wants to call such an object from a thread other than the one on which it was passed, the provider is responsible for explicitly marshaling the object.</span></span>
  

