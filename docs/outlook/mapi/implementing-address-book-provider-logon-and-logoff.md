---
title: Implementar el inicio y cierre de sesión de proveedor de libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4a1fb5d-ae23-445b-a6f0-ef430b03fc9a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f26e7b7ec607c9714012870d5367a0e775c62f34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572105"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a><span data-ttu-id="d11b0-103">Implementar el inicio y cierre de sesión de proveedor de libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="d11b0-103">Implementing Address Book Provider Logon and Logoff</span></span>

<span data-ttu-id="d11b0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d11b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d11b0-105">Los proveedores de la libreta de direcciones compatible con inicio de sesión y cierre de sesión mediante la implementación de los métodos de la [IABProvider: IUnknown](iabprovideriunknown.md) interfaz.</span><span class="sxs-lookup"><span data-stu-id="d11b0-105">Address book providers support session logon and logoff by implementing the methods of the [IABProvider : IUnknown](iabprovideriunknown.md) interface.</span></span> <span data-ttu-id="d11b0-106">El ** IABProvider ** interfaz hereda directamente de **IUnknown** y agrega otros sólo dos métodos: **Inicio de sesión** y **apagado**.</span><span class="sxs-lookup"><span data-stu-id="d11b0-106">The ** IABProvider ** interface inherits directly from **IUnknown** and adds only two other methods: **Logon** and **Shutdown**.</span></span> 
  
## <a name="logoff"></a><span data-ttu-id="d11b0-107">Cierre de sesión</span><span class="sxs-lookup"><span data-stu-id="d11b0-107">Logoff</span></span>

<span data-ttu-id="d11b0-108">MAPI llamará al método de [IABProvider::Logon](iabprovider-logon.md) de su proveedor al principio de cada sesión y siempre que el proveedor se agrega al perfil actual y el cliente permite la reconfiguración dinámica.</span><span class="sxs-lookup"><span data-stu-id="d11b0-108">MAPI will call your provider's [IABProvider::Logon](iabprovider-logon.md) method at the beginning of every session and whenever your provider is added to the current profile and the client supports dynamic reconfiguration.</span></span> <span data-ttu-id="d11b0-109">Cuando el método **IABProvider::Logon** llama a MAPI, su proveedor de libreta de direcciones comienza su proceso de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="d11b0-109">When MAPI calls the **IABProvider::Logon** method, your address book provider begins its logon process.</span></span> 
  
<span data-ttu-id="d11b0-110">**Para implementar IABProvider::Log**</span><span class="sxs-lookup"><span data-stu-id="d11b0-110">**To implement IABProvider::Log**</span></span>
  
1. <span data-ttu-id="d11b0-111">Inicializar todos los punteros de parámetro de salida que se pasó por MAPI.</span><span class="sxs-lookup"><span data-stu-id="d11b0-111">Initialize all of the output parameter pointers passed in by MAPI.</span></span> 
    
2. <span data-ttu-id="d11b0-112">Llamar al método **IUnknown:: AddRef** del objeto de soporte técnico para incrementar su recuento de referencia.</span><span class="sxs-lookup"><span data-stu-id="d11b0-112">Call the support object's **IUnknown::AddRef** method to increment its reference count.</span></span> 
    
3. <span data-ttu-id="d11b0-113">Llamar al método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) del objeto de soporte técnico para abrir la sección del perfil que contiene información de configuración acerca de su proveedor.</span><span class="sxs-lookup"><span data-stu-id="d11b0-113">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to open the section of the profile that contains configuration information about your provider.</span></span> <span data-ttu-id="d11b0-114">Pase NULL para el parámetro _lpUID_ y el indicador MAPI_MODIFY si va a realizar cambios.</span><span class="sxs-lookup"><span data-stu-id="d11b0-114">Pass NULL for the  _lpUID_ parameter and the MAPI_MODIFY flag if you intend to make changes.</span></span> 
    
4. <span data-ttu-id="d11b0-115">Llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la sección de perfil para recuperar las propiedades que necesita su proveedor de inicio de sesión, como el nombre de la tabla de base de datos o archivo de datos.</span><span class="sxs-lookup"><span data-stu-id="d11b0-115">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the properties that your provider needs for logon, such as the name of the data file or database table.</span></span> 
    
5. <span data-ttu-id="d11b0-116">Compruebe que las propiedades están todas disponibles y válido.</span><span class="sxs-lookup"><span data-stu-id="d11b0-116">Check that the properties are all available and valid.</span></span> <span data-ttu-id="d11b0-117">Si es necesario y permitidos, se muestra un cuadro de diálogo para pedir al usuario que realice las correcciones o adiciones a la información no es válido o falta y llamar al método [IMAPIProp::SetProps](imapiprop-setprops.md) de la sección de perfil para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="d11b0-117">If necessary and allowed, display a dialog box to prompt the user to make corrections or additions to invalid or missing information and call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to save any changes.</span></span> <span data-ttu-id="d11b0-118">Algunas de las propiedades comunes que deberían estar disponibles son:</span><span class="sxs-lookup"><span data-stu-id="d11b0-118">Some of the common properties that should be available include:</span></span> 
    
   <span data-ttu-id="d11b0-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d11b0-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
   <span data-ttu-id="d11b0-120">**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d11b0-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
   <span data-ttu-id="d11b0-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d11b0-121">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
   <span data-ttu-id="d11b0-122">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d11b0-122">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="d11b0-123">No establezca **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) o **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d11b0-123">Do not set **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) or **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)).</span></span> <span data-ttu-id="d11b0-124">En tiempo de inicio de sesión, estas propiedades son de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="d11b0-124">At logon time, these properties are read-only.</span></span> 
  
6. <span data-ttu-id="d11b0-125">Si una o más propiedades de configuración no están disponibles, se producirá un error y devolver el valor MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="d11b0-125">If one or more configuration properties are unavailable, fail and return the value MAPI_E_UNCONFIGURED.</span></span>
    
7. <span data-ttu-id="d11b0-126">Llame a [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) para registrar un [MAPIUID](mapiuid.md).</span><span class="sxs-lookup"><span data-stu-id="d11b0-126">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) to register a [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="d11b0-127">El proveedor puede crear una **MAPIUID** por:</span><span class="sxs-lookup"><span data-stu-id="d11b0-127">Your provider can create a **MAPIUID** by:</span></span> 
    
   - <span data-ttu-id="d11b0-128">Llamar al método [IMAPISupport::NewUID](imapisupport-newuid.md) .</span><span class="sxs-lookup"><span data-stu-id="d11b0-128">Calling the [IMAPISupport::NewUID](imapisupport-newuid.md) method.</span></span> 
    
   - <span data-ttu-id="d11b0-129">Llamar a la UUIDGEN. Herramienta de EXE para definir un GUID que el proveedor se usa para incluir en uno de sus archivos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="d11b0-129">Calling the UUIDGEN.EXE tool to define a GUID that your provider uses to include in one of its header files.</span></span>
    
8. <span data-ttu-id="d11b0-130">Si lo desea, guarde un recién creado **MAPIUID** en el perfil actual mediante una llamada a la sección de perfil ** IMAPIProp::SetProps ** (método).</span><span class="sxs-lookup"><span data-stu-id="d11b0-130">If desired, save a newly created **MAPIUID** in the current profile by calling the profile section's ** IMAPIProp::SetProps ** method.</span></span> 
    
9. <span data-ttu-id="d11b0-131">Versión de la sección de perfil llamando a su método **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="d11b0-131">Release the profile section by calling its **IUnknown::Release** method.</span></span> 
    
10. <span data-ttu-id="d11b0-132">Crear una instancia de un nuevo objeto de inicio de sesión y establecer el contenido del parámetro _lppABLogon_ a la dirección de este nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="d11b0-132">Instantiate a new logon object and set the contents of the  _lppABLogon_ parameter to the address of this new object.</span></span> 
    
<span data-ttu-id="d11b0-133">Debido a que es posible de MAPI para llamar a su ** inicio de sesión ** método varias veces durante una sesión, es conveniente admitir esta posibilidad en su implementación por la posibilidad de crear varios objetos de inicio de sesión y realizar un seguimiento de cada objeto que se crea.</span><span class="sxs-lookup"><span data-stu-id="d11b0-133">Because it is possible for MAPI to call your ** Logon ** method several times during a session, it is wise to support this possibility in your implementation by being able to create multiple logon objects and keep track of each object that is created.</span></span> <span data-ttu-id="d11b0-134">Admitir varias llamadas de **Inicio de sesión** , permite a un usuario de una aplicación cliente, por ejemplo, para iniciar sesión en una sesión con identidades diferentes o destinos de entrega diferentes de uso.</span><span class="sxs-lookup"><span data-stu-id="d11b0-134">Supporting multiple **Logon** calls enables a user of a client application, for example, to log on to a session with different identities or use different delivery destinations.</span></span> 
  
<span data-ttu-id="d11b0-135">Se llama al método **Shutdown** cuando finaliza la sesión.</span><span class="sxs-lookup"><span data-stu-id="d11b0-135">**Shutdown** is called when the session is ending.</span></span> <span data-ttu-id="d11b0-136">MAPI llama a su método [IABProvider::Shutdown](iabprovider-shutdown.md) como una de las tareas última necesarios para cerrar una sesión.</span><span class="sxs-lookup"><span data-stu-id="d11b0-136">MAPI calls your [IABProvider::Shutdown](iabprovider-shutdown.md) method as one of the last tasks involved in shutting down a session.</span></span> <span data-ttu-id="d11b0-137">MAPI ha publicado todos los objetos de su proveedor inicio de sesión y, cuando el proveedor recibe esta llamada, puede suponer que se trata de la última llamada que va a recibir.</span><span class="sxs-lookup"><span data-stu-id="d11b0-137">MAPI has released all of your provider's logon objects and, when your provider receives this call, it can assume that this is the last call it will receive.</span></span> <span data-ttu-id="d11b0-138">En la implementación de **IABProvider::Shutdown**, realizar la limpieza final que se siente es necesario.</span><span class="sxs-lookup"><span data-stu-id="d11b0-138">In your implementation of **IABProvider::Shutdown**, perform any final cleanup that you feel is necessary.</span></span> <span data-ttu-id="d11b0-139">Por ejemplo, el proveedor puede llamar a **MAPIDeinitIdle** si se denomina **MAPIInitIdle** para usar el motor de inactividad durante la sesión o el método **IUnknown:: Release** de todos los objetos que todavía tiene que liberar.</span><span class="sxs-lookup"><span data-stu-id="d11b0-139">For example, your provider might call **MAPIDeinitIdle** if it has called **MAPIInitIdle** to use the idle engine during the session or the **IUnknown::Release** method of any objects that have yet to be released.</span></span> 
  
<span data-ttu-id="d11b0-140">Si su proveedor no tiene ninguna limpieza final, su implementación puede constar de una sola línea de código:</span><span class="sxs-lookup"><span data-stu-id="d11b0-140">If your provider has no final cleanup, its implementation can be made up of a single line of code:</span></span> 
  
```cpp
return S_OK;

```


