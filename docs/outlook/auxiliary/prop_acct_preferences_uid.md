---
title: PROP_ACCT_PREFERENCES_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ec0aac33-624e-48f7-8177-8f7b8db6af7d
description: Recupera el identificador exclusivo (UID) de la sección de perfil que almacena las preferencias de cuenta.
ms.openlocfilehash: 97f1a858c8f58e13b72b8d5f052b35359581b718
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395297"
---
# <a name="propacctpreferencesuid"></a><span data-ttu-id="bb97b-103">PROP_ACCT_PREFERENCES_UID</span><span class="sxs-lookup"><span data-stu-id="bb97b-103">PROP_ACCT_PREFERENCES_UID</span></span>

<span data-ttu-id="bb97b-104">Recupera el identificador exclusivo (UID) de la sección de perfil que almacena las preferencias de cuenta.</span><span class="sxs-lookup"><span data-stu-id="bb97b-104">Retrieves the unique identifier (UID) for the profile section that stores the account preferences.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="bb97b-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="bb97b-105">Quick info</span></span>

<span data-ttu-id="bb97b-106">Vea [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="bb97b-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bb97b-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="bb97b-107">Identifier:</span></span>  <br/> |<span data-ttu-id="bb97b-108">0 x 0022</span><span class="sxs-lookup"><span data-stu-id="bb97b-108">0x0022</span></span>  <br/> |
|<span data-ttu-id="bb97b-109">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="bb97b-109">Property type:</span></span>  <br/> |<span data-ttu-id="bb97b-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bb97b-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bb97b-111">Etiqueta de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="bb97b-111">Property tag:</span></span>  <br/> |<span data-ttu-id="bb97b-112">0x00220102</span><span class="sxs-lookup"><span data-stu-id="bb97b-112">0x00220102</span></span>  <br/> |
|<span data-ttu-id="bb97b-113">Access:</span><span class="sxs-lookup"><span data-stu-id="bb97b-113">Access:</span></span>  <br/> |<span data-ttu-id="bb97b-114">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb97b-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb97b-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bb97b-115">Remarks</span></span>

<span data-ttu-id="bb97b-116">Use **PROP_ACCT_PREFERENCES_UID** en las llamadas a [IMAPISupport::OpenProfileSection](https://msdn.microsoft.com/library/cd1fa994-9531-46c4-94e5-505e7f90b884%28Office.15%29.aspx) para recuperar la sección de perfil que contiene las preferencias de cuenta.</span><span class="sxs-lookup"><span data-stu-id="bb97b-116">Use **PROP_ACCT_PREFERENCES_UID** in calls to [IMAPISupport::OpenProfileSection](https://msdn.microsoft.com/library/cd1fa994-9531-46c4-94e5-505e7f90b884%28Office.15%29.aspx) to retrieve the profile section that contains account preferences.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bb97b-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb97b-117">See also</span></span>

- [<span data-ttu-id="bb97b-118">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="bb97b-118">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="bb97b-119">Acerca de la configuración de bloqueo de correo basura</span><span class="sxs-lookup"><span data-stu-id="bb97b-119">About anti-spam settings</span></span>](about-anti-spam-settings.md)

