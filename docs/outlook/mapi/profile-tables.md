---
title: Tablas de perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd8d60df-98fb-4e08-b547-0836bb31be79
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1046c8d92feec16428329636257ed9c1f0ec8719
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571482"
---
# <a name="profile-tables"></a><span data-ttu-id="6da15-103">Tablas de perfil</span><span class="sxs-lookup"><span data-stu-id="6da15-103">Profile Tables</span></span>

  
  
<span data-ttu-id="6da15-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6da15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6da15-105">La tabla de perfil muestra información acerca de todos los perfiles de asociadas con una aplicación de cliente en particular.</span><span class="sxs-lookup"><span data-stu-id="6da15-105">The profile table lists information about all profiles associated with a particular client application.</span></span> <span data-ttu-id="6da15-106">No hay una tabla de perfil para cada sesión, implementada por MAPI para su uso por los clientes.</span><span class="sxs-lookup"><span data-stu-id="6da15-106">There is one profile table for every session, implemented by MAPI for use by clients.</span></span> 
  
<span data-ttu-id="6da15-107">Los clientes de tener acceso a la tabla de perfil llamando al método [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) .</span><span class="sxs-lookup"><span data-stu-id="6da15-107">Clients access the profile table by calling the [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) method.</span></span> 
  
<span data-ttu-id="6da15-108">La tabla de perfil es una tabla estática.</span><span class="sxs-lookup"><span data-stu-id="6da15-108">The profile table is a static table.</span></span> <span data-ttu-id="6da15-109">Los perfiles que se han marcado para su eliminación no se incluyen en la tabla de perfil.</span><span class="sxs-lookup"><span data-stu-id="6da15-109">Profiles that have been marked for deletion are not included in the profile table.</span></span>
  
<span data-ttu-id="6da15-110">Como con la mayoría de las implementaciones de tabla, si se llama **GetProfileTable** y no hay ningún perfiles disponibles para el cliente, la tabla se crea con cero filas.</span><span class="sxs-lookup"><span data-stu-id="6da15-110">As with most table implementations, if **GetProfileTable** is called and there are no profiles available to the client, the table is created with zero rows.</span></span> 
  
<span data-ttu-id="6da15-111">Las siguientes propiedades que conforman la columna requiere establecer en las tablas de perfiles:</span><span class="sxs-lookup"><span data-stu-id="6da15-111">The following properties make up the required column set in profile tables:</span></span>
  
 <span data-ttu-id="6da15-112">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6da15-112">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span></span> 
  
 <span data-ttu-id="6da15-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6da15-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6da15-114">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="6da15-114">See also</span></span>



[<span data-ttu-id="6da15-115">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="6da15-115">MAPI Tables</span></span>](mapi-tables.md)

