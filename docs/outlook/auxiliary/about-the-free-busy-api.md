---
title: Acerca de la API de libre/ocupado
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: La API de la información de disponibilidad permite a los proveedores de correo proporcionar información de estado de disponibilidad para las cuentas de usuario especificado dentro de un intervalo de tiempo especificado.
ms.openlocfilehash: 8b1559173297fbde9930b6f8f7fbc74f176273da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816054"
---
# <a name="about-the-freebusy-api"></a><span data-ttu-id="f3b23-103">Acerca de la API de libre/ocupado</span><span class="sxs-lookup"><span data-stu-id="f3b23-103">About the Free/Busy API</span></span>

<span data-ttu-id="f3b23-104">La API de la información de disponibilidad permite a los proveedores de correo proporcionar información de estado de disponibilidad para las cuentas de usuario especificado dentro de un intervalo de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="f3b23-104">The Free/Busy API allows mail providers to provide free/busy status information for specified user accounts within a specified time range.</span></span> <span data-ttu-id="f3b23-105">El estado de disponibilidad de un bloque de tiempo en el calendario de un usuario es uno de los siguientes: fuera de la oficina, ocupado, provisional o libre.</span><span class="sxs-lookup"><span data-stu-id="f3b23-105">The free/busy status of a block of time on a user's calendar is one of the following: out-of-office, busy, tentative, or free.</span></span>
  
## <a name="create-a-freebusy-provider"></a><span data-ttu-id="f3b23-106">Crear un proveedor de libre/ocupado</span><span class="sxs-lookup"><span data-stu-id="f3b23-106">Create a free/busy provider</span></span>

<span data-ttu-id="f3b23-107">Para proporcionar información de disponibilidad a los usuarios de correo, un proveedor de correo crea un proveedor de libre/ocupado y registra con Outlook.</span><span class="sxs-lookup"><span data-stu-id="f3b23-107">To provide free/busy information to mail users, a mail provider creates a free/busy provider and registers it with Outlook.</span></span> <span data-ttu-id="f3b23-108">El proveedor de disponibilidad debe implementar las interfaces siguientes.</span><span class="sxs-lookup"><span data-stu-id="f3b23-108">The free/busy provider must implement the following interfaces.</span></span> <span data-ttu-id="f3b23-109">Tenga en cuenta que un número de miembros en estas interfaces no es compatibles y debe devolver que valores devueltos especificado.</span><span class="sxs-lookup"><span data-stu-id="f3b23-109">Note that a number of members in these interfaces are not supported and must return the specified return values.</span></span> <span data-ttu-id="f3b23-110">En particular, la API de la información de disponibilidad no es compatible con acceso de escritura para la información de disponibilidad y acceso a las cuentas de delegado.</span><span class="sxs-lookup"><span data-stu-id="f3b23-110">In particular, the Free/Busy API does not support write access to free/busy information and delegate access to accounts.</span></span>
  
- <span data-ttu-id="f3b23-111">[IFreeBusySupport](ifreebusysupport.md) : esta interfaz admite la especificación de las interfaces que tienen acceso a datos de disponibilidad para los usuarios especificados.</span><span class="sxs-lookup"><span data-stu-id="f3b23-111">[IFreeBusySupport](ifreebusysupport.md) —This interface supports specification of interfaces that access free/busy data for specified users.</span></span> <span data-ttu-id="f3b23-112">Se utiliza [FBUser](fbuser.md) para identificar a un usuario.</span><span class="sxs-lookup"><span data-stu-id="f3b23-112">It uses [FBUser](fbuser.md) to identify a user.</span></span> 
    
- <span data-ttu-id="f3b23-113">[IFreeBusyData](ifreebusydata.md) : esta interfaz obtiene y establece un intervalo de tiempo para un usuario determinado y devuelve una interfaz para enumerar los bloques de libre/ocupado de datos dentro de este intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="f3b23-113">[IFreeBusyData](ifreebusydata.md) —This interface gets and sets a time range for a given user and returns an interface for enumerating free/busy blocks of data within this time range.</span></span> <span data-ttu-id="f3b23-114">Tiempo relativo usa para obtener y establecer este intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="f3b23-114">It uses relative time to get and set this time range.</span></span> <span data-ttu-id="f3b23-115">Para obtener más información, vea [usar la hora relativa para tener acceso a datos de disponibilidad](how-to-use-relative-time-to-access-free-busy-data.md).</span><span class="sxs-lookup"><span data-stu-id="f3b23-115">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
- <span data-ttu-id="f3b23-116">[IEnumFBBlock](ienumfbblock.md) : esta interfaz admite el acceso y enumerar los bloques de disponibilidad de datos para un usuario dentro de un intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="f3b23-116">[IEnumFBBlock](ienumfbblock.md) —This interface supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="f3b23-117">Una enumeración contiene bloques de libre/ocupado que indican el estado de disponibilidad de los períodos de tiempo en el calendario de un usuario, dentro de un intervalo de tiempo (especificado por [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)).</span><span class="sxs-lookup"><span data-stu-id="f3b23-117">An enumeration contains free/busy blocks that indicate the free/busy status of periods of time on a user's calendar, within a time range (specified by [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)).</span></span> <span data-ttu-id="f3b23-118">Bloques de formulario de elementos en un calendario, como las citas y las convocatorias de reunión, en la enumeración.</span><span class="sxs-lookup"><span data-stu-id="f3b23-118">Items on a calendar, such as appointments and meeting requests, form blocks in the enumeration.</span></span> <span data-ttu-id="f3b23-119">Se combinan los elementos que están adyacentes en el calendario y tienen el mismo estado libre/ocupado para formulario un bloque único.</span><span class="sxs-lookup"><span data-stu-id="f3b23-119">Items that are adjacent to one another on the calendar and have the same free/busy status are combined to form one single block.</span></span> <span data-ttu-id="f3b23-120">Un período de tiempo en un calendario libre también de formularios de un bloque.</span><span class="sxs-lookup"><span data-stu-id="f3b23-120">A free period of time on a calendar also forms a block.</span></span> <span data-ttu-id="f3b23-121">Por lo tanto, no hay dos bloques consecutivos en una enumeración tendría el mismo estado libre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="f3b23-121">Therefore, no two consecutive blocks in an enumeration would have the same free/busy status.</span></span> <span data-ttu-id="f3b23-122">Estos bloques no se superponen en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="f3b23-122">These blocks do not overlap in time.</span></span> <span data-ttu-id="f3b23-123">Cuando hay elementos superpuestos en un calendario, Outlook combina estos elementos para formar bloques de libre/ocupada no se superponen en la enumeración basándose en este orden de prioridad: fuera de la oficina, ocupado, provisional.</span><span class="sxs-lookup"><span data-stu-id="f3b23-123">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span> 
  
<span data-ttu-id="f3b23-124">Para registrar el proveedor de libre/ocupado con Outlook, el proveedor de correo debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f3b23-124">To register the free/busy provider with Outlook, the mail provider should do the following:</span></span>
  
1. <span data-ttu-id="f3b23-125">Registrar el proveedor de libre/ocupado con COM, proporcionar un CLSID que permite el acceso a la implementación del proveedor de **IFreeBusySupport**.</span><span class="sxs-lookup"><span data-stu-id="f3b23-125">Register the free/busy provider with COM, providing a CLSID that allows access to the provider's implementation of **IFreeBusySupport**.</span></span> 
    
2. <span data-ttu-id="f3b23-126">Decirles a Outlook que existe el proveedor de la disponibilidad mediante la configuración de la clave siguiente (donde `<xx.x>` representa la versión de Outlook) en el registro del sistema:</span><span class="sxs-lookup"><span data-stu-id="f3b23-126">Let Outlook know that the free/busy provider exists by setting the following key (where `<xx.x>` represents the version of Outlook) in the system registry:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   <span data-ttu-id="f3b23-127">Por ejemplo, si el proveedor de transporte es SMTP, para registrar el proveedor con Microsoft Outlook 2010, establezca la siguiente clave a los datos en la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="f3b23-127">For example, if the transport provider is SMTP, to register the provider with Microsoft Outlook 2010, set the following key to the data in the following table:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |<span data-ttu-id="f3b23-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="f3b23-128">Name</span></span> |<span data-ttu-id="f3b23-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="f3b23-129">Type</span></span> |<span data-ttu-id="f3b23-130">Valor</span><span class="sxs-lookup"><span data-stu-id="f3b23-130">Value</span></span> |
   |:-----|:-----|:-----|
   |<span data-ttu-id="f3b23-131">SMTP</span><span class="sxs-lookup"><span data-stu-id="f3b23-131">SMTP</span></span>  |<span data-ttu-id="f3b23-132">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f3b23-132">REG_SZ</span></span>  |<span data-ttu-id="f3b23-133">{CLSID para implementación respectivo de IFreeBusySupport}</span><span class="sxs-lookup"><span data-stu-id="f3b23-133">{CLSID for respective implementation of IFreeBusySupport}</span></span>  |
   
   <span data-ttu-id="f3b23-134">En este escenario, Outlook co-autoría crea la clase COM y lo usa para recuperar información de disponibilidad de los usuarios de correo SMTP.</span><span class="sxs-lookup"><span data-stu-id="f3b23-134">In this scenario, Outlook co-creates the COM class and uses it to retrieve free/busy information for any SMTP mail users.</span></span>
    
<span data-ttu-id="f3b23-135">Para admitir un proveedor de libreta de direcciones y transporte de dirección que use un tipo de entrada de dirección que no sean SMTP, cambiar el *nombre* en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="f3b23-135">To support an address book and transport provider that use an address entry type other than SMTP, change the  *Name* accordingly.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f3b23-136">Durante la instalación, deben comprobar proveedores de libre/ocupado si una configuración del registro para el mismo tipo de entrada de dirección ya existe.</span><span class="sxs-lookup"><span data-stu-id="f3b23-136">During installation, free/busy providers should check whether a registry setting for the the same address entry type already exists.</span></span> <span data-ttu-id="f3b23-137">Si lo hace, el proveedor de libre/ocupado debe sobrescribir el proveedor actual para ese tipo de entrada de dirección y restaurar a ese proveedor cuando desinstala.</span><span class="sxs-lookup"><span data-stu-id="f3b23-137">If it does, the free/busy provider should overwrite the current provider for that address entry type, and restore to that provider when it uninstalls.</span></span> <span data-ttu-id="f3b23-138">Sin embargo, si un usuario ha instalado más de un proveedor de libre/ocupado para el mismo tipo de entrada de dirección, el usuario debe desinstalar estos proveedores en el orden inverso como instalación (es decir, desinstale el proveedor más reciente siempre).</span><span class="sxs-lookup"><span data-stu-id="f3b23-138">However, if a user has installed more than one free/busy provider for the same address entry type, the user should uninstall these providers in the reverse order as installation (that is, always uninstall the latest provider).</span></span> <span data-ttu-id="f3b23-139">De lo contrario, el registro puede apuntar a un proveedor que ya se ha desinstalado.</span><span class="sxs-lookup"><span data-stu-id="f3b23-139">Otherwise, the registry may point to a provider that has already been uninstalled.</span></span> 
  
## <a name="api-components"></a><span data-ttu-id="f3b23-140">Componentes de la API</span><span class="sxs-lookup"><span data-stu-id="f3b23-140">API components</span></span>

<span data-ttu-id="f3b23-141">La API de libre/ocupado incluye los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="f3b23-141">The Free/Busy API includes the following components:</span></span>
  
### <a name="definitions"></a><span data-ttu-id="f3b23-142">Definiciones</span><span class="sxs-lookup"><span data-stu-id="f3b23-142">Definitions</span></span>

- [<span data-ttu-id="f3b23-143">Constantes (API de libre/ocupado)</span><span class="sxs-lookup"><span data-stu-id="f3b23-143">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
    
### <a name="data-types"></a><span data-ttu-id="f3b23-144">Tipos de datos</span><span class="sxs-lookup"><span data-stu-id="f3b23-144">Data types</span></span>

- [<span data-ttu-id="f3b23-145">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="f3b23-145">FBBlock_1</span></span>](fbblock_1.md)
- [<span data-ttu-id="f3b23-146">FBStatus</span><span class="sxs-lookup"><span data-stu-id="f3b23-146">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="f3b23-147">FBUser</span><span class="sxs-lookup"><span data-stu-id="f3b23-147">FBUser</span></span>](fbuser.md)
    
### <a name="interfaces"></a><span data-ttu-id="f3b23-148">Interfaces</span><span class="sxs-lookup"><span data-stu-id="f3b23-148">Interfaces</span></span>

- [<span data-ttu-id="f3b23-149">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="f3b23-149">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="f3b23-150">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="f3b23-150">IFreeBusyData</span></span>](ifreebusydata.md)
- [<span data-ttu-id="f3b23-151">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="f3b23-151">IFreeBusySupport</span></span>](ifreebusysupport.md)
    

