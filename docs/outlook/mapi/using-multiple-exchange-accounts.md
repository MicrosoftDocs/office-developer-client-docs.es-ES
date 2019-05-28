---
title: Usar varias cuentas de Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4e1804bf-4c50-4942-a7ab-9a8caf1be7e5
description: 'Última modificación: 25 de junio de 2012'
ms.openlocfilehash: a5792ebaf78d77924bc3157be63d937b66e9f4b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329658"
---
# <a name="using-multiple-exchange-accounts"></a><span data-ttu-id="d6c95-103">Usar varias cuentas de Exchange</span><span class="sxs-lookup"><span data-stu-id="d6c95-103">Using Multiple Exchange Accounts</span></span>

  
  
<span data-ttu-id="d6c95-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6c95-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6c95-105">Microsoft Outlook 2010 y Microsoft Outlook 2013 admiten la integración con varias cuentas de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d6c95-105">Microsoft Outlook 2010 and Microsoft Outlook 2013 support integration with multiple exchange e-mail accounts.</span></span> <span data-ttu-id="d6c95-106">En Outlook 2010 o Outlook 2013, un usuario podía añadir dos cuentas de Exchange al mismo perfil y seguir disfrutando de las características enriquecidas de Exchange, como la lista global de direcciones (GAL), la configuración Fuera de la Oficina de Exchange y el uso compartido de carpetas.</span><span class="sxs-lookup"><span data-stu-id="d6c95-106">In Outlook 2010 or Outlook 2013, a user could add two exchange accounts to the same profile and still enjoy rich Exchange features such as the published global address list (GAL), Exchange Out-of-Office configuration, and folder sharing.</span></span>
  
<span data-ttu-id="d6c95-107">Quienes ya conocían las secciones de perfil MAPI de Microsoft Office Outlook 2007 y versiones anteriores sabían que la configuración de Exchange, como el nombre de usuario de correo electrónico y el nombre de servidor, se almacenaba en la sección fijada de Perfil Global de Exchange, **pbGlobalProfileSectionGuid**.</span><span class="sxs-lookup"><span data-stu-id="d6c95-107">Those familiar with the MAPI profile sections for Microsoft Office Outlook 2007 and earlier know that Exchange settings, such as the e-mail user name and server name, are stored in the fixed Exchange Global Profile section, **pbGlobalProfileSectionGuid**.</span></span> <span data-ttu-id="d6c95-108">En Outlook 2010 y Outlook 2013, todas las cuentas de Exchange necesitan su propia sección de perfil para almacenar la configuración, lo que vuelve obsoleto **pbGlobalProfileSectionGuid**.</span><span class="sxs-lookup"><span data-stu-id="d6c95-108">In Outlook 2010 and Outlook 2013, each Exchange account needs its own profile section to store settings, making the **pbGlobalProfileSectionGuid** obsolete.</span></span> 
  
<span data-ttu-id="d6c95-p103">Las opciones de configuración de Exchange 2010 y Outlook 2013 siguen almacenadas en el perfil, pero se asigna dinámicamente para cada perfil un identificador único para la sección de perfil que contiene su configuración. La ubicación de la configuración de Exchange en el perfil se almacena en la [Propiedad Canónica PidTagExchangeProfileSectionId](pidtagexchangeprofilesectionid-canonical-property.md), que se puede encontrar en la sección de perfil de servicio de mensajes de la cuenta de Exchange. Esta propiedad también se puede encontrar en la sección de perfil para cada proveedor en este servicio de mensaje de la cuenta. El identificador único no se almacena en el servidor y varía en los distintos perfiles.</span><span class="sxs-lookup"><span data-stu-id="d6c95-p103">Outlook 2010 and Outlook 2013 Exchange settings are still stored in the profile, but a unique identifier for the profile section that contains their settings is dynamically allocated per profile. The location of the Exchange settings in the profile is stored in the [PidTagExchangeProfileSectionId Canonical Property](pidtagexchangeprofilesectionid-canonical-property.md), which can be found in the message service profile section of the Exchange account. This property can also be found in the profile section for each provider in this message service of the account. The unique identifier is not stored on the server and will be different across profiles.</span></span>
  
<span data-ttu-id="d6c95-p104">Outlook 2010 y Outlook 2013 usan **PidTagExchangeProfileSectionId** como identificador único para especificar una cuenta de Exchange. Cuando se usa de esta manera, este identificador único se denomina **emsmdbUID**. En algunas operaciones MAPI y Outlook, es posible que se necesite un **emsmdbUID** para especificar la cuenta de Exchange que se debe usar para la operación.</span><span class="sxs-lookup"><span data-stu-id="d6c95-p104">Outlook 2010 and Outlook 2013 use the **PidTagExchangeProfileSectionId** as a unique identifier to specify an Exchange account. When used in this manner, this unique identifier is known as the **emsmdbUID**. For some MAPI and Outlook operations, an **emsmdbUID** might be required to specify which Exchange account should be used for the operation.</span></span> 
  
<span data-ttu-id="d6c95-p105">A fin de admitir varias cuentas de Exchange, se deben usar algunas llamadas a las nuevas funciones en su código. Reemplace cualquier llamada que utilice una **entryID** y una [IAddrBook::OpenEntry](iaddrbook-openentry.md) o [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) en [IMailUser : IMAPIProp](imailuserimapiprop.md), así como [IDistList : IMAPIContainer](idistlistimapicontainer.md), por una de las funciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="d6c95-p105">In order to support multiple Exchange accounts, you must use some calls to new functions in your code. Replace any call that uses an **entryID** and either [IAddrBook::OpenEntry](iaddrbook-openentry.md) or [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) on [IMailUser : IMAPIProp](imailuserimapiprop.md) and [IDistList : IMAPIContainer](idistlistimapicontainer.md) with one of the following functions.</span></span> 
  
- [<span data-ttu-id="d6c95-118">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="d6c95-118">HrCompareABEntryIDsWithExchangeContext</span></span>](hrcompareabentryidswithexchangecontext.md)
    
- [<span data-ttu-id="d6c95-119">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="d6c95-119">HrDoABDetailsWithExchangeContext</span></span>](hrdoabdetailswithexchangecontext.md)
    
- [<span data-ttu-id="d6c95-120">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="d6c95-120">HrDoABDetailsWithProviderUID</span></span>](hrdoabdetailswithprovideruid.md)
    
- [<span data-ttu-id="d6c95-121">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="d6c95-121">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)
    
- [<span data-ttu-id="d6c95-122">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="d6c95-122">HrOpenABEntryUsingDefaultContext</span></span>](hropenabentryusingdefaultcontext.md)
    
- [<span data-ttu-id="d6c95-123">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="d6c95-123">HrOpenABEntryWithExchangeContext</span></span>](hropenabentrywithexchangecontext.md)
    
- [<span data-ttu-id="d6c95-124">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="d6c95-124">HrOpenABEntryWithProviderUID</span></span>](hropenabentrywithprovideruid.md)
    
- [<span data-ttu-id="d6c95-125">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="d6c95-125">HrOpenABEntryWithProviderUIDSupport</span></span>](hropenabentrywithprovideruidsupport.md)
    
- [<span data-ttu-id="d6c95-126">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="d6c95-126">HrOpenABEntryWithResolvedRow</span></span>](hropenabentrywithresolvedrow.md)
    
- [<span data-ttu-id="d6c95-127">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="d6c95-127">HrOpenABEntryWithSupport</span></span>](hropenabentrywithsupport.md)
    
## <a name="legacy-support"></a><span data-ttu-id="d6c95-128">Soporte técnico heredado</span><span class="sxs-lookup"><span data-stu-id="d6c95-128">Legacy support</span></span>

<span data-ttu-id="d6c95-p106">Se siguen admitiendo todos los clientes MAPI escritos antes de la creación de esta nueva sección **emsmdbUID**. Estos clientes seguirán recuperando la sección global anterior, **pbGlobalProfileSectionGuid**. Las consultas de esta sección de perfil se redirigirán a una cuenta de Exchange designada que controla las consultas heredadas. La cuenta que controla las llamadas heredadas se puede determinar buscando en la tabla de servicio de mensajes y agregando una columna para PR_EMSMDB_LEGACY. Solo un único servicio de mensajes la tendrá definida como true y su **PidTagExchangeProfileSectionId** se denomina **emsmdbUID** heredado.</span><span class="sxs-lookup"><span data-stu-id="d6c95-p106">Any MAPI clients written before the creation of this new **emsmdbUID** section are still supported. These clients will continue to retrieve the previous global section, **pbGlobalProfileSectionGuid**. Queries for this profile section will be redirected to one designated Exchange account that handles legacy inquiries. The account that handles the legacy calls can be determined by looking at the message service table and adding a column for PR_EMSMDB_LEGACY. Only one message service will have this set to true, and its **PidTagExchangeProfileSectionId** is called the legacy **emsmdbUID**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d6c95-p107">Las opciones de ajustes de MAPI configurables, como el almacenamiento predeterminada y la cuenta predeterminada, no tienen ningún efecto en la cuenta que realiza llamadas heredadas. No se puede configurar la cuenta que controla las llamadas heredadas.</span><span class="sxs-lookup"><span data-stu-id="d6c95-p107">Configurable MAPI settings such as the default store and the default account have no effect on which account handles legacy calls. The account that handles the legacy calls cannot be configured.</span></span> 
  
<span data-ttu-id="d6c95-p108">El **emsmdbUID** de la cuenta heredada se copia a la sección del perfil global de Outlook. Si esta propiedad no existe, una consulta a la tabla de servicios de mensajes determinará qué cuenta es el controlador heredado y establecerá el valor en la sección de perfil global de Outlook.</span><span class="sxs-lookup"><span data-stu-id="d6c95-p108">The **emsmdbUID** of the legacy account is copied to the Outlook Global Profile Section. If this property does not exist, querying for the message services table will determine what account is the legacy handler and set the value in the Outlook Global Profile Section.</span></span> 
  
<span data-ttu-id="d6c95-p109">Para mayor claridad, la sección de perfil global de Outlook es diferente de la sección de perfil global de Exchange y, en Outlook 2010 y Outlook 2013, la sección de perfil global de Exchange ya no es realmente global, puesto que se pueden tener varias cuentas de Exchange. La sección perfil global de Outlook contiene propiedades sobre Outlook, como el estado de la carpeta MRU o el estado de la conexión global.</span><span class="sxs-lookup"><span data-stu-id="d6c95-p109">To be clear, the Outlook Global Profile Section differs from the Exchange Global Profile Section, and in Outlook 2010 and Outlook 2013 the Exchange Global Profile Section is no longer really global because you can have multiple Exchange accounts. The Outlook Global Profile section contains properties about Outlook, such as the state of the folder MRU or the state of the global connection.</span></span>
  
## <a name="address-book-account-contexts"></a><span data-ttu-id="d6c95-140">Contextos de cuenta de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="d6c95-140">Address Book Account Contexts</span></span>

<span data-ttu-id="d6c95-141">Para resolver las direcciones correctamente con varias cuentas de Exchange, use las nuevas funciones que toman un contexto de cuenta para que las llamadas a la libreta de direcciones busquen la cuenta de Exchange adecuada.</span><span class="sxs-lookup"><span data-stu-id="d6c95-141">To resolve addresses correctly with multiple Exchange accounts, use the new functions that take an account context so that calls to the address book search the correct Exchange account.</span></span>
  
<span data-ttu-id="d6c95-p110">Algunas API de libreta de direcciones anteriores eran obsoletas porque las API no eran totalmente compatibles con Exchange. Este contexto de cuenta suele ser un **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="d6c95-p110">Some previous address book APIs were deprecated because the APIs were not fully multiple Exchange capable. This account context is usually an **emsmdbUID**.</span></span>
  
<span data-ttu-id="d6c95-144">Además del **emsmdbUID**, las cuentas múltiples de Exchange también tienen un **emsabpUID**.</span><span class="sxs-lookup"><span data-stu-id="d6c95-144">In addition to the **emsmdbUID**, multiple Exchange accounts also have an **emsabpUID**.</span></span>
  
1. <span data-ttu-id="d6c95-145">El valor de **emsmdbUID** identifica el contexto de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="d6c95-145">The **emsmdbUID** value identifies the account context.</span></span> 
    
2. <span data-ttu-id="d6c95-146">El valor de **emsabpUID** identifica un proveedor de libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d6c95-146">The **emsabpUID** value identifies an Exchange address book provider.</span></span> 
    
<span data-ttu-id="d6c95-p111">El valor de **emsabpUID** se utiliza habitualmente al resolver un destinatario. Al resolver un destinatario utilizando [IAddrBook::ResolveName](iaddrbook-resolvename.md), una fila de destinatario de Exchange puede contener la propiedad **PR_AB_PROVIDERS** (0x3D010102), que contiene el valor de **emsabpUID**. Este valor de **emsabpUID** identifica el proveedor de libreta de direcciones de Exchange para el destinatario específico.</span><span class="sxs-lookup"><span data-stu-id="d6c95-p111">The **emsabpUID** value is typically used when resolving a recipient. When resolving a recipient using [IAddrBook::ResolveName](iaddrbook-resolvename.md), an Exchange recipient row contains the **PR_AB_PROVIDERS** (0x3D010102) property, which contains the **emsabpUID** value. This **emsabpUID** value identifies the Exchange address book provider for the specific recipient.</span></span> 
  
<span data-ttu-id="d6c95-150">Si desea determinar el valor de **emsabpUID** para un **emsmdbUID** concreto, abra la sección de perfil del **emsmdbUID** y obtenga la propiedad **PR_EMSABP_USER_UID** (0x0x3D1A0102).</span><span class="sxs-lookup"><span data-stu-id="d6c95-150">If you want to determine the **emsabpUID** value for a particular **emsmdbUID**, open up the profile section for the **emsmdbUID** and get the **PR_EMSABP_USER_UID** (0x0x3D1A0102) property.</span></span> 
  
<span data-ttu-id="d6c95-p112">Si está llamando a [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), asegúrese de que los destinatarios de Exchange de la lista que pase contengan la propiedad **PR_AB_PROVIDERS** que tiene el **emsabpUID** que corresponde al proveedor de libreta de direcciones al que pertenece el destinatario. Para llamar a un [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) en una fila que ha obtenido desde [IAddrBook::ResolveName](iaddrbook-resolvename.md) no requiere realizar acciones adicionales, pero el código llamará a [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) en filas que únicamente contienen la propiedad **PR_ENTRYID**. Las filas en esta situación y en situaciones similares deberían contener **PR_ENTRYID** y **PR_AB_PROVIDERS** con la propiedad **PR_AB_PROVIDERS** ajustada para el **emsabpUID** correcto.</span><span class="sxs-lookup"><span data-stu-id="d6c95-p112">If you are calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), make sure that the Exchange recipients in the list that you pass in contain the **PR_AB_PROVIDERS** property that has the **emsabpUID** that corresponds to the address book provider that the recipient belongs to. Calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on a row that you obtained from [IAddrBook::ResolveName](iaddrbook-resolvename.md) requires no additional action, but some code will call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on rows that contain only the **PR_ENTRYID** property. Rows in this and similar situations should contain both **PR_ENTRYID** and **PR_AB_PROVIDERS** with the **PR_AB_PROVIDERS** property set to the correct **emsabpUID**.</span></span>
  
<span data-ttu-id="d6c95-154">Una descripción simple del proceso para resolver varias cuentas de Exchange es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="d6c95-154">A simple description of the process for resolving multiple Exchange accounts is as follows:</span></span>
  
- <span data-ttu-id="d6c95-p113">Dado el identificador único de servicio, el código busca en la tabla el almacén de mensajes de la propiedad **PR_SERVICE_UID** que coincide con la única que se dispone. A partir de ahí, se puede determinar el **PR_MDB_PROVIDER** correcto. Esta fila contiene el almacén adecuado.</span><span class="sxs-lookup"><span data-stu-id="d6c95-p113">Given the service unique identifier, your code looks in the table of the message store of the **PR_SERVICE_UID** property that matches the one that you have. From there, you can determine the correct **PR_MDB_PROVIDER**. This row contains the appropriate store.</span></span>
    
- <span data-ttu-id="d6c95-158">Dado un **emsmdbUID**, su código busca en la tabla de servicios de mensaje la fila que expone el **PidTagExchangeProfileSectionId** que coincide con el **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="d6c95-158">Given an **emsmdbUID**, your code looks in the message services table for the row that exposes the **PidTagExchangeProfileSectionId** that matches the **emsmdbUID**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d6c95-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6c95-159">See also</span></span>



[<span data-ttu-id="d6c95-160">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="d6c95-160">HrCompareABEntryIDsWithExchangeContext</span></span>](hrcompareabentryidswithexchangecontext.md)
  
[<span data-ttu-id="d6c95-161">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="d6c95-161">HrDoABDetailsWithExchangeContext</span></span>](hrdoabdetailswithexchangecontext.md)
  
[<span data-ttu-id="d6c95-162">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="d6c95-162">HrDoABDetailsWithProviderUID</span></span>](hrdoabdetailswithprovideruid.md)
  
[<span data-ttu-id="d6c95-163">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="d6c95-163">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)
  
[<span data-ttu-id="d6c95-164">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="d6c95-164">HrOpenABEntryUsingDefaultContext</span></span>](hropenabentryusingdefaultcontext.md)
  
[<span data-ttu-id="d6c95-165">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="d6c95-165">HrOpenABEntryWithExchangeContext</span></span>](hropenabentrywithexchangecontext.md)
  
[<span data-ttu-id="d6c95-166">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="d6c95-166">HrOpenABEntryWithProviderUID</span></span>](hropenabentrywithprovideruid.md)
  
[<span data-ttu-id="d6c95-167">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="d6c95-167">HrOpenABEntryWithProviderUIDSupport</span></span>](hropenabentrywithprovideruidsupport.md)
  
[<span data-ttu-id="d6c95-168">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="d6c95-168">HrOpenABEntryWithResolvedRow</span></span>](hropenabentrywithresolvedrow.md)
  
[<span data-ttu-id="d6c95-169">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="d6c95-169">HrOpenABEntryWithSupport</span></span>](hropenabentrywithsupport.md)
  
[<span data-ttu-id="d6c95-170">Propiedad Canónica PidTagExchangeProfileSectionId</span><span class="sxs-lookup"><span data-stu-id="d6c95-170">PidTagExchangeProfileSectionId Canonical Property</span></span>](pidtagexchangeprofilesectionid-canonical-property.md)


[<span data-ttu-id="d6c95-171">Cómo abrir la sección Perfil global</span><span class="sxs-lookup"><span data-stu-id="d6c95-171">How To Open the Global Profile Section</span></span>](https://support.microsoft.com/kb/188482)

