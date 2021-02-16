---
title: Información sobre la API de disponibilidad
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: La API de disponibilidad permite a los proveedores de correo proporcionar información de estado de disponibilidad para cuentas de usuario especificadas dentro de un intervalo de tiempo especificado.
ms.openlocfilehash: 1bcd191b57238771ede6f035216fe3997e82e03a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433762"
---
# <a name="about-the-freebusy-api"></a><span data-ttu-id="6c5e8-103">Información sobre la API de disponibilidad</span><span class="sxs-lookup"><span data-stu-id="6c5e8-103">About the Free/Busy API</span></span>

<span data-ttu-id="6c5e8-104">La API de disponibilidad permite a los proveedores de correo proporcionar información de estado de disponibilidad para cuentas de usuario especificadas dentro de un intervalo de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="6c5e8-104">The Free/Busy API allows mail providers to provide free/busy status information for specified user accounts within a specified time range.</span></span> <span data-ttu-id="6c5e8-105">El estado de disponibilidad de un bloque de tiempo en el calendario de un usuario es uno de los siguientes: fuera de la oficina, ocupado, provisional o gratuito.</span><span class="sxs-lookup"><span data-stu-id="6c5e8-105">The free/busy status of a block of time on a user's calendar is one of the following: out-of-office, busy, tentative, or free.</span></span>
  
## <a name="create-a-freebusy-provider"></a><span data-ttu-id="6c5e8-106">Crear un proveedor de disponibilidad</span><span class="sxs-lookup"><span data-stu-id="6c5e8-106">Create a free/busy provider</span></span>

<span data-ttu-id="6c5e8-107">Para proporcionar información de disponibilidad a los usuarios de correo, un proveedor de correo crea un proveedor de disponibilidad y lo registra con Outlook.</span><span class="sxs-lookup"><span data-stu-id="6c5e8-107">To provide free/busy information to mail users, a mail provider creates a free/busy provider and registers it with Outlook.</span></span> <span data-ttu-id="6c5e8-108">El proveedor de disponibilidad debe implementar las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="6c5e8-108">The free/busy provider must implement the following interfaces.</span></span> <span data-ttu-id="6c5e8-109">Tenga en cuenta que no se admiten varios miembros en estas interfaces y debe devolver los valores devueltos especificados.</span><span class="sxs-lookup"><span data-stu-id="6c5e8-109">Note that a number of members in these interfaces are not supported and must return the specified return values.</span></span> <span data-ttu-id="6c5e8-110">En particular, la API de disponibilidad no admite el acceso de escritura a la información de disponibilidad ni el acceso delegado a las cuentas.</span><span class="sxs-lookup"><span data-stu-id="6c5e8-110">In particular, the Free/Busy API does not support write access to free/busy information and delegate access to accounts.</span></span>
  
- <span data-ttu-id="6c5e8-111">[IFreeBusySupport: esta](ifreebusysupport.md) interfaz admite la especificación de interfaces que tienen acceso a datos de disponibilidad para usuarios especificados.</span><span class="sxs-lookup"><span data-stu-id="6c5e8-111">[IFreeBusySupport](ifreebusysupport.md) —This interface supports specification of interfaces that access free/busy data for specified users.</span></span> <span data-ttu-id="6c5e8-112">Usa [FBUser para](fbuser.md) identificar a un usuario.</span><span class="sxs-lookup"><span data-stu-id="6c5e8-112">It uses [FBUser](fbuser.md) to identify a user.</span></span> 
    
- <span data-ttu-id="6c5e8-113">[IFreeBusyData:](ifreebusydata.md) esta interfaz obtiene y establece un intervalo de tiempo para un usuario determinado y devuelve una interfaz para enumerar bloques de datos de disponibilidad dentro de este intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="6c5e8-113">[IFreeBusyData](ifreebusydata.md) —This interface gets and sets a time range for a given user and returns an interface for enumerating free/busy blocks of data within this time range.</span></span> <span data-ttu-id="6c5e8-114">Usa tiempo relativo para obtener y establecer este intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="6c5e8-114">It uses relative time to get and set this time range.</span></span> <span data-ttu-id="6c5e8-115">Para obtener más información, vea [Usar tiempo relativo para obtener acceso a los datos de disponibilidad.](how-to-use-relative-time-to-access-free-busy-data.md)</span><span class="sxs-lookup"><span data-stu-id="6c5e8-115">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
- <span data-ttu-id="6c5e8-116">[IEnumFBBlock: esta](ienumfbblock.md) interfaz admite el acceso y la enumeración de bloques de datos de disponibilidad de un usuario dentro de un intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="6c5e8-116">[IEnumFBBlock](ienumfbblock.md) —This interface supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="6c5e8-117">Una enumeración contiene bloques de disponibilidad que indican el estado de disponibilidad de períodos de tiempo en el calendario de un usuario, dentro de un intervalo de tiempo (especificado por [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)).</span><span class="sxs-lookup"><span data-stu-id="6c5e8-117">An enumeration contains free/busy blocks that indicate the free/busy status of periods of time on a user's calendar, within a time range (specified by [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)).</span></span> <span data-ttu-id="6c5e8-118">Elementos de un calendario, como citas y solicitudes de reunión, bloques de formulario en la enumeración.</span><span class="sxs-lookup"><span data-stu-id="6c5e8-118">Items on a calendar, such as appointments and meeting requests, form blocks in the enumeration.</span></span> <span data-ttu-id="6c5e8-119">Los elementos adyacentes entre sí en el calendario y que tienen el mismo estado de disponibilidad se combinan para formar un único bloque.</span><span class="sxs-lookup"><span data-stu-id="6c5e8-119">Items that are adjacent to one another on the calendar and have the same free/busy status are combined to form one single block.</span></span> <span data-ttu-id="6c5e8-120">Un período de tiempo libre en un calendario también forma un bloque.</span><span class="sxs-lookup"><span data-stu-id="6c5e8-120">A free period of time on a calendar also forms a block.</span></span> <span data-ttu-id="6c5e8-121">Por lo tanto, no hay dos bloques consecutivos en una enumeración que tengan el mismo estado de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="6c5e8-121">Therefore, no two consecutive blocks in an enumeration would have the same free/busy status.</span></span> <span data-ttu-id="6c5e8-122">Estos bloques no se superponen en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="6c5e8-122">These blocks do not overlap in time.</span></span> <span data-ttu-id="6c5e8-123">Cuando hay elementos superpuestos en un calendario, Outlook combina estos elementos para formar bloques de disponibilidad no superpuestos en la enumeración en función de este orden de prioridad: fuera de la oficina, ocupado, provisional.</span><span class="sxs-lookup"><span data-stu-id="6c5e8-123">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span> 
  
<span data-ttu-id="6c5e8-124">Para registrar el proveedor de disponibilidad con Outlook, el proveedor de correo debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6c5e8-124">To register the free/busy provider with Outlook, the mail provider should do the following:</span></span>
  
1. <span data-ttu-id="6c5e8-125">Registre el proveedor de disponibilidad con COM, proporcionando un CLSID que permite el acceso a la implementación del proveedor de **IFreeBusySupport**.</span><span class="sxs-lookup"><span data-stu-id="6c5e8-125">Register the free/busy provider with COM, providing a CLSID that allows access to the provider's implementation of **IFreeBusySupport**.</span></span> 
    
2. <span data-ttu-id="6c5e8-126">Para que Outlook sepa que existe el proveedor de disponibilidad, establece la siguiente clave (donde representa la versión de `<xx.x>` Outlook) en el Registro del sistema:</span><span class="sxs-lookup"><span data-stu-id="6c5e8-126">Let Outlook know that the free/busy provider exists by setting the following key (where `<xx.x>` represents the version of Outlook) in the system registry:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   <span data-ttu-id="6c5e8-127">Por ejemplo, si el proveedor de transporte es SMTP, para registrar el proveedor con Microsoft Outlook 2010, establezca la siguiente clave para los datos de la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="6c5e8-127">For example, if the transport provider is SMTP, to register the provider with Microsoft Outlook 2010, set the following key to the data in the following table:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |<span data-ttu-id="6c5e8-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="6c5e8-128">Name</span></span> |<span data-ttu-id="6c5e8-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c5e8-129">Type</span></span> |<span data-ttu-id="6c5e8-130">Valor</span><span class="sxs-lookup"><span data-stu-id="6c5e8-130">Value</span></span> |
   |:-----|:-----|:-----|
   |<span data-ttu-id="6c5e8-131">SMTP</span><span class="sxs-lookup"><span data-stu-id="6c5e8-131">SMTP</span></span>  |<span data-ttu-id="6c5e8-132">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="6c5e8-132">REG_SZ</span></span>  |<span data-ttu-id="6c5e8-133">{CLSID para la implementación respectiva de IFreeBusySupport}</span><span class="sxs-lookup"><span data-stu-id="6c5e8-133">{CLSID for respective implementation of IFreeBusySupport}</span></span>  |
   
   <span data-ttu-id="6c5e8-134">En este escenario, Outlook crea en co-crea la clase COM y la usa para recuperar información de disponibilidad de cualquier usuario de correo SMTP.</span><span class="sxs-lookup"><span data-stu-id="6c5e8-134">In this scenario, Outlook co-creates the COM class and uses it to retrieve free/busy information for any SMTP mail users.</span></span>
    
<span data-ttu-id="6c5e8-135">Para admitir una libreta de direcciones y un proveedor de transporte que usen un tipo de entrada de dirección distinto de SMTP, cambie el  *nombre* en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="6c5e8-135">To support an address book and transport provider that use an address entry type other than SMTP, change the  *Name* accordingly.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6c5e8-136">Durante la instalación, los proveedores de disponibilidad deben comprobar si ya existe una configuración del Registro para el mismo tipo de entrada de dirección.</span><span class="sxs-lookup"><span data-stu-id="6c5e8-136">During installation, free/busy providers should check whether a registry setting for the the same address entry type already exists.</span></span> <span data-ttu-id="6c5e8-137">Si es así, el proveedor de disponibilidad debe sobrescribir el proveedor actual para ese tipo de entrada de dirección y restaurarlo cuando se desinstala.</span><span class="sxs-lookup"><span data-stu-id="6c5e8-137">If it does, the free/busy provider should overwrite the current provider for that address entry type, and restore to that provider when it uninstalls.</span></span> <span data-ttu-id="6c5e8-138">Sin embargo, si un usuario ha instalado más de un proveedor de disponibilidad para el mismo tipo de entrada de dirección, el usuario debe desinstalar estos proveedores en el orden inverso como instalación (es decir, desinstalar siempre el proveedor más reciente).</span><span class="sxs-lookup"><span data-stu-id="6c5e8-138">However, if a user has installed more than one free/busy provider for the same address entry type, the user should uninstall these providers in the reverse order as installation (that is, always uninstall the latest provider).</span></span> <span data-ttu-id="6c5e8-139">De lo contrario, el Registro puede apuntar a un proveedor que ya se ha desinstalado.</span><span class="sxs-lookup"><span data-stu-id="6c5e8-139">Otherwise, the registry may point to a provider that has already been uninstalled.</span></span> 
  
## <a name="api-components"></a><span data-ttu-id="6c5e8-140">Componentes de api</span><span class="sxs-lookup"><span data-stu-id="6c5e8-140">API components</span></span>

<span data-ttu-id="6c5e8-141">La API de disponibilidad incluye los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="6c5e8-141">The Free/Busy API includes the following components:</span></span>
  
### <a name="definitions"></a><span data-ttu-id="6c5e8-142">Definiciones</span><span class="sxs-lookup"><span data-stu-id="6c5e8-142">Definitions</span></span>

- [<span data-ttu-id="6c5e8-143">Constantes (API de disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="6c5e8-143">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
    
### <a name="data-types"></a><span data-ttu-id="6c5e8-144">Tipos de datos</span><span class="sxs-lookup"><span data-stu-id="6c5e8-144">Data types</span></span>

- [<span data-ttu-id="6c5e8-145">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="6c5e8-145">FBBlock_1</span></span>](fbblock_1.md)
- [<span data-ttu-id="6c5e8-146">FBStatus</span><span class="sxs-lookup"><span data-stu-id="6c5e8-146">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="6c5e8-147">FBUser</span><span class="sxs-lookup"><span data-stu-id="6c5e8-147">FBUser</span></span>](fbuser.md)
    
### <a name="interfaces"></a><span data-ttu-id="6c5e8-148">Interfaces</span><span class="sxs-lookup"><span data-stu-id="6c5e8-148">Interfaces</span></span>

- [<span data-ttu-id="6c5e8-149">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="6c5e8-149">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="6c5e8-150">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="6c5e8-150">IFreeBusyData</span></span>](ifreebusydata.md)
- [<span data-ttu-id="6c5e8-151">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="6c5e8-151">IFreeBusySupport</span></span>](ifreebusysupport.md)
    

