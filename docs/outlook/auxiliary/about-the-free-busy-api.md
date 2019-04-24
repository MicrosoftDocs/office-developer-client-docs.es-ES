---
title: Información sobre la API de disponibilidad
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: La API de disponibilidad permite que los proveedores de correo proporcionen información de estado de disponibilidad para las cuentas de usuario especificadas dentro de un intervalo de tiempo especificado.
ms.openlocfilehash: 1bcd191b57238771ede6f035216fe3997e82e03a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317013"
---
# <a name="about-the-freebusy-api"></a><span data-ttu-id="18cad-103">Información sobre la API de disponibilidad</span><span class="sxs-lookup"><span data-stu-id="18cad-103">About the Free/Busy API</span></span>

<span data-ttu-id="18cad-104">La API de disponibilidad permite que los proveedores de correo proporcionen información de estado de disponibilidad para las cuentas de usuario especificadas dentro de un intervalo de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="18cad-104">The Free/Busy API allows mail providers to provide free/busy status information for specified user accounts within a specified time range.</span></span> <span data-ttu-id="18cad-105">El estado de disponibilidad de un bloque de tiempo en el calendario de un usuario es uno de los siguientes: fuera de la oficina, ocupado, provisional o libre.</span><span class="sxs-lookup"><span data-stu-id="18cad-105">The free/busy status of a block of time on a user's calendar is one of the following: out-of-office, busy, tentative, or free.</span></span>
  
## <a name="create-a-freebusy-provider"></a><span data-ttu-id="18cad-106">Crear un proveedor de disponibilidad</span><span class="sxs-lookup"><span data-stu-id="18cad-106">Create a free/busy provider</span></span>

<span data-ttu-id="18cad-107">Para proporcionar información de disponibilidad a los usuarios de correo, un proveedor de correo crea un proveedor de disponibilidad y lo registra en Outlook.</span><span class="sxs-lookup"><span data-stu-id="18cad-107">To provide free/busy information to mail users, a mail provider creates a free/busy provider and registers it with Outlook.</span></span> <span data-ttu-id="18cad-108">El proveedor de disponibilidad debe implementar las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="18cad-108">The free/busy provider must implement the following interfaces.</span></span> <span data-ttu-id="18cad-109">Tenga en cuenta que no se admiten varios miembros en estas interfaces y deben devolver los valores devueltos especificados.</span><span class="sxs-lookup"><span data-stu-id="18cad-109">Note that a number of members in these interfaces are not supported and must return the specified return values.</span></span> <span data-ttu-id="18cad-110">En concreto, la API de disponibilidad no admite el acceso de escritura a la información de disponibilidad y el acceso delegado a las cuentas.</span><span class="sxs-lookup"><span data-stu-id="18cad-110">In particular, the Free/Busy API does not support write access to free/busy information and delegate access to accounts.</span></span>
  
- <span data-ttu-id="18cad-111">[IFreeBusySupport](ifreebusysupport.md) : esta interfaz admite la especificación de interfaces que tienen acceso a los datos de disponibilidad de los usuarios especificados.</span><span class="sxs-lookup"><span data-stu-id="18cad-111">[IFreeBusySupport](ifreebusysupport.md) —This interface supports specification of interfaces that access free/busy data for specified users.</span></span> <span data-ttu-id="18cad-112">Usa [FBUser](fbuser.md) para identificar a un usuario.</span><span class="sxs-lookup"><span data-stu-id="18cad-112">It uses [FBUser](fbuser.md) to identify a user.</span></span> 
    
- <span data-ttu-id="18cad-113">[IFreeBusyData](ifreebusydata.md) : esta interfaz obtiene y establece un intervalo de tiempo para un usuario determinado y devuelve una interfaz para enumerar los bloques de disponibilidad de datos dentro de este intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="18cad-113">[IFreeBusyData](ifreebusydata.md) —This interface gets and sets a time range for a given user and returns an interface for enumerating free/busy blocks of data within this time range.</span></span> <span data-ttu-id="18cad-114">Usa el tiempo relativo para obtener y establecer este intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="18cad-114">It uses relative time to get and set this time range.</span></span> <span data-ttu-id="18cad-115">Para obtener más información, vea [usar tiempo relativo para obtener acceso a los datos de disponibilidad](how-to-use-relative-time-to-access-free-busy-data.md).</span><span class="sxs-lookup"><span data-stu-id="18cad-115">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
- <span data-ttu-id="18cad-116">[IEnumFBBlock](ienumfbblock.md) : esta interfaz admite el acceso y la enumeración de bloques de disponibilidad de datos para un usuario dentro de un intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="18cad-116">[IEnumFBBlock](ienumfbblock.md) —This interface supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="18cad-117">Una enumeración contiene bloques de disponibilidad que indican el estado de disponibilidad de períodos de tiempo en el calendario de un usuario, dentro de un intervalo de tiempo (especificado por [IFreeBusyData:: EnumBlocks](ifreebusydata-enumblocks.md)).</span><span class="sxs-lookup"><span data-stu-id="18cad-117">An enumeration contains free/busy blocks that indicate the free/busy status of periods of time on a user's calendar, within a time range (specified by [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)).</span></span> <span data-ttu-id="18cad-118">Elementos de un calendario, como citas y convocatorias de reunión, bloques de formulario en la enumeración.</span><span class="sxs-lookup"><span data-stu-id="18cad-118">Items on a calendar, such as appointments and meeting requests, form blocks in the enumeration.</span></span> <span data-ttu-id="18cad-119">Los elementos que están adyacentes entre sí en el calendario y tienen el mismo estado de disponibilidad se combinan para formar un único bloque.</span><span class="sxs-lookup"><span data-stu-id="18cad-119">Items that are adjacent to one another on the calendar and have the same free/busy status are combined to form one single block.</span></span> <span data-ttu-id="18cad-120">Un período de tiempo gratuito en un calendario también forma un bloque.</span><span class="sxs-lookup"><span data-stu-id="18cad-120">A free period of time on a calendar also forms a block.</span></span> <span data-ttu-id="18cad-121">Por lo tanto, dos bloques consecutivos en una enumeración no tendrían el mismo estado de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="18cad-121">Therefore, no two consecutive blocks in an enumeration would have the same free/busy status.</span></span> <span data-ttu-id="18cad-122">Estos bloques no se superponen en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="18cad-122">These blocks do not overlap in time.</span></span> <span data-ttu-id="18cad-123">Cuando hay elementos superpuestos en un calendario, Outlook combina estos elementos para formar bloques de disponibilidad no superpuestos en la enumeración según este orden de prioridad: fuera de la oficina, no disponible, provisional.</span><span class="sxs-lookup"><span data-stu-id="18cad-123">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span> 
  
<span data-ttu-id="18cad-124">Para registrar el proveedor de disponibilidad con Outlook, el proveedor de correo debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="18cad-124">To register the free/busy provider with Outlook, the mail provider should do the following:</span></span>
  
1. <span data-ttu-id="18cad-125">Registre el proveedor de disponibilidad con COM y proporcione un CLSID que permita el acceso a la implementación del proveedor de **IFreeBusySupport**.</span><span class="sxs-lookup"><span data-stu-id="18cad-125">Register the free/busy provider with COM, providing a CLSID that allows access to the provider's implementation of **IFreeBusySupport**.</span></span> 
    
2. <span data-ttu-id="18cad-126">Deje que Outlook sepa que el proveedor de disponibilidad existe estableciendo la siguiente clave (donde `<xx.x>` representa la versión de Outlook) en el registro del sistema:</span><span class="sxs-lookup"><span data-stu-id="18cad-126">Let Outlook know that the free/busy provider exists by setting the following key (where `<xx.x>` represents the version of Outlook) in the system registry:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   <span data-ttu-id="18cad-127">Por ejemplo, si el proveedor de transporte es SMTP, para registrar el proveedor con Microsoft Outlook 2010, establezca la siguiente clave en los datos de la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="18cad-127">For example, if the transport provider is SMTP, to register the provider with Microsoft Outlook 2010, set the following key to the data in the following table:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |<span data-ttu-id="18cad-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="18cad-128">Name</span></span> |<span data-ttu-id="18cad-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="18cad-129">Type</span></span> |<span data-ttu-id="18cad-130">Valor</span><span class="sxs-lookup"><span data-stu-id="18cad-130">Value</span></span> |
   |:-----|:-----|:-----|
   |<span data-ttu-id="18cad-131">SMTP</span><span class="sxs-lookup"><span data-stu-id="18cad-131">SMTP</span></span>  |<span data-ttu-id="18cad-132">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="18cad-132">REG_SZ</span></span>  |<span data-ttu-id="18cad-133">{CLSID para la implementación respectiva de IFreeBusySupport}</span><span class="sxs-lookup"><span data-stu-id="18cad-133">{CLSID for respective implementation of IFreeBusySupport}</span></span>  |
   
   <span data-ttu-id="18cad-134">En este escenario, Outlook cocrea la clase COM y la usa para recuperar la información de disponibilidad de los usuarios de correo SMTP.</span><span class="sxs-lookup"><span data-stu-id="18cad-134">In this scenario, Outlook co-creates the COM class and uses it to retrieve free/busy information for any SMTP mail users.</span></span>
    
<span data-ttu-id="18cad-135">Para admitir una libreta de direcciones y un proveedor de transporte que usen un tipo de entrada de dirección que no sea SMTP, cambie el *nombre* en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="18cad-135">To support an address book and transport provider that use an address entry type other than SMTP, change the  *Name* accordingly.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="18cad-136">Durante la instalación, los proveedores de disponibilidad deben comprobar si ya existe una configuración del registro para el mismo tipo de entrada de dirección.</span><span class="sxs-lookup"><span data-stu-id="18cad-136">During installation, free/busy providers should check whether a registry setting for the the same address entry type already exists.</span></span> <span data-ttu-id="18cad-137">Si es así, el proveedor de disponibilidad debe sobrescribir el proveedor actual para ese tipo de entrada de dirección y restaurar a ese proveedor al desinstalar.</span><span class="sxs-lookup"><span data-stu-id="18cad-137">If it does, the free/busy provider should overwrite the current provider for that address entry type, and restore to that provider when it uninstalls.</span></span> <span data-ttu-id="18cad-138">Sin embargo, si un usuario ha instalado más de un proveedor de disponibilidad para el mismo tipo de entrada de dirección, el usuario debe desinstalar estos proveedores en orden inverso como la instalación (es decir, desinstalar siempre el último proveedor).</span><span class="sxs-lookup"><span data-stu-id="18cad-138">However, if a user has installed more than one free/busy provider for the same address entry type, the user should uninstall these providers in the reverse order as installation (that is, always uninstall the latest provider).</span></span> <span data-ttu-id="18cad-139">De lo contrario, el registro puede apuntar a un proveedor que ya se ha desinstalado.</span><span class="sxs-lookup"><span data-stu-id="18cad-139">Otherwise, the registry may point to a provider that has already been uninstalled.</span></span> 
  
## <a name="api-components"></a><span data-ttu-id="18cad-140">Componentes de la API</span><span class="sxs-lookup"><span data-stu-id="18cad-140">API components</span></span>

<span data-ttu-id="18cad-141">La API de disponibilidad incluye los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="18cad-141">The Free/Busy API includes the following components:</span></span>
  
### <a name="definitions"></a><span data-ttu-id="18cad-142">Definiciones</span><span class="sxs-lookup"><span data-stu-id="18cad-142">Definitions</span></span>

- [<span data-ttu-id="18cad-143">Constantes (API de disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="18cad-143">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
    
### <a name="data-types"></a><span data-ttu-id="18cad-144">Tipos de datos</span><span class="sxs-lookup"><span data-stu-id="18cad-144">Data types</span></span>

- [<span data-ttu-id="18cad-145">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="18cad-145">FBBlock_1</span></span>](fbblock_1.md)
- [<span data-ttu-id="18cad-146">FBStatus</span><span class="sxs-lookup"><span data-stu-id="18cad-146">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="18cad-147">FBUser</span><span class="sxs-lookup"><span data-stu-id="18cad-147">FBUser</span></span>](fbuser.md)
    
### <a name="interfaces"></a><span data-ttu-id="18cad-148">Interfaces</span><span class="sxs-lookup"><span data-stu-id="18cad-148">Interfaces</span></span>

- [<span data-ttu-id="18cad-149">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="18cad-149">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="18cad-150">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="18cad-150">IFreeBusyData</span></span>](ifreebusydata.md)
- [<span data-ttu-id="18cad-151">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="18cad-151">IFreeBusySupport</span></span>](ifreebusysupport.md)
    

