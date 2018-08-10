---
title: Información sobre la configuración contra correo no deseado
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 04e00e49-c12d-4517-8574-410741d0fa06
description: Outlook permite a los usuarios especificar la configuración para cada cuenta para ayudar a proteger la cuenta contra correo no deseado. Dicha configuración contra correo no deseada se almacena en una sección designada para esa cuenta en el perfil del usuario.
ms.openlocfilehash: 9d1ad6fcc0748d57dd71cb80460705fcd176fae7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816041"
---
# <a name="about-anti-spam-settings"></a><span data-ttu-id="c862d-104">Información sobre la configuración contra correo no deseado</span><span class="sxs-lookup"><span data-stu-id="c862d-104">About anti-spam settings</span></span>

<span data-ttu-id="c862d-105">Outlook permite a los usuarios especificar la configuración para cada cuenta para ayudar a proteger la cuenta contra correo no deseado.</span><span class="sxs-lookup"><span data-stu-id="c862d-105">Outlook allows users to specify settings for each account to help protect the account from spam.</span></span> <span data-ttu-id="c862d-106">Dicha configuración contra correo no deseada se almacena en una sección designada para esa cuenta en el perfil del usuario.</span><span class="sxs-lookup"><span data-stu-id="c862d-106">Such anti-spam settings are stored in a section designated for that account in the user's profile.</span></span> <span data-ttu-id="c862d-107">Utilice la propiedad [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) para obtener el identificador único (UID) para la sección en el perfil que almacena las preferencias del usuario para esta cuenta, incluida la configuración contra correo no deseada.</span><span class="sxs-lookup"><span data-stu-id="c862d-107">Use the [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) property to obtain the unique ID (UID) for the section in the profile that stores the user's preferences for this account, including the anti-spam settings.</span></span> 
  
<span data-ttu-id="c862d-108">Utilice las propiedades siguientes para obtener la configuración contra correo no deseada para la cuenta:</span><span class="sxs-lookup"><span data-stu-id="c862d-108">Use the following properties to obtain anti-spam settings for the account:</span></span>
  
- <span data-ttu-id="c862d-109">[PidTagSpamJunkSenders](http://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)— especifica una lista delimitada por punto y coma de direcciones de correo electrónico y dominios que el usuario haya especificado como remitentes bloqueados para la cuenta.</span><span class="sxs-lookup"><span data-stu-id="c862d-109">[PidTagSpamJunkSenders](http://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as blocked senders for the account.</span></span>
    
- <span data-ttu-id="c862d-110">[PidTagSpamThreshold](http://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx): especifica el nivel de que el usuario ha especificado para la cuenta de filtrado de correo no deseado.</span><span class="sxs-lookup"><span data-stu-id="c862d-110">[PidTagSpamThreshold](http://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)—Specifies the level of spam-filtering that the user has specified for the account.</span></span> <span data-ttu-id="c862d-111">En la siguiente tabla muestra los valores admitidos.</span><span class="sxs-lookup"><span data-stu-id="c862d-111">The following table shows the supported values.</span></span>
    
|<span data-ttu-id="c862d-112">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="c862d-112">Supported value</span></span> |<span data-ttu-id="c862d-113">Definición</span><span class="sxs-lookup"><span data-stu-id="c862d-113">Definition</span></span> |
|:-----|:-----|
|<span data-ttu-id="c862d-114">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c862d-114">None</span></span>  <br/> |<span data-ttu-id="c862d-115">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="c862d-115">0xFFFFFFFF</span></span>  <br/> |
|<span data-ttu-id="c862d-116">Low</span><span class="sxs-lookup"><span data-stu-id="c862d-116">Low</span></span>  <br/> |<span data-ttu-id="c862d-117">0 x 00000006</span><span class="sxs-lookup"><span data-stu-id="c862d-117">0x00000006</span></span>  <br/> |
|<span data-ttu-id="c862d-118">Medio</span><span class="sxs-lookup"><span data-stu-id="c862d-118">Medium</span></span>  <br/> |<span data-ttu-id="c862d-119">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="c862d-119">0x00000005</span></span>  <br/> |
|<span data-ttu-id="c862d-120">High</span><span class="sxs-lookup"><span data-stu-id="c862d-120">High</span></span>  <br/> |<span data-ttu-id="c862d-121">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="c862d-121">0x00000003</span></span>  <br/> |
   
- <span data-ttu-id="c862d-122">[PidTagSpamTrustedRecipients](http://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)— especifica una lista delimitada por punto y coma de direcciones de correo electrónico y dominios que el usuario ha especificado como destinatarios de confianza para la cuenta.</span><span class="sxs-lookup"><span data-stu-id="c862d-122">[PidTagSpamTrustedRecipients](http://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as trusted recipients for the account.</span></span>
    
- <span data-ttu-id="c862d-123">[PidTagSpamTrustedSenders](http://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)— especifica una lista delimitada por punto y coma de direcciones de correo electrónico y dominios que el usuario ha especificado como remitentes de confianza para la cuenta.</span><span class="sxs-lookup"><span data-stu-id="c862d-123">[PidTagSpamTrustedSenders](http://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as trusted senders for the account.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c862d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="c862d-124">See also</span></span>

- [<span data-ttu-id="c862d-125">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="c862d-125">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="c862d-126">Agregar nombres a las listas del filtro de correo electrónico no deseado</span><span class="sxs-lookup"><span data-stu-id="c862d-126">Add names to the Junk Email Filter lists</span></span>](http://office.microsoft.com/en-us/outlook-help/add-names-to-the-junk-email-filter-lists-HA010355043.aspx?CTT=1)
