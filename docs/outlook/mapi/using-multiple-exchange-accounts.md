---
title: Usar varias cuentas de Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4e1804bf-4c50-4942-a7ab-9a8caf1be7e5
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: a5792ebaf78d77924bc3157be63d937b66e9f4b2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723064"
---
# <a name="using-multiple-exchange-accounts"></a><span data-ttu-id="974f2-103">Usar varias cuentas de Exchange</span><span class="sxs-lookup"><span data-stu-id="974f2-103">Using Multiple Exchange Accounts</span></span>

  
  
<span data-ttu-id="974f2-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="974f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="974f2-105">Microsoft Outlook 2010 y Microsoft Outlook 2013 admiten la integración con varias cuentas de correo electrónico de exchange.</span><span class="sxs-lookup"><span data-stu-id="974f2-105">Microsoft Outlook 2010 and Microsoft Outlook 2013 support integration with multiple exchange email accounts.</span></span> <span data-ttu-id="974f2-106">En Outlook 2010 o Outlook 2013, un usuario podr�a agregar dos cuentas de exchange para el mismo perfil y seguir disfrutando de las caracter�sticas avanzadas de Exchange, como la lista publicada global de direcciones (GAL), la configuraci�n de Exchange fuera de la oficina y uso compartido de carpetas.</span><span class="sxs-lookup"><span data-stu-id="974f2-106">In Outlook 2010 or Outlook 2013, a user could add two exchange accounts to the same profile and still enjoy rich Exchange features such as the published global address list (GAL), Exchange Out-of-Office configuration, and folder sharing.</span></span>
  
<span data-ttu-id="974f2-107">Esos familiarizado con las secciones de perfil MAPI de Microsoft Office Outlook 2007 y versiones anteriores saben que la configuración de Exchange, como el nombre de usuario de correo electrónico y el nombre del servidor, se almacena en la sección de perfil de Exchange Global fija, **pbGlobalProfileSectionGuid**.</span><span class="sxs-lookup"><span data-stu-id="974f2-107">Those familiar with the MAPI profile sections for Microsoft Office Outlook 2007 and earlier know that Exchange settings, such as the email user name and server name, are stored in the fixed Exchange Global Profile section, **pbGlobalProfileSectionGuid**.</span></span> <span data-ttu-id="974f2-108">En Outlook 2010 y Outlook 2013, cada cuenta de Exchange necesita su propia secci�n de perfil para almacenar la configuraci�n, realizar la **pbGlobalProfileSectionGuid** obsoleto.</span><span class="sxs-lookup"><span data-stu-id="974f2-108">In Outlook 2010 and Outlook 2013, each Exchange account needs its own profile section to store settings, making the **pbGlobalProfileSectionGuid** obsolete.</span></span> 
  
<span data-ttu-id="974f2-p103">Outlook 2010 and Outlook 2013 Exchange settings are still stored in the profile, but a unique identifier for the profile section that contains their settings is dynamically allocated per profile. The location of the Exchange settings in the profile is stored in the [Propiedad can�nico de PidTagExchangeProfileSectionId](pidtagexchangeprofilesectionid-canonical-property.md), which can be found in the message service profile section of the Exchange account. This property can also be found in the profile section for each provider in this message service of the account. The unique identifier is not stored on the server and will be different across profiles.</span><span class="sxs-lookup"><span data-stu-id="974f2-p103">Outlook 2010 and Outlook 2013 Exchange settings are still stored in the profile, but a unique identifier for the profile section that contains their settings is dynamically allocated per profile. The location of the Exchange settings in the profile is stored in the [PidTagExchangeProfileSectionId Canonical Property](pidtagexchangeprofilesectionid-canonical-property.md), which can be found in the message service profile section of the Exchange account. This property can also be found in the profile section for each provider in this message service of the account. The unique identifier is not stored on the server and will be different across profiles.</span></span>
  
<span data-ttu-id="974f2-p104">Outlook 2010 y Outlook 2013 utilizan el **PidTagExchangeProfileSectionId** como un identificador �nico para especificar una cuenta de Exchange. Cuando se usa de esta manera, este identificador �nico se conoce como el **emsmdbUID**. Para algunas operaciones MAPI y Outlook, un **emsmdbUID** puede requerirse para especificar qu� cuenta de Exchange debe usarse para la operaci�n.</span><span class="sxs-lookup"><span data-stu-id="974f2-p104">Outlook 2010 and Outlook 2013 use the **PidTagExchangeProfileSectionId** as a unique identifier to specify an Exchange account. When used in this manner, this unique identifier is known as the **emsmdbUID**. For some MAPI and Outlook operations, an **emsmdbUID** might be required to specify which Exchange account should be used for the operation.</span></span> 
  
<span data-ttu-id="974f2-p105">In order to support multiple Exchange accounts, you must use some calls to new functions in your code. Replace any call that uses an **entryID** and either [IAddrBook::OpenEntry](iaddrbook-openentry.md) or [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) on [IMailUser: IMAPIProp](imailuserimapiprop.md) and [IDistList: IMAPIContainer](idistlistimapicontainer.md) with one of the following functions.</span><span class="sxs-lookup"><span data-stu-id="974f2-p105">In order to support multiple Exchange accounts, you must use some calls to new functions in your code. Replace any call that uses an **entryID** and either [IAddrBook::OpenEntry](iaddrbook-openentry.md) or [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) on [IMailUser : IMAPIProp](imailuserimapiprop.md) and [IDistList : IMAPIContainer](idistlistimapicontainer.md) with one of the following functions.</span></span> 
  
- [<span data-ttu-id="974f2-118">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="974f2-118">HrCompareABEntryIDsWithExchangeContext</span></span>](hrcompareabentryidswithexchangecontext.md)
    
- [<span data-ttu-id="974f2-119">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="974f2-119">HrDoABDetailsWithExchangeContext</span></span>](hrdoabdetailswithexchangecontext.md)
    
- [<span data-ttu-id="974f2-120">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="974f2-120">HrDoABDetailsWithProviderUID</span></span>](hrdoabdetailswithprovideruid.md)
    
- [<span data-ttu-id="974f2-121">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="974f2-121">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)
    
- [<span data-ttu-id="974f2-122">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="974f2-122">HrOpenABEntryUsingDefaultContext</span></span>](hropenabentryusingdefaultcontext.md)
    
- [<span data-ttu-id="974f2-123">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="974f2-123">HrOpenABEntryWithExchangeContext</span></span>](hropenabentrywithexchangecontext.md)
    
- [<span data-ttu-id="974f2-124">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="974f2-124">HrOpenABEntryWithProviderUID</span></span>](hropenabentrywithprovideruid.md)
    
- [<span data-ttu-id="974f2-125">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="974f2-125">HrOpenABEntryWithProviderUIDSupport</span></span>](hropenabentrywithprovideruidsupport.md)
    
- [<span data-ttu-id="974f2-126">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="974f2-126">HrOpenABEntryWithResolvedRow</span></span>](hropenabentrywithresolvedrow.md)
    
- [<span data-ttu-id="974f2-127">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="974f2-127">HrOpenABEntryWithSupport</span></span>](hropenabentrywithsupport.md)
    
## <a name="legacy-support"></a><span data-ttu-id="974f2-128">Compatibilidad con heredado</span><span class="sxs-lookup"><span data-stu-id="974f2-128">Legacy support</span></span>

<span data-ttu-id="974f2-p106">Los clientes MAPI escritos antes de la creaci�n de esta nueva secci�n **emsmdbUID** a�n se admiten. Estos clientes seguir�n recuperar la secci�n global anterior, **pbGlobalProfileSectionGuid**. Las consultas de esta secci�n de perfil ser� redirigidas a una cuenta de Exchange designada que administra consultas heredadas. Puede determinar la cuenta que administra las llamadas heredadas busca en la tabla de servicios de mensaje y agregando una columna para PR_EMSMDB_LEGACY. Solo un servicio de mensaje tendr�n establecido en true y su **PidTagExchangeProfileSectionId** se denomina la heredado **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="974f2-p106">Any MAPI clients written before the creation of this new **emsmdbUID** section are still supported. These clients will continue to retrieve the previous global section, **pbGlobalProfileSectionGuid**. Queries for this profile section will be redirected to one designated Exchange account that handles legacy inquiries. The account that handles the legacy calls can be determined by looking at the message service table and adding a column for PR_EMSMDB_LEGACY. Only one message service will have this set to true, and its **PidTagExchangeProfileSectionId** is called the legacy **emsmdbUID**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="974f2-p107">[!NOTA] Opciones de configuraci�n de MAPI, como el almac�n predeterminado y la cuenta predeterminada de tengan ning�n efecto en el que cuenta controla las llamadas heredadas. No se puede configurar la cuenta que administra las llamadas heredadas.</span><span class="sxs-lookup"><span data-stu-id="974f2-p107">Configurable MAPI settings such as the default store and the default account have no effect on which account handles legacy calls. The account that handles the legacy calls cannot be configured.</span></span> 
  
<span data-ttu-id="974f2-p108">El **emsmdbUID** de la cuenta heredada se copian en la Outlook secci�n de perfil Global. Si esta propiedad no existe, la consulta de la tabla de servicios de mensaje determinar qu� cuenta es el controlador heredado y establecer el valor en la secci�n de perfil Global Outlook.</span><span class="sxs-lookup"><span data-stu-id="974f2-p108">The **emsmdbUID** of the legacy account is copied to the Outlook Global Profile Section. If this property does not exist, querying for the message services table will determine what account is the legacy handler and set the value in the Outlook Global Profile Section.</span></span> 
  
<span data-ttu-id="974f2-p109">Para borrar la Outlook que secci�n de perfil Global difiere de la secci�n de perfil Global de Exchange, y en Outlook 2010 y Outlook 2013 la secci�n de perfil Global de Exchange ya no es realmente global porque puede tener varias cuentas de Exchange. Outlook secci�n de perfil Global contiene propiedades de Outlook, como el estado de la carpeta de elementos utilizados Recientemente o el estado de la conexi�n global.</span><span class="sxs-lookup"><span data-stu-id="974f2-p109">To be clear, the Outlook Global Profile Section differs from the Exchange Global Profile Section, and in Outlook 2010 and Outlook 2013 the Exchange Global Profile Section is no longer really global because you can have multiple Exchange accounts. The Outlook Global Profile section contains properties about Outlook, such as the state of the folder MRU or the state of the global connection.</span></span>
  
## <a name="address-book-account-contexts"></a><span data-ttu-id="974f2-140">Contextos de cuenta de libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="974f2-140">Address Book Account Contexts</span></span>

<span data-ttu-id="974f2-141">Para resolver direcciones correctamente con varias cuentas de Exchange, utilice las nuevas funciones que toman un contexto de la cuenta para que la cuenta de Exchange correcta de b�squeda de las llamadas a la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="974f2-141">To resolve addresses correctly with multiple Exchange accounts, use the new functions that take an account context so that calls to the address book search the correct Exchange account.</span></span>
  
<span data-ttu-id="974f2-p110">Algunos libreta de direcciones anterior API son obsoletas debido a las API no eran capaces de Exchange completamente varios. En este contexto de la cuenta normalmente es un **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="974f2-p110">Some previous address book APIs were deprecated because the APIs were not fully multiple Exchange capable. This account context is usually an **emsmdbUID**.</span></span>
  
<span data-ttu-id="974f2-144">Adem�s de la **emsmdbUID**, varias cuentas de Exchange tienen un **emsabpUID**.</span><span class="sxs-lookup"><span data-stu-id="974f2-144">In addition to the **emsmdbUID**, multiple Exchange accounts also have an **emsabpUID**.</span></span>
  
1. <span data-ttu-id="974f2-145">El valor de **emsmdbUID** identifica el contexto de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="974f2-145">The **emsmdbUID** value identifies the account context.</span></span> 
    
2. <span data-ttu-id="974f2-146">El valor de **emsabpUID** identifica un proveedor de libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="974f2-146">The **emsabpUID** value identifies an Exchange address book provider.</span></span> 
    
<span data-ttu-id="974f2-p111">The **emsabpUID** value is typically used when resolving a recipient. When resolving a recipient using [IAddrBook::ResolveName](iaddrbook-resolvename.md), an Exchange recipient row contains the **PR_AB_PROVIDERS** (0x3D010102) property, which contains the **emsabpUID** value. This **emsabpUID** value identifies the Exchange address book provider for the specific recipient.</span><span class="sxs-lookup"><span data-stu-id="974f2-p111">The **emsabpUID** value is typically used when resolving a recipient. When resolving a recipient using [IAddrBook::ResolveName](iaddrbook-resolvename.md), an Exchange recipient row contains the **PR_AB_PROVIDERS** (0x3D010102) property, which contains the **emsabpUID** value. This **emsabpUID** value identifies the Exchange address book provider for the specific recipient.</span></span> 
  
<span data-ttu-id="974f2-150">Si desea determinar el valor de **emsabpUID** para un determinado **emsmdbUID**, abra la secci�n de perfil para el **emsmdbUID** y obtener la propiedad **PR_EMSABP_USER_UID** (0x0x3D1A0102).</span><span class="sxs-lookup"><span data-stu-id="974f2-150">If you want to determine the **emsabpUID** value for a particular **emsmdbUID**, open up the profile section for the **emsmdbUID** and get the **PR_EMSABP_USER_UID** (0x0x3D1A0102) property.</span></span> 
  
<span data-ttu-id="974f2-p112">If you are calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), make sure that the Exchange recipients in the list that you pass in contain the **PR_AB_PROVIDERS** property that has the **emsabpUID** that corresponds to the address book provider that the recipient belongs to. Calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on a row that you obtained from [IAddrBook::ResolveName](iaddrbook-resolvename.md) requires no additional action, but some code will call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on rows that contain only the **PR_ENTRYID** property. Rows in this and similar situations should contain both **PR_ENTRYID** and **PR_AB_PROVIDERS** with the **PR_AB_PROVIDERS** property set to the correct **emsabpUID**.</span><span class="sxs-lookup"><span data-stu-id="974f2-p112">If you are calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), make sure that the Exchange recipients in the list that you pass in contain the **PR_AB_PROVIDERS** property that has the **emsabpUID** that corresponds to the address book provider that the recipient belongs to. Calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on a row that you obtained from [IAddrBook::ResolveName](iaddrbook-resolvename.md) requires no additional action, but some code will call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on rows that contain only the **PR_ENTRYID** property. Rows in this and similar situations should contain both **PR_ENTRYID** and **PR_AB_PROVIDERS** with the **PR_AB_PROVIDERS** property set to the correct **emsabpUID**.</span></span>
  
<span data-ttu-id="974f2-154">Una descripci�n sencilla del proceso para la resoluci�n de varias cuentas de Exchange es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="974f2-154">A simple description of the process for resolving multiple Exchange accounts is as follows:</span></span>
  
- <span data-ttu-id="974f2-p113">Dado el identificador �nico del servicio, el c�digo busca en la tabla del almac�n de mensajes de la propiedad **PR_SERVICE_UID** que coincida con el que tiene. Desde all�, puede determinar la correcta **PR_MDB_PROVIDER**. Esta fila contiene el almac�n apropiado.</span><span class="sxs-lookup"><span data-stu-id="974f2-p113">Given the service unique identifier, your code looks in the table of the message store of the **PR_SERVICE_UID** property that matches the one that you have. From there, you can determine the correct **PR_MDB_PROVIDER**. This row contains the appropriate store.</span></span>
    
- <span data-ttu-id="974f2-158">Dado un **emsmdbUID**, el c�digo que se busca en la tabla de servicios de mensaje para la fila que expone el **PidTagExchangeProfileSectionId** que coincida con la **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="974f2-158">Given an **emsmdbUID**, your code looks in the message services table for the row that exposes the **PidTagExchangeProfileSectionId** that matches the **emsmdbUID**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="974f2-159">Vea tambi�n</span><span class="sxs-lookup"><span data-stu-id="974f2-159">See also</span></span>



[<span data-ttu-id="974f2-160">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="974f2-160">HrCompareABEntryIDsWithExchangeContext</span></span>](hrcompareabentryidswithexchangecontext.md)
  
[<span data-ttu-id="974f2-161">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="974f2-161">HrDoABDetailsWithExchangeContext</span></span>](hrdoabdetailswithexchangecontext.md)
  
[<span data-ttu-id="974f2-162">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="974f2-162">HrDoABDetailsWithProviderUID</span></span>](hrdoabdetailswithprovideruid.md)
  
[<span data-ttu-id="974f2-163">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="974f2-163">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)
  
[<span data-ttu-id="974f2-164">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="974f2-164">HrOpenABEntryUsingDefaultContext</span></span>](hropenabentryusingdefaultcontext.md)
  
[<span data-ttu-id="974f2-165">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="974f2-165">HrOpenABEntryWithExchangeContext</span></span>](hropenabentrywithexchangecontext.md)
  
[<span data-ttu-id="974f2-166">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="974f2-166">HrOpenABEntryWithProviderUID</span></span>](hropenabentrywithprovideruid.md)
  
[<span data-ttu-id="974f2-167">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="974f2-167">HrOpenABEntryWithProviderUIDSupport</span></span>](hropenabentrywithprovideruidsupport.md)
  
[<span data-ttu-id="974f2-168">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="974f2-168">HrOpenABEntryWithResolvedRow</span></span>](hropenabentrywithresolvedrow.md)
  
[<span data-ttu-id="974f2-169">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="974f2-169">HrOpenABEntryWithSupport</span></span>](hropenabentrywithsupport.md)
  
[<span data-ttu-id="974f2-170">Propiedad can�nico de PidTagExchangeProfileSectionId</span><span class="sxs-lookup"><span data-stu-id="974f2-170">PidTagExchangeProfileSectionId Canonical Property</span></span>](pidtagexchangeprofilesectionid-canonical-property.md)


[<span data-ttu-id="974f2-171">How To Open the Global Profile Section</span><span class="sxs-lookup"><span data-stu-id="974f2-171">How To Open the Global Profile Section</span></span>](https://support.microsoft.com/kb/188482)

