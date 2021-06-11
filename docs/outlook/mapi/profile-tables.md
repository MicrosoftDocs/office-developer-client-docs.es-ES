---
title: Tablas de perfiles
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd8d60df-98fb-4e08-b547-0836bb31be79
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 15c07c05af82389bce697c300cd9b1d504e98736
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424353"
---
# <a name="profile-tables"></a><span data-ttu-id="c6aba-103">Tablas de perfiles</span><span class="sxs-lookup"><span data-stu-id="c6aba-103">Profile Tables</span></span>

  
  
<span data-ttu-id="c6aba-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6aba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6aba-105">En la tabla de perfiles se muestra información sobre todos los perfiles asociados a una aplicación cliente determinada.</span><span class="sxs-lookup"><span data-stu-id="c6aba-105">The profile table lists information about all profiles associated with a particular client application.</span></span> <span data-ttu-id="c6aba-106">Hay una tabla de perfil para cada sesión, implementada por MAPI para su uso por los clientes.</span><span class="sxs-lookup"><span data-stu-id="c6aba-106">There is one profile table for every session, implemented by MAPI for use by clients.</span></span> 
  
<span data-ttu-id="c6aba-107">Los clientes tienen acceso a la tabla de perfiles mediante una llamada [al método IProfAdmin::GetProfileTable.](iprofadmin-getprofiletable.md)</span><span class="sxs-lookup"><span data-stu-id="c6aba-107">Clients access the profile table by calling the [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) method.</span></span> 
  
<span data-ttu-id="c6aba-108">La tabla de perfiles es una tabla estática.</span><span class="sxs-lookup"><span data-stu-id="c6aba-108">The profile table is a static table.</span></span> <span data-ttu-id="c6aba-109">Los perfiles marcados para su eliminación no se incluyen en la tabla de perfiles.</span><span class="sxs-lookup"><span data-stu-id="c6aba-109">Profiles that have been marked for deletion are not included in the profile table.</span></span>
  
<span data-ttu-id="c6aba-110">Al igual que con la mayoría de las implementaciones de tabla, si se llama a **GetProfileTable** y no hay perfiles disponibles para el cliente, la tabla se crea con cero filas.</span><span class="sxs-lookup"><span data-stu-id="c6aba-110">As with most table implementations, if **GetProfileTable** is called and there are no profiles available to the client, the table is created with zero rows.</span></span> 
  
<span data-ttu-id="c6aba-111">Las siguientes propiedades son la columna necesaria establecida en las tablas de perfiles:</span><span class="sxs-lookup"><span data-stu-id="c6aba-111">The following properties make up the required column set in profile tables:</span></span>
  
 <span data-ttu-id="c6aba-112">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c6aba-112">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span></span> 
  
 <span data-ttu-id="c6aba-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c6aba-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c6aba-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6aba-114">See also</span></span>



[<span data-ttu-id="c6aba-115">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="c6aba-115">MAPI Tables</span></span>](mapi-tables.md)

