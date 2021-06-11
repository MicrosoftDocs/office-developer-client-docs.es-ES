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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316432"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a><span data-ttu-id="db0f1-103">Propiedad canónica PidTagExchangeProfileSectionId</span><span class="sxs-lookup"><span data-stu-id="db0f1-103">PidTagExchangeProfileSectionId Canonical Property</span></span>

  
  
<span data-ttu-id="db0f1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db0f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db0f1-105">Contiene un GUID generado dinámicamente que se usa para determinar una cuenta cuando se usan varias Microsoft Exchange Server cuentas.</span><span class="sxs-lookup"><span data-stu-id="db0f1-105">Contains a dynamically generated GUID used to determine an account when you are using multiple Microsoft Exchange Server accounts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="db0f1-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="db0f1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="db0f1-107">PR_EMSMDB_SECTION_UID</span><span class="sxs-lookup"><span data-stu-id="db0f1-107">PR_EMSMDB_SECTION_UID</span></span>  <br/> |
|<span data-ttu-id="db0f1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="db0f1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="db0f1-109">0x3d150102</span><span class="sxs-lookup"><span data-stu-id="db0f1-109">0x3d150102</span></span>  <br/> |
|<span data-ttu-id="db0f1-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="db0f1-110">Data type:</span></span>  <br/> |<span data-ttu-id="db0f1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="db0f1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="db0f1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="db0f1-112">Area:</span></span>  <br/> |<span data-ttu-id="db0f1-113">Varias cuentas de Exchange</span><span class="sxs-lookup"><span data-stu-id="db0f1-113">Multiple Exchange Accounts</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db0f1-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="db0f1-114">Remarks</span></span>

<span data-ttu-id="db0f1-115">Microsoft Outlook 2010 y Microsoft Outlook 2013 admiten varias Exchange en lugar de una sola Exchange cuenta.</span><span class="sxs-lookup"><span data-stu-id="db0f1-115">Microsoft Outlook 2010 and Microsoft Outlook 2013 support multiple Exchange accounts instead of one single Exchange account.</span></span> <span data-ttu-id="db0f1-116">Para dar cabida a varias Exchange, se cambió el diseño del perfil MAPI.</span><span class="sxs-lookup"><span data-stu-id="db0f1-116">To accommodate multiple Exchange accounts, the MAPI profile layout was changed.</span></span> <span data-ttu-id="db0f1-117">En Microsoft Office Outlook 2007 y versiones anteriores, los perfiles contenían una sección de perfil fijo dedicada a la configuración de Exchange, como el nombre del servidor, el nombre de usuario y el archivo de carpeta sin conexión (.ost).</span><span class="sxs-lookup"><span data-stu-id="db0f1-117">In Microsoft Office Outlook 2007 and earlier, profiles contained a fixed profile section dedicated to Exchange settings such as server name, user name, and Offline Folder file (.ost).</span></span> <span data-ttu-id="db0f1-118">ubicación.</span><span class="sxs-lookup"><span data-stu-id="db0f1-118">location.</span></span> <span data-ttu-id="db0f1-119">Esta configuración se identificó mediante un identificador único, la **propiedad pbGlobalProfileSectionGuid.**</span><span class="sxs-lookup"><span data-stu-id="db0f1-119">These settings were identified by using a unique identifier, the **pbGlobalProfileSectionGuid** property.</span></span> <span data-ttu-id="db0f1-120">La sección usada para la Exchange se denomina Exchange de perfil global.</span><span class="sxs-lookup"><span data-stu-id="db0f1-120">The section used for Exchange settings is called the Exchange Global Profile Section.</span></span> 
  
<span data-ttu-id="db0f1-121">Una ubicación de sección de perfil fijo ya no es suficiente para dar cabida a varias Exchange cuentas.</span><span class="sxs-lookup"><span data-stu-id="db0f1-121">A fixed profile section location is no longer sufficient to accommodate multiple Exchange accounts.</span></span> <span data-ttu-id="db0f1-122">En su lugar, para Exchange cuenta del perfil, existe una sección dedicada a la configuración de esa cuenta.</span><span class="sxs-lookup"><span data-stu-id="db0f1-122">Instead, for each Exchange account in your profile, a section exists that is dedicated to settings for that account.</span></span> <span data-ttu-id="db0f1-123">La nueva sección usada para la Exchange se identifica mediante el identificador único **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="db0f1-123">The new section used for Exchange settings is identified by the unique identifier **emsmdbUID**.</span></span>
  
<span data-ttu-id="db0f1-124">En la sección perfil de servicio de mensajes de la cuenta Exchange, puede encontrar una propiedad que contenga un GUID que se genera dinámicamente en el momento en que se crea la cuenta.</span><span class="sxs-lookup"><span data-stu-id="db0f1-124">In the message service profile section for the Exchange account, you can find a property that contains a GUID that is dynamically generated at the time that the account is created.</span></span> <span data-ttu-id="db0f1-125">Este GUID se almacena en la **propiedad PidTagExchangeProfileSectionId.**</span><span class="sxs-lookup"><span data-stu-id="db0f1-125">This GUID is stored in the **PidTagExchangeProfileSectionId** property.</span></span> <span data-ttu-id="db0f1-126">Los almacenes de mensajes y los contenedores de libreta de direcciones exponen una propiedad para determinar Exchange cuenta a la que pertenecen.</span><span class="sxs-lookup"><span data-stu-id="db0f1-126">Message stores and address book containers expose a property to determine which Exchange account they belong to.</span></span> <span data-ttu-id="db0f1-127">Accesible en la tabla de servicios de mensajes, Exchange servicio expone esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="db0f1-127">Accessible in the message services table, each Exchange service exposes this property.</span></span> 
  
<span data-ttu-id="db0f1-128">Puede recuperar esta propiedad mediante una llamada a [IMAPIProp::GetProps](imapiprop-getprops.md) en **PidTagExchangeProfileSectionId** después de consultar cualquiera de las interfaces siguientes:</span><span class="sxs-lookup"><span data-stu-id="db0f1-128">You can retrieve this property through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) on **PidTagExchangeProfileSectionId** after querying for any of the following interfaces:</span></span> 
  
- [<span data-ttu-id="db0f1-129">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="db0f1-129">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="db0f1-130">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="db0f1-130">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
    
- [<span data-ttu-id="db0f1-131">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="db0f1-131">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)
    
<span data-ttu-id="db0f1-132">Si el objeto no está asociado con Exchange, la llamada devuelve **MAPI_E_NOT_FOUND**.</span><span class="sxs-lookup"><span data-stu-id="db0f1-132">If the object is not affiliated with Exchange, the call returns **MAPI_E_NOT_FOUND**.</span></span>
  
<span data-ttu-id="db0f1-133">Puede restringir contenedores en **un PidTagExchangeProfileSectionId** al mostrar la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="db0f1-133">You can restrict containers on a **PidTagExchangeProfileSectionId** when displaying the address book.</span></span> <span data-ttu-id="db0f1-134">Una vez que tenga un contenedor abierto, puede consultar **el emsmdbUID** desde él.</span><span class="sxs-lookup"><span data-stu-id="db0f1-134">Once you have an opened container, you can query the **emsmdbUID** from it.</span></span> <span data-ttu-id="db0f1-135">También es importante tener en cuenta que si un destinatario se seleccionó de una libreta de direcciones de Exchange, el destinatario también tiene **pidTagExchangeProfileSectionId** en su lista de propiedades.</span><span class="sxs-lookup"><span data-stu-id="db0f1-135">It is also worth noting that if a recipient was selected from an Exchange address book, the recipient also has the **PidTagExchangeProfileSectionId** in its list of properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="db0f1-136">A lo largo de los ejemplos de código y los encabezados de función, este GUID se conoce como **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="db0f1-136">Throughout the code samples and function headers, this GUID is known as **emsmdbUID**.</span></span> 
  
<span data-ttu-id="db0f1-137">Una de las Exchange cuenta está marcada como cuenta heredada Exchange cuenta.</span><span class="sxs-lookup"><span data-stu-id="db0f1-137">One of the Exchange accounts is marked as the legacy Exchange account.</span></span> <span data-ttu-id="db0f1-138">Normalmente, es la primera cuenta agregada al perfil.</span><span class="sxs-lookup"><span data-stu-id="db0f1-138">Usually, it is the first account added to the profile.</span></span> <span data-ttu-id="db0f1-139">Cada llamada para abrir **pbGlobalProfileSectionGuid** se redirige a la Exchange global de la cuenta heredada.</span><span class="sxs-lookup"><span data-stu-id="db0f1-139">Every call to open **pbGlobalProfileSectionGuid** is redirected to the Exchange global section of the legacy account.</span></span> <span data-ttu-id="db0f1-140">Las llamadas del modelo de objetos que interactúan con la cuenta de Exchange no heredada también interactúan con la cuenta Exchange heredada.</span><span class="sxs-lookup"><span data-stu-id="db0f1-140">The object model calls that interact with the non-legacy Exchange account also interact with the legacy Exchange account.</span></span> 
  
<span data-ttu-id="db0f1-141">El servicio de Exchange heredado tiene la propiedad **PR_EMSMDB_LEGACY** (0x3D18000B), que se establece en **true** en la tabla de servicios de mensajes.</span><span class="sxs-lookup"><span data-stu-id="db0f1-141">The legacy Exchange service has the property **PR_EMSMDB_LEGACY** (0x3D18000B), which is set to **true** in the message services table.</span></span> 
  
<span data-ttu-id="db0f1-142">El **emsmdbUID** heredado también se marca en la sección Outlook perfil global del perfil como **PidTagExchangeProfileSectionId**.</span><span class="sxs-lookup"><span data-stu-id="db0f1-142">The legacy **emsmdbUID** is also stamped in the Outlook Global Profile Section of the profile as **PidTagExchangeProfileSectionId**.</span></span> <span data-ttu-id="db0f1-143">El código escrito para admitir varias cuentas de Exchange no debe tener que recuperar el **emsmdbUID** heredado porque debe obtener el **emsmdbUID** correcto, en función de la cuenta con la que interactúe el código.</span><span class="sxs-lookup"><span data-stu-id="db0f1-143">Code written to support multiple Exchange accounts should not have to retrieve the legacy **emsmdbUID** because it should get the correct **emsmdbUID**, depending on the account your code is interacting with.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="db0f1-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="db0f1-144">See also</span></span>



[<span data-ttu-id="db0f1-145">Uso de varias Exchange cuentas</span><span class="sxs-lookup"><span data-stu-id="db0f1-145">Using Multiple Exchange Accounts</span></span>](using-multiple-exchange-accounts.md)


[<span data-ttu-id="db0f1-146">How To Open the Global Profile Section</span><span class="sxs-lookup"><span data-stu-id="db0f1-146">How To Open the Global Profile Section</span></span>](https://support.microsoft.com/kb/188482)

