---
title: Propiedad canónica PidTagExchangeProfileSectionId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExchangeProfileSectionId
api_type:
- HeaderDef
ms.assetid: 4ad2f417-be8f-4fc8-9321-82097289074b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ce823159047410a8cea13b7eff5566cd8abaa5b9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699516"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a><span data-ttu-id="29134-103">Propiedad canónica PidTagExchangeProfileSectionId</span><span class="sxs-lookup"><span data-stu-id="29134-103">PidTagExchangeProfileSectionId Canonical Property</span></span>

  
  
<span data-ttu-id="29134-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29134-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29134-105">Contiene un GUID generado de forma dinámica se utiliza para determinar una cuenta cuando esté usando varias cuentas de Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="29134-105">Contains a dynamically generated GUID used to determine an account when you are using multiple Microsoft Exchange Server accounts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="29134-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="29134-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="29134-107">PR_EMSMDB_SECTION_UID</span><span class="sxs-lookup"><span data-stu-id="29134-107">PR_EMSMDB_SECTION_UID</span></span>  <br/> |
|<span data-ttu-id="29134-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="29134-108">Identifier:</span></span>  <br/> |<span data-ttu-id="29134-109">0x3d150102</span><span class="sxs-lookup"><span data-stu-id="29134-109">0x3d150102</span></span>  <br/> |
|<span data-ttu-id="29134-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="29134-110">Data type:</span></span>  <br/> |<span data-ttu-id="29134-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="29134-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="29134-112">Área:</span><span class="sxs-lookup"><span data-stu-id="29134-112">Area:</span></span>  <br/> |<span data-ttu-id="29134-113">Varias cuentas de Exchange</span><span class="sxs-lookup"><span data-stu-id="29134-113">Multiple Exchange Accounts</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29134-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="29134-114">Remarks</span></span>

<span data-ttu-id="29134-115">Microsoft Outlook 2010 y Microsoft Outlook 2013 admiten varias cuentas de Exchange en lugar de una única cuenta de Exchange.</span><span class="sxs-lookup"><span data-stu-id="29134-115">Microsoft Outlook 2010 and Microsoft Outlook 2013 support multiple Exchange accounts instead of one single Exchange account.</span></span> <span data-ttu-id="29134-116">Para dar cabida a varias cuentas de Exchange, se ha cambiado el diseño de perfiles MAPI.</span><span class="sxs-lookup"><span data-stu-id="29134-116">To accommodate multiple Exchange accounts, the MAPI profile layout was changed.</span></span> <span data-ttu-id="29134-117">En Microsoft Office Outlook 2007 y versiones anteriores, los perfiles contiene una sección de perfil fijo dedicada a la configuración de Exchange, como el nombre del servidor, el nombre de usuario y el archivo de carpetas sin conexión (.ost).</span><span class="sxs-lookup"><span data-stu-id="29134-117">In Microsoft Office Outlook 2007 and earlier, profiles contained a fixed profile section dedicated to Exchange settings such as server name, user name, and Offline Folder file (.ost).</span></span> <span data-ttu-id="29134-118">ubicación.</span><span class="sxs-lookup"><span data-stu-id="29134-118">location.</span></span> <span data-ttu-id="29134-119">Estas opciones se han identificado mediante el uso de un identificador único, la propiedad **pbGlobalProfileSectionGuid** .</span><span class="sxs-lookup"><span data-stu-id="29134-119">These settings were identified by using a unique identifier, the **pbGlobalProfileSectionGuid** property.</span></span> <span data-ttu-id="29134-120">La sección que se usa para la configuración de Exchange se denomina la sección de perfil Global de Exchange.</span><span class="sxs-lookup"><span data-stu-id="29134-120">The section used for Exchange settings is called the Exchange Global Profile Section.</span></span> 
  
<span data-ttu-id="29134-121">Una ubicación de sección de perfil fijo ya no es suficiente para dar cabida a varias cuentas de Exchange.</span><span class="sxs-lookup"><span data-stu-id="29134-121">A fixed profile section location is no longer sufficient to accommodate multiple Exchange accounts.</span></span> <span data-ttu-id="29134-122">En su lugar, para cada cuenta de Exchange en su perfil, existe una sección dedicada a la configuración para esa cuenta.</span><span class="sxs-lookup"><span data-stu-id="29134-122">Instead, for each Exchange account in your profile, a section exists that is dedicated to settings for that account.</span></span> <span data-ttu-id="29134-123">La nueva sección usada para la configuración de Exchange se identifica mediante el identificador único **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="29134-123">The new section used for Exchange settings is identified by the unique identifier **emsmdbUID**.</span></span>
  
<span data-ttu-id="29134-124">En la sección de perfil de servicio de mensaje para la cuenta de Exchange, puede encontrar una propiedad que contiene un GUID que se genera de forma dinámica en el momento en que se crea la cuenta.</span><span class="sxs-lookup"><span data-stu-id="29134-124">In the message service profile section for the Exchange account, you can find a property that contains a GUID that is dynamically generated at the time that the account is created.</span></span> <span data-ttu-id="29134-125">Este GUID se almacena en la propiedad **PidTagExchangeProfileSectionId** .</span><span class="sxs-lookup"><span data-stu-id="29134-125">This GUID is stored in the **PidTagExchangeProfileSectionId** property.</span></span> <span data-ttu-id="29134-126">Almacenes de mensajes y los contenedores de la libreta de direcciones exponen una propiedad para determinar qué cuenta de Exchange que pertenecen.</span><span class="sxs-lookup"><span data-stu-id="29134-126">Message stores and address book containers expose a property to determine which Exchange account they belong to.</span></span> <span data-ttu-id="29134-127">Puede tener acceso en la tabla de servicios de mensaje, cada servicio de Exchange expone esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="29134-127">Accessible in the message services table, each Exchange service exposes this property.</span></span> 
  
<span data-ttu-id="29134-128">Puede recuperar esta propiedad a través de una llamada a [IMAPIProp::GetProps](imapiprop-getprops.md) en **PidTagExchangeProfileSectionId** después de la consulta de cualquiera de las siguientes interfaces:</span><span class="sxs-lookup"><span data-stu-id="29134-128">You can retrieve this property through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) on **PidTagExchangeProfileSectionId** after querying for any of the following interfaces:</span></span> 
  
- [<span data-ttu-id="29134-129">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="29134-129">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="29134-130">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="29134-130">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
    
- [<span data-ttu-id="29134-131">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="29134-131">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)
    
<span data-ttu-id="29134-132">Si el objeto no está relacionado con Exchange, la llamada devuelve **MAPI_E_NOT_FOUND**.</span><span class="sxs-lookup"><span data-stu-id="29134-132">If the object is not affiliated with Exchange, the call returns **MAPI_E_NOT_FOUND**.</span></span>
  
<span data-ttu-id="29134-133">Puede restringir los contenedores en un **PidTagExchangeProfileSectionId** al mostrar la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="29134-133">You can restrict containers on a **PidTagExchangeProfileSectionId** when displaying the address book.</span></span> <span data-ttu-id="29134-134">Una vez que haya un contenedor abierto, puede consultar el **emsmdbUID** de él.</span><span class="sxs-lookup"><span data-stu-id="29134-134">Once you have an opened container, you can query the **emsmdbUID** from it.</span></span> <span data-ttu-id="29134-135">También merece la pena tener en cuenta que si se ha seleccionado un destinatario de una libreta de direcciones de Exchange, el destinatario también tiene la **PidTagExchangeProfileSectionId** en su lista de propiedades.</span><span class="sxs-lookup"><span data-stu-id="29134-135">It is also worth noting that if a recipient was selected from an Exchange address book, the recipient also has the **PidTagExchangeProfileSectionId** in its list of properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="29134-136">A lo largo de los ejemplos de código y los encabezados de función, este GUID se conoce como **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="29134-136">Throughout the code samples and function headers, this GUID is known as **emsmdbUID**.</span></span> 
  
<span data-ttu-id="29134-137">Una de las cuentas de Exchange está marcada como la cuenta de Exchange heredada.</span><span class="sxs-lookup"><span data-stu-id="29134-137">One of the Exchange accounts is marked as the legacy Exchange account.</span></span> <span data-ttu-id="29134-138">Normalmente, es la primera cuenta que se agregan al perfil.</span><span class="sxs-lookup"><span data-stu-id="29134-138">Usually, it is the first account added to the profile.</span></span> <span data-ttu-id="29134-139">Todas las llamadas para abrir **pbGlobalProfileSectionGuid** se redirigen a la sección global de Exchange de la cuenta heredada.</span><span class="sxs-lookup"><span data-stu-id="29134-139">Every call to open **pbGlobalProfileSectionGuid** is redirected to the Exchange global section of the legacy account.</span></span> <span data-ttu-id="29134-140">Las llamadas al modelo de objeto que interactúan con la cuenta de Exchange heredado que no sean también interactúan con la cuenta de Exchange heredada.</span><span class="sxs-lookup"><span data-stu-id="29134-140">The object model calls that interact with the non-legacy Exchange account also interact with the legacy Exchange account.</span></span> 
  
<span data-ttu-id="29134-141">El servicio de Exchange heredado tiene la propiedad **PR_EMSMDB_LEGACY** (0x3D18000B), que se establece en **true** en la tabla de servicios de mensaje.</span><span class="sxs-lookup"><span data-stu-id="29134-141">The legacy Exchange service has the property **PR_EMSMDB_LEGACY** (0x3D18000B), which is set to **true** in the message services table.</span></span> 
  
<span data-ttu-id="29134-142">El heredado **emsmdbUID** también se mostrará en la sección de perfil de Outlook Global del perfil como **PidTagExchangeProfileSectionId**.</span><span class="sxs-lookup"><span data-stu-id="29134-142">The legacy **emsmdbUID** is also stamped in the Outlook Global Profile Section of the profile as **PidTagExchangeProfileSectionId**.</span></span> <span data-ttu-id="29134-143">El código escrito para admitir varias cuentas de Exchange no debe tener que recuperar el heredado **emsmdbUID** debido a que debe obtener la correcta **emsmdbUID**, dependiendo de la cuenta de con que su código está interactuando.</span><span class="sxs-lookup"><span data-stu-id="29134-143">Code written to support multiple Exchange accounts should not have to retrieve the legacy **emsmdbUID** because it should get the correct **emsmdbUID**, depending on the account your code is interacting with.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="29134-144">Consulte también</span><span class="sxs-lookup"><span data-stu-id="29134-144">See also</span></span>



[<span data-ttu-id="29134-145">Uso de varias cuentas de Exchange</span><span class="sxs-lookup"><span data-stu-id="29134-145">Using Multiple Exchange Accounts</span></span>](using-multiple-exchange-accounts.md)


[<span data-ttu-id="29134-146">How To Open the Global Profile Section</span><span class="sxs-lookup"><span data-stu-id="29134-146">How To Open the Global Profile Section</span></span>](https://support.microsoft.com/kb/188482)

