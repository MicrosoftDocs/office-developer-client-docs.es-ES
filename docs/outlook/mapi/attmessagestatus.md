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
ms.openlocfilehash: 158e4db4b0f80b80385e85c8afa16fa515dc61b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816475"
---
# <a name="attmessagestatus"></a><span data-ttu-id="c00f4-103">attMessageStatus</span><span class="sxs-lookup"><span data-stu-id="c00f4-103">attMessageStatus</span></span>

  
  
<span data-ttu-id="c00f4-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c00f4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c00f4-105">Indicadores de mensaje MAPI se asignan a marcas TNEF para preservar la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="c00f4-105">MAPI message flags are mapped to TNEF flags to preserve backward compatibility.</span></span> <span data-ttu-id="c00f4-106">Todos los indicadores se agrupan juntos y codificados en un solo byte.</span><span class="sxs-lookup"><span data-stu-id="c00f4-106">All the flags are grouped together and encoded in a single byte.</span></span> <span data-ttu-id="c00f4-107">Las asignaciones son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="c00f4-107">The mappings are as follows:</span></span>
  
|<span data-ttu-id="c00f4-108">**Indicadores de mensaje MAPI**</span><span class="sxs-lookup"><span data-stu-id="c00f4-108">**MAPI message flags**</span></span>|<span data-ttu-id="c00f4-109">**Indicadores TNEF**</span><span class="sxs-lookup"><span data-stu-id="c00f4-109">**TNEF flags**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c00f4-110">MSGFLAG_READ</span><span class="sxs-lookup"><span data-stu-id="c00f4-110">MSGFLAG_READ</span></span>  <br/> |<span data-ttu-id="c00f4-111">fmsRead</span><span class="sxs-lookup"><span data-stu-id="c00f4-111">fmsRead</span></span>  <br/> |
|<span data-ttu-id="c00f4-112">MSGFLAG_UNMODIFED</span><span class="sxs-lookup"><span data-stu-id="c00f4-112">MSGFLAG_UNMODIFED</span></span>  <br/> |<span data-ttu-id="c00f4-113">~ fmsModified</span><span class="sxs-lookup"><span data-stu-id="c00f4-113">~fmsModified</span></span>  <br/> |
|<span data-ttu-id="c00f4-114">MSGFLAG_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="c00f4-114">MSGFLAG_SUBMIT</span></span>  <br/> |<span data-ttu-id="c00f4-115">fmsSubmitted</span><span class="sxs-lookup"><span data-stu-id="c00f4-115">fmsSubmitted</span></span>  <br/> |
|<span data-ttu-id="c00f4-116">MSGFLAG_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="c00f4-116">MSGFLAG_HASATTACH</span></span>  <br/> |<span data-ttu-id="c00f4-117">fmsHasAttach</span><span class="sxs-lookup"><span data-stu-id="c00f4-117">fmsHasAttach</span></span>  <br/> |
|<span data-ttu-id="c00f4-118">MSGFLAG_UNSENT</span><span class="sxs-lookup"><span data-stu-id="c00f4-118">MSGFLAG_UNSENT</span></span>  <br/> |<span data-ttu-id="c00f4-119">fmsLocal</span><span class="sxs-lookup"><span data-stu-id="c00f4-119">fmsLocal</span></span>  <br/> |
   
<span data-ttu-id="c00f4-120">Estos marcadores se definen en el TNEF. Archivo de encabezado H.</span><span class="sxs-lookup"><span data-stu-id="c00f4-120">These flags are defined in the TNEF.H header file.</span></span>
  

