---
title: Implementar una función de punto de entrada de proveedor de libreta de direcciones
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 00b3b30101ee1efb984cf45afb35b0b085d545ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409716"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a><span data-ttu-id="335f4-103">Implementar una función de punto de entrada de proveedor de libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="335f4-103">Implementing an Address Book Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="335f4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="335f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="335f4-105">Cuando una aplicación de cliente llama a [MAPILogonEx](mapilogonex.md) para iniciar una sesión con un perfil que contiene el proveedor de la libreta de direcciones, MAPI carga el proveedor y el resto de los elementos que forman parte del perfil.</span><span class="sxs-lookup"><span data-stu-id="335f4-105">When a client application calls [MAPILogonEx](mapilogonex.md) to begin a session using a profile that contains your address book provider, MAPI loads your provider and all others that are part of the profile.</span></span> <span data-ttu-id="335f4-106">MAPI aprende el nombre de la función de punto de entrada de su proveedor al buscar en el perfil.</span><span class="sxs-lookup"><span data-stu-id="335f4-106">MAPI learns of the name of your provider's entry point function by looking in the profile.</span></span> <span data-ttu-id="335f4-107">Recuerde que esta función no es la misma que una función de punto de entrada de DLL; Vea la documentación de **DllMain** en la documentación de Win32.</span><span class="sxs-lookup"><span data-stu-id="335f4-107">Remember that this function is not the same as a DLL entry point function; see the documentation for **DllMain** in the Win32 documentation.</span></span> 
  
<span data-ttu-id="335f4-108">Hay varias entradas, algunas de las cuales deben aparecer en el archivo de configuración MAPISVC. inf, que se incluyen en la sección de Perfil de todos los proveedores de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="335f4-108">There are several entries, some of which must appear in the mapisvc.inf configuration file, that are included in the profile section of every address book provider.</span></span> <span data-ttu-id="335f4-109">En la siguiente tabla se enumeran estas entradas de sección de perfil y si el archivo MAPISVC. inf debe incluirlas o no.</span><span class="sxs-lookup"><span data-stu-id="335f4-109">The following table lists these profile section entries and whether or not the mapisvc.inf file must include them.</span></span>
  
|<span data-ttu-id="335f4-110">**Entrada de sección de perfil**</span><span class="sxs-lookup"><span data-stu-id="335f4-110">**Profile section entry**</span></span>|<span data-ttu-id="335f4-111">**requisito de MAPISVC. inf**</span><span class="sxs-lookup"><span data-stu-id="335f4-111">**mapisvc.inf requirement**</span></span>|
|:-----|:-----|
|<span data-ttu-id="335f4-112">PR_DISPLAY_NAME = _String_</span><span class="sxs-lookup"><span data-stu-id="335f4-112">PR_DISPLAY_NAME= _string_</span></span> <br/> |<span data-ttu-id="335f4-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="335f4-113">Optional</span></span>  <br/> |
|<span data-ttu-id="335f4-114">PR_PROVIDER_DISPLAY = _String_</span><span class="sxs-lookup"><span data-stu-id="335f4-114">PR_PROVIDER_DISPLAY= _string_</span></span> <br/> |<span data-ttu-id="335f4-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="335f4-115">Required</span></span>  <br/> |
|<span data-ttu-id="335f4-116">PR_PROVIDER_DLL_NAME = _nombre_ de archivo dll</span><span class="sxs-lookup"><span data-stu-id="335f4-116">PR_PROVIDER_DLL_NAME= _DLL filename_</span></span> <br/> |<span data-ttu-id="335f4-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="335f4-117">Required</span></span>  <br/> |
|<span data-ttu-id="335f4-118">PR_RESOURCE_TYPE = _Long_</span><span class="sxs-lookup"><span data-stu-id="335f4-118">PR_RESOURCE_TYPE= _long_</span></span> <br/> |<span data-ttu-id="335f4-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="335f4-119">Required</span></span>  <br/> |
|<span data-ttu-id="335f4-120">PR_RESOURCE_FLAGS = _máscara_ de</span><span class="sxs-lookup"><span data-stu-id="335f4-120">PR_RESOURCE_FLAGS= _bitmask_</span></span> <br/> |<span data-ttu-id="335f4-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="335f4-121">Optional</span></span>  <br/> |
   
<span data-ttu-id="335f4-122">El proveedor de la libreta de direcciones puede incluir esta información en un perfil directamente llamando al método [IMAPIProp:: SetProps](imapiprop-setprops.md) de la sección del perfil o indirectamente modificando MAPISVC. inf.</span><span class="sxs-lookup"><span data-stu-id="335f4-122">Your address book provider can place this information into a profile directly by calling its profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method or indirectly by modifying MAPISVC.INF.</span></span> <span data-ttu-id="335f4-123">Los perfiles se crean con la información relevante en MAPISVC. INF para los proveedores de servicios o los servicios de mensajes seleccionados.</span><span class="sxs-lookup"><span data-stu-id="335f4-123">Profiles are built using the relevant information in MAPISVC.INF for the selected service providers or message services.</span></span> <span data-ttu-id="335f4-124">Para obtener más información acerca de la organización y el contenido de MAPISVC. INF, consulte [formato de archivo de MapiSvc. inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="335f4-124">For more information about the organization and contents of MAPISVC.INF, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
  
<span data-ttu-id="335f4-125">El nombre de la función de punto de entrada de DLL del proveedor de la libreta de direcciones debe ser [ABProviderInit](abproviderinit.md) y debe cumplir con el prototipo **ABProviderInit** .</span><span class="sxs-lookup"><span data-stu-id="335f4-125">The name of your address book provider's DLL entry point function must be [ABProviderInit](abproviderinit.md) and it must conform to the **ABProviderInit** prototype.</span></span> <span data-ttu-id="335f4-126">Realice las siguientes tareas en la función de punto de entrada de DLL del proveedor:</span><span class="sxs-lookup"><span data-stu-id="335f4-126">Perform the following tasks in your provider's DLL entry point function:</span></span> 
  
- <span data-ttu-id="335f4-127">Compruebe la versión de la interfaz del proveedor de servicios (SPI) para asegurarse de que MAPI está usando una versión compatible con la versión que el proveedor de la libreta de direcciones usa.</span><span class="sxs-lookup"><span data-stu-id="335f4-127">Check the version of the service provider interface (SPI) to make sure MAPI is using a version that is compatible with the version that your address book provider is using.</span></span>
    
- <span data-ttu-id="335f4-128">Crear una instancia de un objeto de proveedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="335f4-128">Instantiate an address book provider object.</span></span>
    
<span data-ttu-id="335f4-129">No llame a **MAPIInitialize** o **MAPIUninitialize** en esta función.</span><span class="sxs-lookup"><span data-stu-id="335f4-129">Do not call either **MAPIInitialize** or **MAPIUninitialize** in this function.</span></span> 
  
<span data-ttu-id="335f4-130">La función de punto de entrada de DLL crea una instancia de un objeto de proveedor y devuelve a MAPI un puntero a ese objeto.</span><span class="sxs-lookup"><span data-stu-id="335f4-130">The DLL entry point function instantiates a provider object and returns to MAPI a pointer to that object.</span></span> 
  

