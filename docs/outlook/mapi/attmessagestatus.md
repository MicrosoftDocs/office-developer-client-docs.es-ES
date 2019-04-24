---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d4dc72309ff090317b2353cab0b4fc2c5be41181
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318217"
---
# <a name="attmessagestatus"></a><span data-ttu-id="7384b-103">attMessageStatus</span><span class="sxs-lookup"><span data-stu-id="7384b-103">attMessageStatus</span></span>

  
  
<span data-ttu-id="7384b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7384b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7384b-105">Las marcas de mensajes MAPI se asignan a las marcas TNEF para mantener la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="7384b-105">MAPI message flags are mapped to TNEF flags to preserve backward compatibility.</span></span> <span data-ttu-id="7384b-106">Todas las marcas se agrupan y se codifican en un solo byte.</span><span class="sxs-lookup"><span data-stu-id="7384b-106">All the flags are grouped together and encoded in a single byte.</span></span> <span data-ttu-id="7384b-107">Las asignaciones son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="7384b-107">The mappings are as follows:</span></span>
  
|<span data-ttu-id="7384b-108">**Marcas de mensaje MAPI**</span><span class="sxs-lookup"><span data-stu-id="7384b-108">**MAPI message flags**</span></span>|<span data-ttu-id="7384b-109">**Marcas TNEF**</span><span class="sxs-lookup"><span data-stu-id="7384b-109">**TNEF flags**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7384b-110">MSGFLAG_READ</span><span class="sxs-lookup"><span data-stu-id="7384b-110">MSGFLAG_READ</span></span>  <br/> |<span data-ttu-id="7384b-111">fmsRead</span><span class="sxs-lookup"><span data-stu-id="7384b-111">fmsRead</span></span>  <br/> |
|<span data-ttu-id="7384b-112">MSGFLAG_UNMODIFED</span><span class="sxs-lookup"><span data-stu-id="7384b-112">MSGFLAG_UNMODIFED</span></span>  <br/> |<span data-ttu-id="7384b-113">~ fmsModified</span><span class="sxs-lookup"><span data-stu-id="7384b-113">~fmsModified</span></span>  <br/> |
|<span data-ttu-id="7384b-114">MSGFLAG_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="7384b-114">MSGFLAG_SUBMIT</span></span>  <br/> |<span data-ttu-id="7384b-115">fmsSubmitted</span><span class="sxs-lookup"><span data-stu-id="7384b-115">fmsSubmitted</span></span>  <br/> |
|<span data-ttu-id="7384b-116">MSGFLAG_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="7384b-116">MSGFLAG_HASATTACH</span></span>  <br/> |<span data-ttu-id="7384b-117">fmsHasAttach</span><span class="sxs-lookup"><span data-stu-id="7384b-117">fmsHasAttach</span></span>  <br/> |
|<span data-ttu-id="7384b-118">MSGFLAG_UNSENT</span><span class="sxs-lookup"><span data-stu-id="7384b-118">MSGFLAG_UNSENT</span></span>  <br/> |<span data-ttu-id="7384b-119">fmsLocal</span><span class="sxs-lookup"><span data-stu-id="7384b-119">fmsLocal</span></span>  <br/> |
   
<span data-ttu-id="7384b-120">Estas marcas se definen en la TNEF. H archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="7384b-120">These flags are defined in the TNEF.H header file.</span></span>
  

