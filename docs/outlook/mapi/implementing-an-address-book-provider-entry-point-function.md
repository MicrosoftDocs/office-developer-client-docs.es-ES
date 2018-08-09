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
ms.openlocfilehash: b60a80bc0ede0c2800f6cfd98a98f498b93a1d8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817678"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a><span data-ttu-id="56cab-103">Implementar una función de punto de entrada de proveedor de libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="56cab-103">Implementing an Address Book Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="56cab-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="56cab-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="56cab-105">Cuando una aplicación las llamadas del cliente [MAPILogonEx](mapilogonex.md) para comenzar una sesión con un perfil que contiene el proveedor de libreta de direcciones, MAPI carga el proveedor y todos los demás que forman parte del perfil.</span><span class="sxs-lookup"><span data-stu-id="56cab-105">When a client application calls [MAPILogonEx](mapilogonex.md) to begin a session using a profile that contains your address book provider, MAPI loads your provider and all others that are part of the profile.</span></span> <span data-ttu-id="56cab-106">MAPI aprende del nombre de la función de punto de entrada de su proveedor mirando en el perfil.</span><span class="sxs-lookup"><span data-stu-id="56cab-106">MAPI learns of the name of your provider's entry point function by looking in the profile.</span></span> <span data-ttu-id="56cab-107">Recuerde que esta función no es el mismo que una función de punto de entrada DLL; vea la documentación de **DllMain** en la documentación de Win32.</span><span class="sxs-lookup"><span data-stu-id="56cab-107">Remember that this function is not the same as a DLL entry point function; see the documentation for **DllMain** in the Win32 documentation.</span></span> 
  
<span data-ttu-id="56cab-108">Hay varias entradas, algunos de los cuales deben aparecer en el archivo de configuración mapisvc.inf, que se incluyen en la sección de perfil de cada proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="56cab-108">There are several entries, some of which must appear in the mapisvc.inf configuration file, that are included in the profile section of every address book provider.</span></span> <span data-ttu-id="56cab-109">En la siguiente tabla se enumera estas entradas de la sección de perfil y si el archivo mapisvc.inf debe incluirlos.</span><span class="sxs-lookup"><span data-stu-id="56cab-109">The following table lists these profile section entries and whether or not the mapisvc.inf file must include them.</span></span>
  
|<span data-ttu-id="56cab-110">**Entrada de la sección de perfil**</span><span class="sxs-lookup"><span data-stu-id="56cab-110">**Profile section entry**</span></span>|<span data-ttu-id="56cab-111">**requisito de MAPISVC.inf**</span><span class="sxs-lookup"><span data-stu-id="56cab-111">**mapisvc.inf requirement**</span></span>|
|:-----|:-----|
|<span data-ttu-id="56cab-112">PR_DISPLAY_NAME = _cadena_</span><span class="sxs-lookup"><span data-stu-id="56cab-112">PR_DISPLAY_NAME= _string_</span></span> <br/> |<span data-ttu-id="56cab-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="56cab-113">Optional</span></span>  <br/> |
|<span data-ttu-id="56cab-114">PR_PROVIDER_DISPLAY = _cadena_</span><span class="sxs-lookup"><span data-stu-id="56cab-114">PR_PROVIDER_DISPLAY= _string_</span></span> <br/> |<span data-ttu-id="56cab-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="56cab-115">Required</span></span>  <br/> |
|<span data-ttu-id="56cab-116">PR_PROVIDER_DLL_NAME = _nombre de DLL_</span><span class="sxs-lookup"><span data-stu-id="56cab-116">PR_PROVIDER_DLL_NAME= _DLL filename_</span></span> <br/> |<span data-ttu-id="56cab-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="56cab-117">Required</span></span>  <br/> |
|<span data-ttu-id="56cab-118">PR_RESOURCE_TYPE = _largo_</span><span class="sxs-lookup"><span data-stu-id="56cab-118">PR_RESOURCE_TYPE= _long_</span></span> <br/> |<span data-ttu-id="56cab-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="56cab-119">Required</span></span>  <br/> |
|<span data-ttu-id="56cab-120">PR_RESOURCE_FLAGS = _máscara de bits_</span><span class="sxs-lookup"><span data-stu-id="56cab-120">PR_RESOURCE_FLAGS= _bitmask_</span></span> <br/> |<span data-ttu-id="56cab-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="56cab-121">Optional</span></span>  <br/> |
   
<span data-ttu-id="56cab-122">Su proveedor de libreta de direcciones puede colocar esta información en un perfil directamente mediante una llamada al método [IMAPIProp::SetProps](imapiprop-setprops.md) de la sección de su perfil o indirectamente mediante la modificación de MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="56cab-122">Your address book provider can place this information into a profile directly by calling its profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method or indirectly by modifying MAPISVC.INF.</span></span> <span data-ttu-id="56cab-123">Los perfiles se crean utilizando la información pertinente en MAPISVC. INF para los proveedores de servicio seleccionada o servicios de mensaje.</span><span class="sxs-lookup"><span data-stu-id="56cab-123">Profiles are built using the relevant information in MAPISVC.INF for the selected service providers or message services.</span></span> <span data-ttu-id="56cab-124">Para obtener más información acerca de la organización y el contenido de MAPISVC. INF, vea el [Archivo de formato de MapiSvc.inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="56cab-124">For more information about the organization and contents of MAPISVC.INF, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
  
<span data-ttu-id="56cab-125">El nombre de la función de punto de entrada DLL de su proveedor libreta de direcciones debe ser [ABProviderInit](abproviderinit.md) y debe cumplir con el prototipo de **ABProviderInit** .</span><span class="sxs-lookup"><span data-stu-id="56cab-125">The name of your address book provider's DLL entry point function must be [ABProviderInit](abproviderinit.md) and it must conform to the **ABProviderInit** prototype.</span></span> <span data-ttu-id="56cab-126">Realizar las siguientes tareas en función de punto de entrada DLL de su proveedor:</span><span class="sxs-lookup"><span data-stu-id="56cab-126">Perform the following tasks in your provider's DLL entry point function:</span></span> 
  
- <span data-ttu-id="56cab-127">Comprobar la versión de la interfaz de proveedor de servicios (SPI) para asegurarse de que MAPI está usando una versión que sea compatible con la versión que está usando el proveedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="56cab-127">Check the version of the service provider interface (SPI) to make sure MAPI is using a version that is compatible with the version that your address book provider is using.</span></span>
    
- <span data-ttu-id="56cab-128">Crear una instancia de un objeto de proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="56cab-128">Instantiate an address book provider object.</span></span>
    
<span data-ttu-id="56cab-129">No llame a **MAPIInitialize** o **MAPIUninitialize** en esta función.</span><span class="sxs-lookup"><span data-stu-id="56cab-129">Do not call either **MAPIInitialize** or **MAPIUninitialize** in this function.</span></span> 
  
<span data-ttu-id="56cab-130">La función de punto de entrada DLL crea una instancia de un objeto de proveedor y devuelve a MAPI un puntero a ese objeto.</span><span class="sxs-lookup"><span data-stu-id="56cab-130">The DLL entry point function instantiates a provider object and returns to MAPI a pointer to that object.</span></span> 
  

