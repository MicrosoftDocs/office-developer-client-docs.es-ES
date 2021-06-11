---
title: Implementación del inicio de sesión y cierre de sesión del proveedor de libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4a1fb5d-ae23-445b-a6f0-ef430b03fc9a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8d33bccdd01075d692e5a887082ba51ee23bb083
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438739"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a><span data-ttu-id="29294-103">Implementación del inicio de sesión y cierre de sesión del proveedor de libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="29294-103">Implementing Address Book Provider Logon and Logoff</span></span>

<span data-ttu-id="29294-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29294-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29294-105">Los proveedores de libreta de direcciones admiten el inicio de sesión y el cierre de sesión mediante la implementación de los métodos de la [interfaz IABProvider : IUnknown.](iabprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="29294-105">Address book providers support session logon and logoff by implementing the methods of the [IABProvider : IUnknown](iabprovideriunknown.md) interface.</span></span> <span data-ttu-id="29294-106">La interfaz \*\* IABProvider \*\* hereda directamente de **IUnknown** y agrega solo otros dos métodos: **Logon** y **Shutdown**.</span><span class="sxs-lookup"><span data-stu-id="29294-106">The \*\* IABProvider \*\* interface inherits directly from **IUnknown** and adds only two other methods: **Logon** and **Shutdown**.</span></span> 
  
## <a name="logoff"></a><span data-ttu-id="29294-107">Cierre de sesión</span><span class="sxs-lookup"><span data-stu-id="29294-107">Logoff</span></span>

<span data-ttu-id="29294-108">MAPI llamará al método [IABProvider::Logon](iabprovider-logon.md) del proveedor al principio de cada sesión y siempre que el proveedor se agrega al perfil actual y el cliente admite la reconfiguración dinámica.</span><span class="sxs-lookup"><span data-stu-id="29294-108">MAPI will call your provider's [IABProvider::Logon](iabprovider-logon.md) method at the beginning of every session and whenever your provider is added to the current profile and the client supports dynamic reconfiguration.</span></span> <span data-ttu-id="29294-109">Cuando MAPI llama al **método IABProvider::Logon,** el proveedor de la libreta de direcciones inicia el proceso de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="29294-109">When MAPI calls the **IABProvider::Logon** method, your address book provider begins its logon process.</span></span> 
  
<span data-ttu-id="29294-110">**Para implementar IABProvider::Log**</span><span class="sxs-lookup"><span data-stu-id="29294-110">**To implement IABProvider::Log**</span></span>
  
1. <span data-ttu-id="29294-111">Inicializa todos los punteros de parámetro de salida pasados por MAPI.</span><span class="sxs-lookup"><span data-stu-id="29294-111">Initialize all of the output parameter pointers passed in by MAPI.</span></span> 
    
2. <span data-ttu-id="29294-112">Llame al método **IUnknown::AddRef** del objeto de soporte técnico para incrementar su recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="29294-112">Call the support object's **IUnknown::AddRef** method to increment its reference count.</span></span> 
    
3. <span data-ttu-id="29294-113">Llame al método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) del objeto de soporte técnico para abrir la sección del perfil que contiene información de configuración sobre el proveedor.</span><span class="sxs-lookup"><span data-stu-id="29294-113">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to open the section of the profile that contains configuration information about your provider.</span></span> <span data-ttu-id="29294-114">Pase NULL para el  _parámetro lpUID_ y la marca MAPI_MODIFY si desea realizar cambios.</span><span class="sxs-lookup"><span data-stu-id="29294-114">Pass NULL for the  _lpUID_ parameter and the MAPI_MODIFY flag if you intend to make changes.</span></span> 
    
4. <span data-ttu-id="29294-115">Llame al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la sección de perfil para recuperar las propiedades que el proveedor necesita para el inicio de sesión, como el nombre del archivo de datos o la tabla de base de datos.</span><span class="sxs-lookup"><span data-stu-id="29294-115">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the properties that your provider needs for logon, such as the name of the data file or database table.</span></span> 
    
5. <span data-ttu-id="29294-116">Compruebe que todas las propiedades están disponibles y son válidas.</span><span class="sxs-lookup"><span data-stu-id="29294-116">Check that the properties are all available and valid.</span></span> <span data-ttu-id="29294-117">Si es necesario y está permitido, muestre un cuadro de diálogo para solicitar al usuario que realice correcciones o adiciones a información no válida o que falte y llame al método [IMAPIProp::SetProps](imapiprop-setprops.md) de la sección de perfil para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="29294-117">If necessary and allowed, display a dialog box to prompt the user to make corrections or additions to invalid or missing information and call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to save any changes.</span></span> <span data-ttu-id="29294-118">Algunas de las propiedades comunes que deben estar disponibles incluyen:</span><span class="sxs-lookup"><span data-stu-id="29294-118">Some of the common properties that should be available include:</span></span> 
    
   <span data-ttu-id="29294-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="29294-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
   <span data-ttu-id="29294-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="29294-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
   <span data-ttu-id="29294-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="29294-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
   <span data-ttu-id="29294-122">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="29294-122">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="29294-123">No establezca **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) **o PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="29294-123">Do not set **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) or **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)).</span></span> <span data-ttu-id="29294-124">En el momento del inicio de sesión, estas propiedades son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="29294-124">At logon time, these properties are read-only.</span></span> 
  
6. <span data-ttu-id="29294-125">Si una o varias propiedades de configuración no están disponibles, se producirá un error y se devolverá el MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="29294-125">If one or more configuration properties are unavailable, fail and return the value MAPI_E_UNCONFIGURED.</span></span>
    
7. <span data-ttu-id="29294-126">Llame [a IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) para registrar [un MAPIUID](mapiuid.md).</span><span class="sxs-lookup"><span data-stu-id="29294-126">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) to register a [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="29294-127">El proveedor puede crear un **MAPIUID** mediante:</span><span class="sxs-lookup"><span data-stu-id="29294-127">Your provider can create a **MAPIUID** by:</span></span> 
    
   - <span data-ttu-id="29294-128">Llamar al [método IMAPISupport::NewUID.](imapisupport-newuid.md)</span><span class="sxs-lookup"><span data-stu-id="29294-128">Calling the [IMAPISupport::NewUID](imapisupport-newuid.md) method.</span></span> 
    
   - <span data-ttu-id="29294-129">Llamar a la UUIDGEN.EXE para definir un GUID que el proveedor usa para incluir en uno de sus archivos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="29294-129">Calling the UUIDGEN.EXE tool to define a GUID that your provider uses to include in one of its header files.</span></span>
    
8. <span data-ttu-id="29294-130">Si lo desea, guarde un **MAPIUID** recién creado en el perfil actual llamando al método \*\* IMAPIProp::SetProps \*\* de la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="29294-130">If desired, save a newly created **MAPIUID** in the current profile by calling the profile section's \*\* IMAPIProp::SetProps \*\* method.</span></span> 
    
9. <span data-ttu-id="29294-131">Libere la sección de perfil llamando a su **método IUnknown::Release.**</span><span class="sxs-lookup"><span data-stu-id="29294-131">Release the profile section by calling its **IUnknown::Release** method.</span></span> 
    
10. <span data-ttu-id="29294-132">Cree una instancia de un nuevo objeto de inicio de sesión y establezca el contenido del parámetro  _lppABLogon_ en la dirección de este nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="29294-132">Instantiate a new logon object and set the contents of the  _lppABLogon_ parameter to the address of this new object.</span></span> 
    
<span data-ttu-id="29294-133">Dado que es posible que MAPI llame al método \*\* Logon \*\* varias veces durante una sesión, es aconsejable admitir esta posibilidad en la implementación al poder crear varios objetos de inicio de sesión y realizar un seguimiento de cada objeto que se crea.</span><span class="sxs-lookup"><span data-stu-id="29294-133">Because it is possible for MAPI to call your \*\* Logon \*\* method several times during a session, it is wise to support this possibility in your implementation by being able to create multiple logon objects and keep track of each object that is created.</span></span> <span data-ttu-id="29294-134">Admitir varias llamadas **de inicio** de sesión permite al usuario de una aplicación cliente, por ejemplo, iniciar sesión en una sesión con identidades diferentes o usar destinos de entrega diferentes.</span><span class="sxs-lookup"><span data-stu-id="29294-134">Supporting multiple **Logon** calls enables a user of a client application, for example, to log on to a session with different identities or use different delivery destinations.</span></span> 
  
<span data-ttu-id="29294-135">**Se** llama al apagado cuando finaliza la sesión.</span><span class="sxs-lookup"><span data-stu-id="29294-135">**Shutdown** is called when the session is ending.</span></span> <span data-ttu-id="29294-136">MAPI llama al [método IABProvider::Shutdown](iabprovider-shutdown.md) como una de las últimas tareas relacionadas con el cierre de una sesión.</span><span class="sxs-lookup"><span data-stu-id="29294-136">MAPI calls your [IABProvider::Shutdown](iabprovider-shutdown.md) method as one of the last tasks involved in shutting down a session.</span></span> <span data-ttu-id="29294-137">MAPI ha liberado todos los objetos de inicio de sesión del proveedor y, cuando el proveedor recibe esta llamada, puede suponer que esta es la última llamada que recibirá.</span><span class="sxs-lookup"><span data-stu-id="29294-137">MAPI has released all of your provider's logon objects and, when your provider receives this call, it can assume that this is the last call it will receive.</span></span> <span data-ttu-id="29294-138">En la implementación de **IABProvider::Shutdown**, realice cualquier limpieza final que crea necesaria.</span><span class="sxs-lookup"><span data-stu-id="29294-138">In your implementation of **IABProvider::Shutdown**, perform any final cleanup that you feel is necessary.</span></span> <span data-ttu-id="29294-139">Por ejemplo, el proveedor puede llamar a **MAPIDeinitIdle** si ha llamado a **MAPIInitIdle** para usar el motor inactivo durante la sesión o el método **IUnknown::Release** de los objetos que aún no se han liberado.</span><span class="sxs-lookup"><span data-stu-id="29294-139">For example, your provider might call **MAPIDeinitIdle** if it has called **MAPIInitIdle** to use the idle engine during the session or the **IUnknown::Release** method of any objects that have yet to be released.</span></span> 
  
<span data-ttu-id="29294-140">Si el proveedor no tiene ninguna limpieza final, su implementación puede estar hecha de una sola línea de código:</span><span class="sxs-lookup"><span data-stu-id="29294-140">If your provider has no final cleanup, its implementation can be made up of a single line of code:</span></span> 
  
```cpp
return S_OK;

```


